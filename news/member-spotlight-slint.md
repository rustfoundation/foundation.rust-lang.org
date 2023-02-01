---
title: 'Member Spotlight: Slint'
byline:
description: |
  Introducing Slint, a Rust Foundation Silver Member.
date: 2023-02-03T12:30:00Z
tags:
  - member spotlight
index: false
layout: layouts/news.njk
---
<img src="/img/news/2023-02-03-slint-member-spotlight/olivier-goffart.png" width="580" height="326" alt="Slint Silver Member Spotlight" title="Heading: Silver Member Spotlight featuring Slint. A headshot of Slint Co-Founder Olivier Goffart is underneath the heading in a zig-zag, circular frame." />

Welcome to another Rust Foundation Member Spotlight blog! This series aims to introduce our community to various Rust Foundation Member organizations and their leaders. In this installment, we spoke with Olivier Goffart, Co-Founder of Rust Foundation Silver Member Organization, Slint who shared a bit about the company, how they are using Rust, and more.&nbsp;

### Tell us about Slint. What do you do and who do you serve?

[<u>Slint</u>](https://slint-ui.com/) is a toolkit to efficiently develop graphical user interfaces and human-machine interfaces for any display. With Slint, users can develop interfaces from desktops to embedded (scalable), for devices where available processing power and memory are very limited (lightweight), and for applications that should look like other native applications. Slint’s architecture creates a clear separation between interface definition and business logic. This allows it to be easily combined with other programming languages. Currently, Slint supports Rust, C++, and JavaScript.

As an open source project, our goal is to build a healthy community around Slint, where users can share ideas, experiences, and information, and where we can welcome contributions. There are a number of community-built, Slint-based applications on both desktop and embedded systems. Our commercial customers are primarily from industries where safety critical systems are relevant (industrial, medical, automotive, etc).

### How is Slint using Rust?

In [<u>Slint</u>](https://github.com/slint-ui/slint/), the interface is defined in a User Interface Description Language that provides a way to describe graphical elements, their placement, and the flow of data through the different states. The interface is compiled ahead of time using a compiler, which uses the typical compiler phases of lexing, parsing, optimization, and finally code generation. Depending upon the target language (Rust, C++, or JavaScript), the compiler uses different engines for code generation. The runtime library connects the compiled interface and the different rendering backgrounds and styles, which are configurable at compile time.&nbsp;

The compiler, the compiled interface, the runtime library, and the language server are all implemented in Rust.

### Why did Slint decide to join the Rust Foundation?

As an organization, Slint has a strong understanding of the value of open source software – and the communities around them. It's important for us to be part of the wider Rust ecosystem by providing our own crates and contributing to crates that we depend on. Joining the Rust Foundation as a Silver Member was a natural step along this path for us – we ultimately decided to become members to better engage with the community as part of the Rust Foundation.

Additionally, we believe that this is a good time to start engaging with Rust at the industry level, especially with companies that place a lot of value where memory safety when qualifying software. It’s time to start discussions about how these sorts of organizations and industries can adopt Rust in their new projects but also how they could leverage Rust in existing or legacy software as part of any code refactoring effort. We believe that the Rust Foundation can be a driver of these conversations and movements.&nbsp;

### How is Slint thinking about the future of Rust?

The future of Rust is looking very bright. Rust is proving to be beneficial for Android, it’s becoming an officially supported language in the Linux kernel, and Google has announced that Chrome will start using Rust. Automotive players such as AutoSAR and Blackberry QNX have announced that they will also start using Rust. We hope that the Rust Foundation continues to grow and that there are more industry-focused activities as it provides a stronger motivation for developers to learn Rust and use it in their daily work.

### What is your personal favorite thing about Rust?

Cargo in combination with crates.io. It’s ridiculously easy to find, use, and share Rust-based software. The best thing is that it works like a charm every time and makes life so much easier.

---

*Thank you to Slint for their Rust Foundation Silver-level membership!*

*You can learn more about Slint via their <a target="_blank" rel="noopener" href="https://slint-ui.com/">website</a>&nbsp;and connect with them on <a target="_blank" rel="noopener" href="https://github.com/slint-ui/slint/discussions">GitHub</a>, <a target="_blank" rel="noopener" href="https://twitter.com/slint_ui">Twitter</a>, <a target="_blank" rel="noopener" href="https://fosstodon.org/@slint">Fosstodon</a>, and <a target="_blank" rel="noopener" href="https://www.linkedin.com/company/slint-ui/">LinkedIn</a>.*