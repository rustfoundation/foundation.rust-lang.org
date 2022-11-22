---
title: Secure App Development with Rust's Memory Model
byline: >-
  Jane Lewis (Software Developer) & Nathan West (Senior Software Developer) of
  1Password
description: 'Rust Foundation Guest Blog Series: 1Password''s Jane Lewis & Nathan West'
date: 2022-11-22T15:30:00Z
tags:
  - guest blog series
index: false
layout: layouts/news.njk
---
&nbsp;

<img src="/img/news/2022-11-22-secure-app-development-with-rusts-memory-model/Guest-Blog.png" width="580" height="326" alt="Orange gradient background with white rust foundation logo up top (letter &quot;R&quot; inside gear icon) with the following white italicized text: “Guest “Blog Series”. Underneath is the title “Securing App Development with Rust’s Memory Model.” Two circular zig-zag shapes frame the headshots of both authors: Jane Lewis and Nathan West." title="Securing App Development with Rust's Memory Model" />

*Welcome to another installment in the Rust Foundation&nbsp;*<a target="_blank" rel="noopener" href="https://foundation.rust-lang.org/tags/guest%20blog%20series/">guest blog series</a>,*&nbsp;written by members of the Rust Foundation and/or community. Today, we are pleased to have a post from Jane Lewis (Software Developer) & Nathan West (Senior Developer) of <a target="_blank" rel="noopener" href="https://1password.com/">1Password</a>— a Rust Foundation Silver Member. Read on to learn about how this team is using Rust to go beyond memory safety when making their password manager as safe as it can possibly be..*

---

## **Modern security applications cannot afford to be memory unsafe**

In 2019, Microsoft reported at a security conference that 70% of all security vulnerabilities they encountered were due to memory <a target="_blank" rel="noopener" href=" https://msrc-blog.microsoft.com/2019/07/16/a-proactive-approach-to-more-secure-code">vulnerabilities</a>. Google has reported <a target="_blank" rel="noopener" href="https://www.chromium.org/Home/chromium-security/memory-safety">similar statistics for vulnerabilities in Chrome</a>.

Using a memory-safe language, like Python or Java, prevents buffer overflows and other common exploits from occurring. However, these languages usually rely on a garbage collector, which makes finalization and de-allocation of memory a non-deterministic process. Unless a zeroization procedure is directly called on a piece of memory, this leaves potentially secret data lingering in that memory for an unknown amount of time– possibly even forever– where it is theoretically vulnerable to exploits from other parts of the program, dumps, or side channel attacks. In this article, we’d like to talk about how **1Password is using Rust to go beyond memory safety when making our password manager as safe as it can possibly be.**

## **A quick primer on memory allocation**

Virtually all languages have some concept of memory allocation, though different languages expose or hide these concepts from the developer, depending on how they’re designed.&nbsp; There’s a number of ways that languages operate on allocated memory or allow developers to access it, but the underlying concepts are basically the same for all languages.

Fundamentally, a memory allocator is responsible for taking a single, large block of memory (often several KB or MB) and slicing it up into manageable chunks for the program to use. For example, if your 1Password account password is 29 characters long, that will usually take up about 29 bytes of memory, so the allocator will find a block of 29 bytes of memory out of its much larger block and give it to the program to store the password. This is called allocating memory.

To ensure the allocator doesn’t run out of memory, programs must also inform it when they are *done* with memory, so that it can be reused by future allocations. This is called de-allocating memory. When you deallocate memory, allocators will usually mark the block as available to future allocations.To stay as fast as possible, they won’t go out of their way to clear any of the data *in* that block.

