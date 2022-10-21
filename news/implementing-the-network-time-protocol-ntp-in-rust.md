---
title: Implementing the Network Time Protocol (NTP) in Rust
byline: Folkert de Vries
description: 'Guest Blog Series: Folkert de Vries'
date: 2022-10-21T16:30:00Z
tags:
  - guest blog series
index: false
layout: layouts/news.njk
---
&nbsp;

&nbsp;

<img src="/img/news/2022-10-21-implementing-a-ntp-in-rust/folkert-de-vries.png" width="2560" height="1440" />

*Welcome to another installment in the Rust Foundation&nbsp;*[guest blog series](https://foundation.rust-lang.org/tags/guest%20blog%20series/),*&nbsp;written by members of the Rust Foundation and/or community. Today, we are pleased to have a post from Folkert de Vries, Embedded Software Engineer at Tweede golf. Read on to learn about how Folkert's team implemented a Network Time Protocol (NTP) client and server in Rust.*

---

For the last few months, we at&nbsp;[Tweede golf](https://tweedegolf.nl/)&nbsp;have been working on implementing a&nbsp;[Network Time Protocol (NTP) client and server in Rust](https://github.com/memorysafety/ntpd-rs).

The project is a&nbsp;[Prossimo](https://www.memorysafety.org/)&nbsp;initiative and is supported by their sponsors, Cisco and AWS. Our first short-term goal is to deploy our implementation at&nbsp;[Let’s Encrypt](https://letsencrypt.org/), the free, automated, and open certificate authority. The long-term goal is to develop an alternative fully-featured NTP implementation that can be widely used.

In this blog post we’ll talk about the process of implementing a new open-source version of the protocol in Rust, why an alternative NTP implementation is important, and our experiences along the way.

Our project is called ntpd-rs. More information and the initial release of the client can be found&nbsp;[here](https://github.com/memorysafety/ntpd-rs).

## What is NTP?

The network time protocol synchronizes time between devices connected to a network. Accurate time is essential when your device communicates with other devices, mostly to make sure events are ordered correctly. The device you are reading this article on is probably running an NTP process that regularly synchronizes itself with the real time.

NTP is one of the oldest Internet protocols, and although it is less known than HTTP or DNS for example, the Internet and its billions of devices depend on it every day.

The clocks in our devices are reasonably accurate, but can drift meaningfully in the space of hours. The real time is kept with atomic clocks. Many technology companies and foundations provide NTP servers that make this time available to the internet.

<img src="/Blog-2022-10-11-relationship-various-levels-ntp.png" width="1116" height="1056" alt="A diagram showing the relationships between the various levels of NTP servers. The blue numbers are the stratum numbers; yellow arrows show a direct connection, such as RS-232, while red arrows show a network connection." title="Relationships between the various levels of NTP servers." />

*Image source: [Wikipedia Commons](https://commons.wikimedia.org/wiki/File:Network_Time_Protocol_servers_and_clients.svg)*

But if you ask such a server what time it is, then by the time its response reaches you, that time is out of date. You need to somehow correct for the transmission delay.

The NTP client performs this correction and maintains connections with multiple NTP servers for increased reliability.

## Goals

NTP is part of the foundation of the Internet, and must be absolutely secure and reliable. For example, precise time is used to check TLS certificates– it would be a disaster if an attacker could adjust the system time such that an outdated certificate is seen as valid\!

The primary goal for this project is to provide an alternative implementation of NTP, that is just that: secure and reliable.

## About Prossimo and the relevance of our project

Our NTP project fits seamlessly into Prossimo’s objectives.&nbsp;[Memory safety](https://www.memorysafety.org/docs/memory-safety/)&nbsp;is a requirement to achieve a secure implementation of any critical software. Prossimo’s mission states:

> Memory safety for the Internet’s most critical infrastructure

Simply put: we should provide memory-safe implementations for pieces of software that run the Internet wherever we can. This has materialized in work being done on TLS (Rustls), curl, the Linux kernel, and this project.

### Security of open source software

Prossimo’s mission has recently attracted more attention since the Linux Foundation project OpenSSF published&nbsp;[The Plan](https://openssf.org/oss-security-mobilization-plan/)&nbsp;and selected&nbsp;*Memory Safety*&nbsp;as one of ten points of action to improve security of open source software. The plan is backed by open source foundations including&nbsp;**the Rust Foundation**, the technology industry, as well as the White House. The execution of the memory safety work in The Plan consists in large part of Prossimo projects.

We will not dive into all the pros and cons of re-implementations in memory-safe languages here, but we do hope to show that these types of efforts do not need to be lengthy and painful. You can deliver solid results far more quickly than you might think, if you use a programming language like Rust, with its strong ecosystem and tools.

### Rust

Using Rust for our implementation means that the client we build is memory safe. We don’t do many allocations, but we can be confident that we’ll have no segfaults, buffer overflows or memory leaks ever. The same is true for anyone building on top of our implementation.

Another benefit of Rust is that we can use its standard library and package ecosystem, so our NTP implementation is much smaller (hence easier to validate) than the alternatives. This small size also makes it easier to play around with extensions to the NTP specification (e.g. in the development of the next version of NTP, NTPv5).

A nice side-effect of our effort is that more people are now familiar with how NTP works, and hopefully our implementation is more accessible. As we noted above, accurate time is crucial for a lot of modern internet infrastructure.

## Our experiences

### The protocol

We initially struggled with turning the NTP specification text into code. What seems reasonable at a distance becomes painfully imprecise when you actually implement it. Still, after some deliberation, we were ready to get to work.

The core of our implementation is a collection of data structures and algorithms that implement the logic of NTP. This part does not do any network calls or clock modification, it just describes as data what calls and modifications are needed.

Modeling this core,&nbsp;`ntp-proto`&nbsp;as pure functions makes it easily testable, and means we have no unsafe code in this part of the code base.

Our implementation is not a port of the logic of existing implementations ntpd or chrony. In fact, we barely looked at their implementation at all, because we found it hard to map their source code to the NTP specification. Our implementation is based solely on the specification.

### The network

Our networking requirements go beyond what the Rust standard library provides. NTP uses UDP to send packets, which is well-supported, but we want more.

The NTP algorithm uses send and receive timestamps, which means we have to know the time right before a packet was sent, and right after it was received.

We could create these timestamps in our program with&nbsp;`Instant::now`, but that time would include the time spent between the socket receiving the message, and our program actually resuming to process the message.

Unix sockets provide more accurate send and receive timestamps. But to get them, we must configure the socket with functions from&nbsp;`libc`, which is unsafe and wildly under documented. After lots of digging, we figured out the mechanism,&nbsp;[made a tiny contribution to libc](https://github.com/rust-lang/libc/pull/2881), and implemented a safe&nbsp;`async`&nbsp;version of kernel software timestamping.

### The clock

Manipulating the system clock is not exposed by the standard library, so here too we must drop down to&nbsp;`libc`. Luckily we had some experience with manipulating the clock on Linux from our&nbsp;[Precision Time Protocol project](https://tweedegolf.nl/en/blog/72/announcing-statime-a-rust-ptp-implementation).

### The system

The above components are combined in what NTP calls the “system”: it orchestrates how the NTP daemon interacts with the outside world and the system clock.

The system relies on Rust’s&nbsp;`async`&nbsp;support and the&nbsp;[tokio](https://tokio.rs/)&nbsp;async runtime. We use&nbsp;`clap`&nbsp;to define our command-line interfaces.

The existing C solutions need to build concurrency, argument parsing and other basic functionality from scratch. Having no dependencies brings distribution advantages, but has serious downsides in terms of lines of code and maintainability. Verifying memory safety and other security properties in such a big code base is hard.

In Rust, checking properties of the system is much easier: memory safety is guaranteed by the compiler, and the standard library and many of the popular libraries have undergone serious security scrutiny. Our code, and by extension the work involved in security reviews, is comparatively small.

## Conclusion

Once we had a handle on NTP’s core ideas, development went smoothly. Setting up all the other parts, networking, clock adjustment and the asynchronous tasks, was a joy.

> **Our smooth experience strengthens us in the conviction that Rust is the correct choice for projects of this type: all of the protocol logic is completely safe, and only when we interact directly with the OS do we need to reason about unsafe code. We start the subsequent phases of the project with confidence.**

Our code is available&nbsp;[on Github](https://github.com/memorysafety/ntpd-rs).

---

*Thank you for reading this post in the Rust Foundation&nbsp;[guest blog series](https://foundation.rust-lang.org/tags/guest%20blog%20series/). Stay tuned for more installments in the future\!*