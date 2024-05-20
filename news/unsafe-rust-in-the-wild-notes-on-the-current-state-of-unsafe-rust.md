---
title: 'Unsafe Rust in the Wild: Notes on the Current State of Unsafe Rust'
byline: Rust Foundation Team
description: >-
  With so many damaging software exploits haunting our industry and so much at
  stake, software foundations, technology consortiums, and governments around
  the world are taking notice and advocating for improved programming practices
  and tools. 
date: 2024-05-21T12:30:00Z
tags:
  - rust
  - foundation
  - security
index: true
layout: layouts/news.njk
---
Programs access memory – this concept is fundamental to computing. Depending on the programming language used to write code, there are various ways to manage the allocation and use of that memory. Each approach requires care and caution.

Unintended, out-of-scope access to a program’s memory regions can expose sensitive data or serve as an entry point for exploitation, posing significant risk and potentially contributing to zero-day attacks. In short, whether a programmer manages and allocates memory manually or relies on the language and compiler to do it for them, robust memory management practices are a necessity.

Memory safety issues account for a significant share of software vulnerabilities. \[1\] Malicious actors are well aware of this and use an evolving set of tactics to exploit memory-unsafe code in some of the most recognizable and damaging software attacks in recent years, such as Heartbleed.

With so many damaging software exploits haunting our industry and so much at stake, software foundations, technology consortiums, and governments around the world are taking notice and advocating for improved programming practices and tools.

## The Power and Promise of Rust

The Rust programming language is frequently cited by memory-safety advocates as one of the most secure programming languages on the market today. A memory-safe language by default through a concept called ownership, Rust provides rules and guarantees for memory management and centers security as a first-class concept.

Programs using Rust are *unable* to compile if memory management rules are violated, essentially eliminating the possibility of a memory issue at runtime. This provides Rust developers and users of applications written in Rust with a high degree of confidence that memory vulnerabilities need not be a concern.

## Safe Rust and “Unsafe Rust”