Apps like 1Password will often have thousands of these small blocks while they’re running, ranging from dozens to (rarely) thousands of bytes. New blocks may be allocated and old blocks de-allocated hundreds of times per second, and modern allocators like Microsoft’s&nbsp;[<u>mimalloc</u>](https://github.com/microsoft/mimalloc) use complex algorithms to keep track of where these blocks are in the larger original block. This ensures new allocations can happen as quickly as possible, and that de-allocated memory can be reused as efficiently as possible.

## **Rust keeps us from compromising on memory safety**

Here at 1Password, our number one priority is keeping users secure. One way we do this is by destroying sensitive information in memory as soon as possible. That means your decrypted items are disposed whenever 1Password locks, and your account password and decryption keys are disposed of as soon as unlocking is complete.

*Note:*&nbsp;*For more information about how 1Password encrypts your data and manages cryptographic keys, check out our <a target="_blank" rel="noopener" href="https://1password.com/security/#security-white-paper">security design whitepaper</a>*.

But here's the issue: traditionally, we've used different languages and frameworks to build the 1Password app for each platform, leading to limitations unique to each language. For example, with garbage-collected languages, controlling when sensitive data is de-allocated is tricky, especially since zeroing-out memory is an operation frequently optimized away by compilers.

With 1Password 8, we’re taking an entirely new approach to this problem, empowered by a cross-platform core framework written entirely in Rust. This core framework contains our business logic, view model code, and, most critically, our data model and secrets management.

Rust’s direct control over memory management is a breath of fresh air for security programmers because it gives us memory safety while being just as precise as C or C++ in how memory is allocated and deallocated. Rust directly ties resource allocation to data initialization (commonly known as RAII - Resource Allocation Is Initialization). All data in Rust is “owned”, and is disposed of at the same time as its owner (or sooner). This means that the lifetime of a secret can easily be traced to the secret itself, which takes far less mental overhead – the secret will be disposed of, and relevant memory deallocated, as soon as it’s done being used.

Rust’s reduction in mental overhead is also a big win for security. Since programmers can trust the compiler to keep their applications memory-safe, and precisely track where sensitive data is being allocated, they can architect higher-level functionality without having to worry about a shaky memory foundation.

But these are all somewhat abstract improvements. What are some actual examples of Rust making our security tighter?

### **Zeroization**

One major problem that Rust and its ecosystem helped us with is zeroization of memory. In most languages&nbsp; – including Rust itself – simply de-allocating memory quickly may not be sufficient. While the data is no longer accessible under normal program operation, the data is still in memory and theoretically accessible under extremely abnormal circumstances, since allocators generally don’t go out of their way to erase data when deallocating.&nbsp;

We wanted to go the extra mile and ensure that sensitive data is fully erased before it’s de-allocated. The [<u>zeroize</u>](https://crates.io/crates/zeroize) crate does exactly this– by storing data inside of `zeroizing`, we can ensure that that data is *always* fully erased when it’s being disposed of, regardless of when or how that happens. Combined with Rust’s lifetime-oriented memory management, this ensures that data is disposed of as soon as it’s no longer needed. It also means that cryptographic keys are immediately zeroed out in memory once we finish using them.

### Correctness with ownership and types

Another major benefit is Rust’s type system which, as much as possible, ensures that our use of cryptographic APIs is correct. Rust has a famously strong and restrictive [<u>type system</u>](https://doc.rust-lang.org/reference/types.html), allowing developers to tightly circumscribe how different kinds of data may be used, and even how *often* they may be used. There are simple examples – every type of cryptographic secret has a unique type, for instance, so there’s no risk of mixing up Secret Keys, account passwords, Master Unlock Keys, SRP components, or anything else. However, these examples are common to any typical strongly-typed language – Rust’s unique ownership system lets us take this even farther.

Consider the problem of a cryptographic nonce, which is a small value used in encryption that must only ever be used once. We’d like to ensure as strictly as possible that this single-use requirement is upheld. Rust’s type system allows us to guarantee this at compile time by providing a notion of “ownership” of data. All data in Rust is “owned” in exactly one place. Ownership can be transferred, but this means that the previous owner of the data no longer has access to it. We can therefore split up the cryptographic nonce into two types: `UsedNonce` and `UnusedNonce`. When a new `UnusedNonce` is created, it’s guaranteed to be unique, and we explicitly omit any APIs that would allow it to be duplicated (like `Clone` or `Serialize`).&nbsp;

We can then *require* that an encryption operation includes transferring ownership of an `UnusedNonce` into the encryption. After encryption finishes, it returns to us a new `UsedNonce`. Conceptually, this is exactly the same piece of data as the original `UnusedNonce`. But because that data has a different type, it can only ever be used to *decrypt* something – never to create a new encryption. And because we lost ownership of the original `UnusedNonce`, it’s no longer possible for it to be used for additional encryption.

## **Looking towards the future**

Idiomatic Rust gives developers some assurance of security without having to compromise on readability or structure, but there’s always room to grow for the future. At the moment, the `zeroize` crate can’t clear CPU registers, in which residual cryptographic secrets may reside. It also can’t `zeroize` every instance of a buffer if the buffer has been re-allocated. Luckily, the latter issue is solved by the [<u>secrecy</u>](https://crates.io/crates/secrecy) crate, which prevents re-allocation (or any mutation at all) of secret data.&nbsp;

We’re always looking for new ways to keep 1Password as secure as possible – not just in theory, with whitepapers and cryptographic algorithm designs – but in practice, with systems that aggressively check our work during development and defensively manage data when the app is running. We believe there is no better language up to that challenge than Rust.

---

*Thank you for reading this post in the Rust Foundation&nbsp;[guest blog series](https://foundation.rust-lang.org/tags/guest%20blog%20series/). Stay tuned for more installments in the future\!*