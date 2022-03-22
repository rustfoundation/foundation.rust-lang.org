---
layout: news
series: "Member Spotlight"
title: "Member Spotlight: 1Password"
description: Introducing 1Password, Rust Foundation Silver Member.
date: 2022-03-08
tags:
   - member spotlight
---

![Nathan West](/img/news/2022-03-08-member-spotlight-1password/member_spotlight_nathan_west.png)

It’s time for another installment of our member spotlight blog series, designed to introduce you to our diverse community of silver member companies. Having recently passed our one-year anniversary, we at the Rust Foundation are thrilled at the growth we’ve seen to date in our silver member roster. We’re honored and privileged to have the support of such an interesting and dynamic group, and we look forward to all the great work we can achieve together. Today, we hear from Nathan West, Senior Developer, Client Apps (and Senior Rustacean) at [1Password](https://1password.com/). Read on to learn more. 

## Tell us a bit about 1Password. What do you do and who do you serve?

1Password has been protecting individuals, families, and businesses for the last 15 years. Our password manager keeps their secrets safe, accessible, and easy to use no matter what devices or operating systems they rely on. Besides passwords, we protect payment information, private notes, medical records, business secrets, and over 20 other kinds of data. We’re always working to bridge the gap between security and convenience so anyone can protect their data and take charge of their online safety.

## How is 1Password using Rust?

In 2017, our Windows team started experimenting with Rust and loved it – bugs and crash reports decreased. Eventually, the rest of our team saw the value of Rust, and things took off from there. We’d gone from being unfamiliar with Rust to a prototype of filling within the browser, and it was a turning point for 1Password development. Now, around 63 percent of the 1Password core is using Rust. It powers the latest versions of our client apps and browser extensions. It provides the fundamental logic that underpins everything from encryption to sync, ensuring a consistent, performant experience no matter what combination of operating system and device you’re using. The newest versions of our client applications and browser extensions share a common Rust backend that ensures we provide a consistent look, feel, and experience across any browser and operating system combination. Crucially, 1Password has to be secure, but it also has to be fast. Rust enables the secure management of passwords and other secrets, and allows us to evict them from memory as fast as possible.

## What benefits have you seen from using Rust? What has it helped your company achieve? 

1Password deploys Rust across a wide range of computing contexts:

- **Operating systems**: Android, iOS, Linux, macOS, Windows 
- **Devices**: phones, tablets, watches, desktop PCs, servers
- **Computing architectures**: ARM, x86-64, and WebAssembly

This gives us a unique perspective on the language’s flexibility and productivity benefits.

​​For example, as 1Password was growing, there was a divergence between the different platforms – 1Password 7 for Windows felt different than 1Password for Mac, and so on. Now, Rust empowers our whole team to write code across the entire product stack. We can ship Rust to every platform we want, which means not only do we realize all the technical benefits of Rust, but we can also deliver a much more consistent cross-platform experience than we have in the past. Rust makes this possible and accessible in a way that few languages do. 

Rust puts both a technical and cultural emphasis on the correctness of all things, enabling us to work more confidently in a distributed setting. An extremely strict compiler means that if changes to one platform might affect another adversely, we find out about it quickly, providing us with cross-platform confidence that helps us scale our teams.

## What was 1Password’s motivation to join the Rust Foundation?

As a community-driven project, Rust derives much of its success from the wealth of viewpoints that have informed its development since the beginning. We think this community is critical to the language’s continued success. Joining the Rust Foundation allows us to add our voice to that community and help the project become even more secure, productive, and accessible to developers of all kinds.

## What do you hope the Rust Foundation will accomplish in the months and years ahead?

On a technical level, I’d love to see the Foundation continue to support the work of the language team and third party open source contributors in improving the language’s capabilities, as well as continuing to improve the developer experience in areas like WebAssembly, cryptography, and supply chain integrity.

On a bigger-picture level though, my hope is that the Rust Foundation continues to nurture the inclusive, independent, community-led spirit of the project. Rust isn’t owned by any one organization or leader, and I believe it’s that diversity of input and distributed leadership that’s helped Rust thrive.

## When and how did you personally get involved with Rust itself and how has your involvement evolved?

I first became interested in Rust in 2015 when I heard it was similar to C++, my favorite language at the time. I’d always been a fan of C++ because of the way it provides precise and deterministic control over your resources and how your program could run and behave. Rust shares these ideas, so I was excited to try it.

By the end of 2017, Rust had essentially totally replaced C++ and Python as my favorite language for personal projects. In 2018, I started making standard library contributions and I was gaining confidence in my understanding of how Rust works. I became very active in the Rust community, particularly on Twitter, where I started to discover the many people learning and sharing their experiences with Rust in real time. I would reply to those tweets with encouragement and try to offer help and advice where I could.

Bringing this into the present, I got hired at 1Password largely on the strength of my Rust knowledge, and on my enthusiasm in teaching and advocating for the language. The company needed people who were not just able to write good Rust code, but who could come in and provide strong feedback, teach proper patterns, and cultivate best practice techniques to help the engineering team transition to a Rust-based foundation.

While Rust’s steep learning curve can be unforgiving, it’s exactly that precision and fastidiousness that make it such a good fit for 1Password. Its strictness naturally enforces a meticulous approach to coding that helps us avoid critical errors and vulnerabilities.

As a security company, we couldn’t ask for a more fitting community to align ourselves with as we build the next generation of 1Password.

To learn more about the Rust Foundation, check out our [website](https://foundation.rust-lang.org/), [learn about becoming a member](https://foundation.rust-lang.org/info/become-a-member/) and follow us on [Twitter](https://twitter.com/rust_foundation) and [LinkedIn](https://www.linkedin.com/company/rust-foundation/) to stay up to date.
