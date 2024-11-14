---
title: >-
  Rust Foundation Collaborates With AWS Initiative to Verify Rust Standard
  Libraries
byline: Rust Foundation Team
description: >-
  The Rust Foundation is excited to support a new contest from AWS that
  endeavors to crowd-source the verification of the Rust standard libraries.
date: 2024-11-14T15:00:00Z
tags:
  - foundation
index: false
layout: layouts/news.njk
---
Today, Amazon Web Services (AWS) \[announced\](link) a collaborative initiative aimed at verifying the safety of the Rust standard libraries. The Rust Foundation has reviewed the plans behind this effort and is excited to serve as host!

Although the Rust Programming language is designed to be both safe and efficient, unsafe operations that can compromise these guarantees are possible. Currently, the Rust standard library contains approximately 35,000 functions, including 7,500 marked as unsafe, necessitating a focused effort to ensure their reliability and security.

This initiative will include a series of challenges that focus on verifying memory safety and a subset of undefined behaviors in the Rust standard library. Participants can contribute by specifying contracts, verifying library components, or developing new verification tools. AWS’ goal is to contribute to an ecosystem where verification becomes an integral part of the Rust language's continuous integration process.

Other key notes:

* Participants can contribute by specifying contracts, verifying library components, or developing new verification tools.
* The challenge specifies success criteria that must be met for the solution to be reviewed and merged into the forked repository CI pipeline.
* The effort is tool agnostic
* The repository provides templates for introducing new challenges, new tools, and instructions on how to submit solutions to challenges.
* At this time, AWS has over 20 students, academics, and researchers involved.

### The Rust Foundation’s Role

Although AWS is a Platinum Member of the Rust Foundation, we have opted to host the challenge purely out of our shared belief in the safety and reliability of Rust libraries and our desire to have as much insight as possible into important efforts like this.

The challenge rewards committee is responsible for reviewing activity and dispensing rewards.

### Get Involved!

AWS invites you to participate by solving challenges, introducing *new* challenges or tools, and/or helping review and refine the current processes.

Challenge announcement from AWS: \{link\}

Associated GitHub Repository: [https://github.com/model-checking/verify-rust-std](https://github.com/model-checking/verify-rust-std)

&nbsp;