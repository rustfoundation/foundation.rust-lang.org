---
layout: news
series: "Getting to know the board"
title: Introducing Mark Rousskov
byline: Mark Rousskov, Project Director, Core
description: Introducing Mark Rousskov as a Project Director for Core. Part of the "Getting to know the board" series.
tags:
   - getting to know the board series
---

_Over the next five weeks, we'll be running a series called "Getting to know the board", publishing blog posts from each member of the Rust Foundation [Board of Directors](/board), introducing them to the community. You can view the posts in this series [here](/tags/getting%20to%20know%20the%20board%20series/)._

Hey, I’m Mark Rousskov (often going by simulacrum online), and I’m excited to serve as one of the project directors representing the Core team! I’ve been around in the Rust project since 2016, and currently lead the release team, and am a member of the core, infrastructure, and compiler contributors teams.

What excites me about Rust is our strong commitment to solving problems through working together, both with people already around us today, but also always looking to include more people to learn from their experiences. I believe this emphasis on connections is the core reason for Rust's success.

One example where this collaboration with other communities has had a memorable experience for me was during work on enabling fine-grained parallelism in the Rust compiler. The way that rustc and cargo manage parallelism today is via the [make jobserver](http://make.mad-scientist.net/papers/jobserver-implementation/) protocol. The current stable compiler isn't parallelized beyond the tail end - code generation - and increasing opportunities for parallelism stressed the jobserver. This led to a performance problem, where all readers on a pipe (used within the jobserver as a semaphore) were being woken when a single byte is written in. This led to a thundering herd of threads attempting to read from the pipe (all but one of which would fail). Normally, the next step would likely be to start trying to identify whether this was a known bug and working to report or fix it. However, we happened to have someone already active in the Linux kernel community - Josh Triplett - around helping us benchmark the results, and he informed us that this bug was already being fixed upstream. He also helped us understand the delay before most of our users could expect to see the change in the kernel on their systems. Growing and establishing these connections enhances everyone’s experience, and I look forward to finding opportunities to foster this growth.

One of the reasons I'm so excited for the Foundation is it will help us define Rust's values and goals not just around software or programming language design, but around what I believe to be a more fundamental exploration: developing a model for sustainable, effective open collaboration on a global scale, bridging numerous communities. We already go far beyond ‘just’ a programming language in the project’s scope; I’m excited to see where our exploration goes, and what we can achieve together.
