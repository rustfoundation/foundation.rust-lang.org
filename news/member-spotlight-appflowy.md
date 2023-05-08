---
title: 'Member Spotlight: AppFlowy'
byline:
description: ' Introducing AppFlowy, a Rust Foundation Silver Member organization.'
date: 2023-05-09T12:00:00Z
tags:
  - member spotlight
index: false
layout: layouts/news.njk
---
<img src="/img/news/2023-05-09-appflowy-member-spotlight/appflowy.png" width="580" height="324" alt="Member Spotlight: AppFlowy Featuring Co-Founder &amp; CTO Nathan Foo" title="AppFlowy Member Spotlight Featuring Co-Founder &amp; CTO Nathan Foo" />

Welcome to another installment of the Rust Foundation Member Spotlight series! These blogs aim to introduce our community to various Rust Foundation Member organizations and their leaders. In this installment, we spoke with Nathan Foo, the Co-Founder and CTO of AppFlowy (a Rust Foundation Silver Member Organization) who shared a bit about the company, how they use Rust, and more.&nbsp;

## **Tell us about AppFlowy. What do you do and who do you serve?**

AppFlowy is a privacy-first, open source workspace for your notes, wikis, projects, and more. You are in charge of your data and customizations, with no vendor lock-in. Our mission is to empower everyone to create apps that suit their needs. Built on a community-driven toolbox, including plugins, themes, and more, our platform enables makers to play with and tweak AppFlowy without a limit on what’s possible.

With AppFlowy, you can track the status of different projects by building detailed lists of to-dos in a visually appealing and easy-to-use database. You can also use AppFlowy to visualize tasks in a Kanban Board moving through stages of a project or group them by tags. In addition, you can experience the power of AI right inside a powerful and beautiful rich-text editor. With AppFlowy’s building blocks such as databases, code blocks, and auto-generators, you can communicate efficiently and visually. Unlike with the closed source alternatives, users of AppFlowy own their data – they don't need to give it away to a particular vendor.

A local-first release of AppFlowy is available to beta users at the moment. We are building a mobile app for iOS and Android and cloud-based solutions supporting team collaboration.&nbsp;&nbsp;

## **How is AppFlowy using Rust?**

AppFlowy was built with Rust from the very beginning. We saw Rust as a no-brainer option&nbsp; to create enterprise-grade productivity software because it is a high-integrity language that ensures stability, security, and performance. We have used Rust to build AppFlowy’s backend, which handles all the business logic. The common code base helps us to achieve code reuse, high performance, and memory safety on iOS, Android, macOS, Linux, and Windows. Thanks to Rust, we haven’t run into memory or multithreading issues in production releases. In addition, with the help of the Rust community, the difficulties of building cross-platform programs and ensuring their correctness and stability have been greatly reduced.

