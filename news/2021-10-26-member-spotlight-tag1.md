---
layout: news
series: "Member Spotlight"
title: Tag1
description: Introducing Tag1, Rust Foundation Silver Member.
date: 2021-10-26
tags:
   - member spotlight
---

<h2>by <a href="https://github.com/tmandry">Tyler Mandry</a>, Quality Director, Rust Foundation </h2>

![Jeremy Andrews](/img/news/2021-10-26-member-spotlight-tag1/member_spotlight_jeremy_andrews.png)

Another week, another new member spotlight! The Rust Foundation continues to grow, and we’re so excited to introduce our new members to the greater Rust community. This blog series has been shining a light on each company, its use of Rust, and its involvement in the Foundation. In this installment I heard from [Jeremy Andrews](https://www.linkedin.com/in/jeremyandrews/), CEO and Founding Partner at [Tag1 Consulting](https://www.tag1consulting.com/). Read on for his thoughts.

### Mandry: Please tell us a little about Tag1. What do you do and who do you serve?

**Andrews**: Tag1 is a global technology consulting firm and the 2nd all-time leading contributor to the Drupal platform that powers 3% of the internet. We specialize in architecting, optimizing, securing and delivering large scale systems. Beyond Drupal, we are experts in real-time collaboration, configuration and infrastructure management, security, performance and we provide full stack web development services.

Our clients include Google, Fortive, Capgemini, The NY Times, Al Jazeera, Whitehouse.gov, the ACLU, the Linux Foundation, Stanford University, The University of Michigan and many other great organizations.

### Mandry: Tell us about Tag1’s use of Rust. What are you working on currently and do you have any plans you’d like to share?

**Andrews**: We started using Rust to improve internal tools and processes. We ported a number of scripts and utilities that were originally written in Python and were increasingly impressed by the dramatic gains in performance and reliability. We spend much less time debugging problems with the Rust versions of these internal tools, and we can rapidly deploy updates when remote APIs change or we need new functionality.

Our primary contribution to the community is [Goose](https://goose.rs/), a highly-scalable load testing tool inspired by Locust. Many of our clients operate at an extremely large scale, and reliably load testing at these scales with a Python-based tool created its own challenges. By creating Goose, thanks to its Rust underpinnings, we have solved these headaches and can easily operate at the scale we require. It has continued to mature and gain additional features, described in [The Goose Book](https://book.goose.rs/).

We are seeing growing interest from the community with requests for new functionality and added flexibility. We will introduce a graphical user interface for Goose soon, making it easier to run load tests and analyze the results. We're continuing to expand the [Goose Eggs library](https://docs.rs/goose-eggs/), which has already proven to be helpful in quickly developing powerful load tests. Finally, the more we use Rust the more we continue to improve the underlying load testing codebase, embracing best practices and new features available in the rapidly evolving language.

### Mandry: What was Tag1’s motivation to join the Rust Foundation? 

**Andrews**: We first explored this question [in our blog where we announced our membership in the Rust Foundation](https://www.tag1consulting.com/blog/tag1-joins-rust-foundation-first-silver-member). We remain strong believers in Open Source Software. As long-time contributors to Drupal and the Drupal Association, we've seen how effective stewardship can greatly benefit a community. Joining the Rust Foundation echoes our excitement for Rust itself, we want to see it and the community around it grow and thrive. Rust is already known for its excellent documentation and its passionate and helpful community. We are very proud to be even a small part of this.

### Mandry: What do you hope the Rust Foundation will accomplish in the future? 

**Andrews**: The Rust Foundation will be critical to the success and growth of the project and community. We hope that the Rust Foundation will encourage users to continue creating new things with the language, promote new features and uses and advocate for the community. The Foundation will be essential to fundraising, supporting and scaling the project. It will also help organize conferences and bring the community together, as well as help build a robust ecosystem around the project. 

### Mandry: What is your personal involvement with Rust? Do you consider yourself a Rustacean? Please tell us a bit about your involvement with the language.

**Andrews**: My first six months of learning Rust was an odd combination of overwhelming frustration mixed with just enough moments of happiness to keep me using it. At times, it felt like the compiler was constantly fighting me, forcing me to change decades of learned habits. At the same time, there was profound satisfaction each time I managed to get my code to compile and run.
 
At some point I stopped fighting the compiler and fully embraced the patterns it was teaching me. I also enabled Clippy on all my projects, open source and internal, and look forward to new versions introducing new improvements.
 
Now when I need to program in other languages, I find I miss the strictness of the Rust compiler! I often adapt Rust patterns into tools I maintain in other languages. And whenever possible, I use Rust.
 
I have not made the time yet to contribute to the compiler or the standard Rust toolchain, but this is still something on my programming bucket list.

To learn more about the Rust Foundation, check out our [website](https://foundation.rust-lang.org), [introductory video](https://www.youtube.com/watch?v=AI4lPN0BqGc) and [recent blog posts](https://foundation.rust-lang.org/posts/), and follow us on [Twitter](https://twitter.com/rust_foundation) and [LinkedIn](https://www.linkedin.com/company/rust-foundation/) to stay up to date.  
