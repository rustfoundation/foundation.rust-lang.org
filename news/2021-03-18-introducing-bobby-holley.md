---
layout: news
series: Getting to know the board
title: Introducing Bobby Holley
byline: Bobby Holley, Member Director, Mozilla
description: >-
   Introducing Bobby Holley as the Member Director for Mozilla. Part of the
   "Getting to know the board" series.
date: 2021-03-18T00:00:00Z
tags:
   - getting to know the board series
   - board of directors
---
*Over the next five weeks, we'll be running a series called "Getting to know the board", publishing blog posts from each member of the Rust Foundation [Board of Directors](/board), introducing them to the community. You can view the posts in this series [here](/tags/getting%20to%20know%20the%20board%20series/).*

Hi\! I'm [Bobby Holley](https://bholley.net/about/). I've been a Mozillian since 2008, and currently work in the office of the [Firefox CTO](https://www.mozilla.org/en-US/about/leadership/#eric-rescorla) on technical strategy and coordination. Last month I joined the Rust Foundation’s inaugural [Board of Directors](https://foundation.rust-lang.org/board/), and today I thought I’d share a bit about why I’m here, what I like about Rust, and why I’m excited for its future.

Since the [announcement](http://venge.net/graydon/talks/intro-talk-2.pdf) of Rust in 2010, I've had the privilege of watching it grow from a skunkworks side-project into the force of nature it is today. I wasn't involved much during the early years, but in 2015 I began working with the Servo team to figure out how to bring Rust’s unique capabilities to Firefox. We focused on the CSS engine because it was both performance-critical and extremely complex: in principle we wanted to parallelize it, but in practice couldn’t see a realistic path with C++ concurrency. Rust’s [mutability control](https://blog.rust-lang.org/2015/04/10/Fearless-Concurrency.html) and package ecosystem were [exactly what we needed](https://www.youtube.com/watch?t=220&amp;v=UN_iIExdB9Q), and allowed us to ship [Stylo](https://bholley.net/blog/2017/stylo.html) with better performance, fewer bugs, and in less time than anyone thought possible. Since then I’ve worked on several other Rust-based initiatives in Firefox such as [WebRender](https://hacks.mozilla.org/2017/10/the-whole-web-at-maximum-fps-how-webrender-gets-rid-of-jank/) and [Neqo](https://github.com/mozilla/neqo/), all of which have continued to deepen my appreciation for both the language and the community around it.

In the early (pre-1.0) days, I had the mistaken impression that Rust was just for building browsers at Mozilla. So when I first joined \#rust on IRC, I was surprised to find it teeming with smart and friendly people — often with no other connection to Mozilla — working together to use the language and move it forward. It’s clear to me now that this broad coalition was crucial. [From the start](http://venge.net/graydon/talks/intro-talk-2.pdf#page=6), Rust did not aim to distinguish itself with novel technical ideas, but rather sought to bring together a number of well-understood concepts from the research community into something coherent, learnable, and broadly useful. This is hard work that takes a village, particularly the feedback loop around feature design, wide experimentation, and iteration.

In some sense, the most important insight behind Rust’s success was not about technology but rather about people. Early on the Rust team [made it a priority](https://www.reddit.com/r/rust/comments/6ewjt5/question_about_rusts_odd_code_of_conduct/didrult/) to build a healthy and welcoming community around the project. This attracted talented contributors, helped them collaborate productively, and made it fun to stick around. This resulted in excellent software, which in turn attracted even more talent. This approach seems simple and obvious in retrospect, which is a reaction I frequently have to things that Rust gets right.

Mozilla incubated Rust to build a better Firefox and contribute to a better Internet, but today it's clear that Rust has outgrown its roots. In its new home with the Rust Foundation, Rust will have the room to grow into its own success, while continuing to amplify some of the core values that Mozilla shares with the Rust community:

* **Safety** in a connected world requires securing the browser, but also securing other client software along with the servers that handle people's data. Rust’s memory safety properties eliminate entire classes of exploits, and bringing those guarantees to more programs can protect people from harm.
* **Empowering** people to create things themselves involves building tools that are safe, performant, and approachable. Web technologies like HTML and JavaScript have dramatically lowered the barrier to publishing information and interactive experiences, but some disciplines — like high-performance or embedded development — have traditionally required experts-only languages like C. Rust’s type checking, tooling, and documentation offer a much more accessible path for these use-cases, allowing more people to build more things.
* Foundational technologies should be developed in a truly **open**, **collaborative**, and **inclusive** way. Since its inception, the Rust project has set a very high standard for constructive dialog and positive collaboration, and serves as a model for how to build a healthy community around open-source technology.

Mozilla and the Rust project are well-aligned on these values today, and you can expect us to champion them in our engagement with the Rust Foundation going forward.

Rust exists because of the efforts of countless people working together to make software better, and the Foundation exists to empower and support those people to do their best work. This is an important chapter in Rust's history, and I'm excited to be a part of it.