These early successes gave us the confidence to try more ambitious things. We are using Rust to build our Web Server and the [<u>AppFlowy-Collab</u>](https://github.com/AppFlowy-IO/AppFlowy-Collab) crate for data collaboration. The frontend application and Web Server use the same crate, ensuring the collaboration algorithm's consistency and accuracy.

You can learn more about how AppFlowy is built with Rust and the technical challenges we tackled by subscribing to [<u>AppFlowy Binary</u>](https://blog-appflowy.ghost.io/), our newsletter for developers and makers.

<img src="/img/news/2023-05-09-appflowy-member-spotlight/appflowy-diagram.png" width="580" height="456" alt="AppFlowy Architecture Rust" title="AppFlowy Architecture" />

*Image Source: AppFlowy*

## **Why did AppFlowy decide to join the Rust Foundation?**

Rust has been fundamental to AppFlowy’s strategy since day one. We use it as a full stack language in both the frontend and backend of AppFlowy and it will continue to be core to our project. As our software solutions evolve with a larger and more diverse user base, we believe Rust will build up AppFlowy’s sustainable advantages, due to its memory safety, code reusability across platforms, and high performance.

As an open source organization, we understand the value of open source software and the community around it. We benefit not only from the Rust project, but from the Rust community as well. AppFlowy makes use of Rust’s many learning resources, supportive Rust peers, and awesome open-source Rust projects that help power AppFlowy such as &nbsp;[<u>tauri-apps</u>](https://github.com/tauri-apps/tauri),&nbsp;[<u>y-crdt</u>](https://github.com/y-crdt/y-crdt),&nbsp;[<u>tokio</u>](https://github.com/tokio-rs/tokio),&nbsp;[<u>diesel-rs</u>](https://github.com/diesel-rs/diesel),&nbsp;[<u>actix-web</u>](https://github.com/actix/actix-web), and&nbsp;[<u>sled</u>](https://github.com/spacejam/sled), to name a few.

We became part of the Rust community by open-sourcing our Rust code and contributing to Rust projects we depend on. We decided to join the Rust Foundation in order to give back to the community that has given us so much and better engage with the wider Rust ecosystem as collaborators, evangelists, and stewards. We are glad that the Rust Foundation is in place to work with stakeholders to sustain and grow this participatory open source ecosystem, through active collaborations, initiatives, and funding. Becoming a member of the Rust Foundation is a natural step for us to make a small contribution to the Rust ecosystem.

## **Nathan, tell us about your personal journey/involvement with Rust.**

I started my career as a software engineer in 2013, focusing on audio and video editing tools. In 2018, at my previous company, I had the chance to develop Rust SDKs for an online collaborative office suite. This started my journey of learning and loving Rust. I learned through writing command line tools. I spent most of my time staring at Rust compiler errors, gradually learning and growing from these mistakes. Over time, I've come to appreciate the true power and strengths of the Rust language.

Rust has a special place in my heart because it has reignited my passion for coding after being overworked and burned out in my day jobs. It helped me regain the joy of programming I used to experience when I just started off my career. As the Rust language and the community continue to grow and thrive, I believe it will become mainstream, and more and more developers will adopt and fall in love with it.

I built AppFlowy from scratch using Rust as a single developer. In addition to growing our founding team with my co-founder Annie Wang, my main role is to oversee the engineering team and contribute as a software architect.

## **Nathan, what is your personal favorite thing about Rust?**

The first thing that comes to my mind is the borrow-checker. It is a unique feature of Rust that enforces strict memory safety and concurrency rules at compile time. Using the borrow-checker leads to high-quality code that is both reliable and performant. I've really enjoyed building AppFlowy on Rust — both projects are proof that open source doesn't mean making tradeoffs when it comes to safety and security.

Also, the Rust toolchain enables us to compile and run code on various operating systems and hardware architectures without requiring extensive modifications. Cargo is one of the tools in the Rust toolchain that I find particularly powerful and easy to use. It automatically manages dependencies and builds artifacts for distribution.&nbsp;

In addition, I find lots of useful tools in&nbsp;[<u>crate.io</u>](http://crate.io) that boost our developing efficiency. For example, Tokio is an asynchronous runtime for Rust that provides a safe and efficient way to write async code. Another tool we use in AppFlowy is Diesel, a powerful, safe, and easy-to-use ORM for Rust that provides a type-safe way to interact with databases.&nbsp;

## **What are AppFlowy’s hopes for the future of Rust?**

AppFlowy believes that the Rust project and the community will continue to grow and thrive with the help of the Rust Foundation. We would like to see continuous improvements in tooling, including IDE support, debugging, and profiling tools, which will streamline the development process and make Rust more accessible to developers. We look forward to seeing greater adoption by developers for all kinds of applications in the future. Additionally, we hope that the Rust Foundation continues to nurture a culture of inclusivity, independence, open source, and sustainability.

---

Thank you to AppFlowy for joining the Rust Foundation as a Silver Member!

You can follow AppFlowy on [<u>GitHub</u>](https://github.com/AppFlowy-IO/AppFlowy), [<u>Discord</u>](https://discord.gg/9Q2xaN37tV), or [<u>Twitter</u>](https://twitter.com/appflowy) for the latest updates.