Although Rust is a powerful tool for memory-safety and security, the power of its safety checks can become limiting when the program cannot actually go wrong but the compiler is unable to guarantee that itself; the programmer can prove the impossibility of undefined behavior in ways not available to the compiler. In these instances, Rust programmers will apply the \`unsafe\` keyword to indicate a function or code segment which has a) additional safety considerations or b) invariants a programmer must manually follow to guarantee safety that are not necessarily expressible by Rust or the function itself. The \`unsafe\` keyword enables developers to dereference a raw pointer, modify a mutable static variable, and, crucially, call unsafe functions.

While using Unsafe Rust can theoretically produce vulnerabilities similar to that of memory-unsafe languages, there are four primary safeguards to minimize those chances to near zero:

1. Using the \`unsafe\` keyword in Rust is an explicit act, requiring the developer to opt-in to proceed. This means that you will never be able to enter an unsafe context within your Rust code without making the conscious effort to do so; other languages may allow you to call unsafe or unmanaged code directly.
2. \`unsafe\` has to be isolated in its own code blocks. If anything goes wrong while using Unsafe Rust, it is clear what code has likely caused the issue.
3. There are a limited number of ways to use \`unsafe\` \[2\] and all safe Rust code continues to have its normal safety checks even inside an unsafe block.
4. The Rust type system still provides safety constraints for safe Rust types even within an \`unsafe\` block.

These additional measures bolstering Unsafe Rust make exploits rare – but not impossible.\[3, 4\] To determine the risk posed by Unsafe Rust, we must examine how much actual Rust code uses the \`unsafe\` keyword.

## Unsafe Rust in the Wild

The canonical way to distribute Rust code is through a package called a crate \[5\]. As of May 2024, there are about 145,000 crates; of which, approximately 127,000 contain significant code. Of those 127,000 crates, 24,362 make use of the unsafe keyword, which is 19.11% of all crates. And 34.35% make a direct function call into another crate that uses the \`unsafe\` keyword. \[6\] Nearly 20% of all crates have at least one instance of the \`unsafe\` keyword, a non-trivial number.

Most of these Unsafe Rust uses are calls into existing third-party non-Rust language code or libraries, such as C or C++. In fact, the crate with the most uses of the \`unsafe\` keyword is the Windows crate \[7\], which allows Rust developers to call into various Windows APIs. This does not mean that the code in these Unsafe Rust blocks are inherently exploitable (a majority or all of that code is most likely not), but that special care must be taken while using Unsafe Rust in order to avoid potential vulnerabilities.

At a superficial glance, it might appear that Unsafe Rust undercuts the memory-safety benefits Rust is becoming increasingly celebrated for. In reality, the \`unsafe\` keyword comes with special safeguards and can be a powerful way to work with fewer restrictions when a function requires flexibility, so long as standard precautions are used.

## Safety & Security: a Shared Responsibility

As discussed, Rust lives up to its reputation as an excellent and transformative tool for safe and secure programming, even in an Unsafe context. But this reputation requires resources, collaboration, and constant examination to uphold properly. For example, the Rust Project is continuing to develop tools like Miri \[8\] to allow the checking of unsafe Rust code. The Rust Foundation is committed to this work through its Security Initiative: a program to support and advance the state of security within the Rust Programming language ecosystem and community. \[9\] Under the Security Initiative, the Rust Foundation’s Technology team has developed new tools like Painter, TypoMania \[10\] and Sandpit to detect vulnerabilities within Rust code, giving users insight into vulnerabilities before they can happen and allowing for a quick response if an exploitation occurs.

Safety is a shared responsibility – this concept is fundamental to healthy communities. Between the developers using Unsafe Rust, the groups advocating for the use of security-enhancing tools like Rust, and language stewards like our organization, we all have a part to play in secure programming practices. A collaborative, ongoing focus on safety and security will allow the language to remain as resistant to vulnerabilities as possible well into the future.

\[1\] <a href="https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/\" title="A proactive approach to more secure code" target="_blank" rel="noopener">https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/</a>, <a href="https://cwe.mitre.org/top25/archive/2023/2023_stubborn_weaknesses.html" title="Common Weakness Enumeration (CWE)" target="_blank" rel="noopener">https://cwe.mitre.org/top25/archive/2023/2023_stubborn_weaknesses.html </a>

\[2\] <a href="https://doc.rust-lang.org/book/ch19-01-unsafe-rust.html#unsafe-superpowers" title="Unsafe Rust" target="_blank" rel="noopener">https://doc.rust-lang.org/book/ch19-01-unsafe-rust.html#unsafe-superpowers</a>

\[3\] <a href="https://rustsec.org/advisories/RUSTSEC-2019-0012.html" title="RUSTSEC-2019-0012" target="_blank" rel="noopener">https://rustsec.org/advisories/RUSTSEC-2019-0012.html</a>, <a href="https://nvd.nist.gov/vuln/detail/CVE-2019-15554" title=" CVE-2019-15554 Detail" target="_blank" rel="noopener">https://nvd.nist.gov/vuln/detail/CVE-2019-15554 </a>

\[4\] <a href="https://rustsec.org/advisories/CVE-2018-1000657.html" title="Buffer overflow vulnerability in VecDeque::reserve()" target="_blank" rel="noopener">https://rustsec.org/advisories/CVE-2018-1000657.html</a>

\[5\] <a href="https://crates.io" title="crates.io: Rust Package Manager" target="_blank" rel="noopener">https://crates.io</a>

\[6\] These numbers were derived from a Rust Foundation project called Painter. <a href="https://github.com/rustfoundation/painter" title="The Rust Foundation Project: Painter" target="_blank" rel="noopener">https://github.com/rustfoundation/painter</a>

\[7\] <a href="https://crates.io/crates/windows" title="Rust for Windows" target="_blank" rel="noopener">https://crates.io/crates/windows</a>

\[8\] <a href="https://github.com/rust-lang/miri" title="Miri: Undefined Behavior detection tool for Rust" target="_blank" rel="noopener">https://github.com/rust-lang/miri</a>

&nbsp;

&nbsp;