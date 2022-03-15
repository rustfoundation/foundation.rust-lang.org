---
layout: post
series: "Member Spotlight"
title: Knoldus
byline: Shane Miller, Rust Foundation Chairwoman and Member Director (AWS)
description: Introducing Knoldus, Rust Foundation Silver Member.
tags:
   - member spotlight
---

![Bhavya Aggarwal](/img/posts/2021-10-07-member-spotlight-knoldus/member_spotlight_bhavya_aggarwal.png)

The Rust Foundation is growing fast! And as we expand our membership base, we are also expanding our member spotlight series. Designed to help our audience get better acquainted with member companies, this series dives into the details of each member, its use of Rust, its interest in the Foundation, and what they hope we’ll accomplish going forward. [I](https://twitter.com/SkippersWif) recently shared some questions with [Bhavya Aggarwal](https://www.linkedin.com/in/bhavya-aggarwal-680929a/), CTO at [Knoldus, Inc.](https://www.knoldus.com/home) Check out his thoughts below. 

### [Miller](https://twitter.com/SkippersWif): Tell us a bit about Knoldus. What do you do and who do you serve?

**Aggarwal**: [Knoldus](https://www.knoldus.com/home) engineers high-performance systems, data strategy and analytics and intelligence-driven systems with a product mindset to make businesses succeed with technology. We modernize enterprises through cutting-edge digital engineering by leveraging functional programming and a fast data ecosystem. Our mission is to provide cloud-native, reactive and streaming fast data solutions that are message-driven, elastic, resilient and responsive. With a team of 350+ seasoned experts, we help enterprise clients - including many Fortune 500 companies - create the next-generation capabilities that set them apart and create new opportunities. To learn more about Knoldus, please visit: www.knoldus.com or follow Knoldus on Twitter at @knolspeak.

### Miller: How is Knoldus using Rust?

**Aggarwal**: [Knoldus has embraced Rust since 2019](https://www.knoldus.com/accelerators/technology/rust) and implemented it in all aspects of development, from source control to compilers. One of the main reasons for our interest in Rust was to build highly performant systems because of its better safety standards that decrease the development process cost. Rust has been making its mark in multiple areas like Embedded programming, Networking, CLI, Web Assemblies and Blockchains. Knoldus has been successfully contributing to these areas and some of the achievements are discussed in detail below.

- Kerb - Kerb is a consumer location intelligence platform designed to measure the flow of consumers. The platform uses an AI-powered camera that maps and measures the pedestrian foot traffic flow on sidewalks to calculate total potential customers, customers captured, potential leads, intent to buy metrics for each potential lead and demographics of each potential lead, enabling businesses to measure footfall insights. The Jetson Nano devices were used for edge computing and all the services to capture the relevant data like Stereo Images, GPS, Accelerometer, etc. were built on Rust.   

- Polkadex - Polkadex is a dedicated blockchain for decentralized exchange, which is purpose-built and configured to optimize the performance of DEXs. Polkadex solves the problem of low liquidity by having AMMs directly connected to its trading engine. These AMMs act as On-Chain market-making bots. Polkadex provides two ways to bring liquidity, Polkadot Parachain, and Snowfork trustless Ethereum Bridge. Polkadex para chain will have just one functionality to bridge liquidity to and from Polkadot to Polkadex. The platform is made using the Substrate Blockchain Framework.

- Embedded Engineering - Knoldus has developed two major products: 

  - Image Recognition System for Attendance Management and Security.
  - Conference Monitor - An IoT-based system for monitoring the conferences. 

Currently, we are working on building the edge computing solutions for our own IoT Platform called Knurons and have been able to supply various sensor data using devices like Jetson Nano, Raspberry PI as well as devices having STM32F3Discovery Microcontroller.

- Networking - Knoldus have built an internal product for monitoring activities of network protocols like DHCP (Domain Host Configuration Protocol) & AD (Active Directories). The product has the ability to monitor any type of logs and is completely configurable.

- CLI - To test the powers of Rust Programming, we have developed a tool that monitors the system’s processes and terminates them when they go beyond their configured memory consumption limit.

- Web Assembly – We have developed some POCs to understand the concepts more thoroughly. POCs include hosting wasm modules in JS, building checkers games, hosting wasm modules on RaspberryPi and much more.

- Rust Compiler – Knoldus has also been contributing to the Rust compiler (rustc) to make it more reliable. 

### Miller: How do you expect that to change?

**Aggarwal**: Previously we were involved on the application level only where we developed a few products, but now we are more focused on the system-level programming. Since Rust programming overcomes the pitfalls of C & C++ and the most powerful feature is it guarantees memory safety, which is the pain point for C & C++ where we need to handle all the memory by ourselves, we decided to make use of these features and build highly performant and intelligent systems. We are working on the development of embedded software for the IoT platforms and also trying to use the core capabilities of Rust programming in the Networking, Web Assemblies and CLI area.

### Miller: What was Knoldus’s motivation to join the Rust Foundation?

**Aggarwal**: At Knoldus, we always try to incorporate cutting-edge technologies into our tech stack. We have been functional programmers for the last 10 years and are primarily invested in Scala and Haskell. For many of our engineers, Rust was a language that we evaluated and loved. Since the advent of Rust, it has been on a path to growth, and like the Rust Foundation, which  supports Rust programming, Knoldus also has the same vision to always contribute to the community. The prime motivation behind Knoldus joining the Foundation is that we both believe Rust is the future of Systems Programming and together we can support the Rust project in its work to move Rust forward.

### Miller: What do you hope the Rust Foundation will accomplish in the months and years ahead?

**Aggarwal**: The Rust Foundation has been playing a pivotal role in promoting Rust programming across the globe. We anticipate the Rust Foundation will provide a centralized platform to the Rust community to make the Rust ecosystem more mature and contribute towards the growth of the Rust programming language. This centralized platform is already supervised by competent maintainers. The coming together of industry giants behind Rust Foundation lays the groundwork for successful adoption and appeal for the language.

### Miller: When and how did you personally get involved with Rust itself and how has your involvement evolved?

**Aggarwal**: We started exploring Rust programming in 2019 to leverage its powers over C & C++  in areas like no memory management issues. Where Rust catches any misuse of memory at the compile-time only, it also provides high performance, which is because of the absence of a garbage collector and so many other features, like cross-platform support, rich ecosystem, etc. 

Initially, we started small with Rust by understanding the language and developing capabilities around its ecosystem, and then we built some in-house solutions like Attendance Management and Network scanning tools for our internal use. Fortunately, we got a chance to work on full-scale Rust development projects, which helped us to delve more into Rust and its ecosystem. The current focus is clearly in the Embedded space as we are working on efficient capture of data and utilizing that data to make better decisions and drive the business value for our end customers.


To learn more about the Rust Foundation, check out our [website](https://foundation.rust-lang.org), [introductory video](https://www.youtube.com/watch?v=AI4lPN0BqGc) and [recent blog posts](https://foundation.rust-lang.org/posts/), and follow us on [Twitter](https://twitter.com/rust_foundation) and [LinkedIn](https://www.linkedin.com/company/rust-foundation/) to stay up to date.  
