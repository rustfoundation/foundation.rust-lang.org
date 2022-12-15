---
title: Implementing Borrow Checking in Rust GCC
byline: >-
  Philip Herron, Lead Maintainer of Rust GCC and Arthur Cohen, Maintainer of
  Rust GCC
description: >-
  Guest blog by Philip Herron, Lead Maintainer of Rust GCC and Arthur Cohen,
  Maintainer of Rust GCC
date: 2022-12-16T13:00:00Z
tags:
  - guest blog series
index: false
layout: layouts/news.njk
---
&nbsp;

<img width="580" height="326" alt="Rust Foundation logo at top (Uppercase letter &quot;R&quot; inside a gear icon). Below, a heading reads &quot;Guest Blog Series: Rust GCC  (Supported by Open Source Security, inc and Embecosm)&quot; Underneath, a larger heading reads “Implementing Borrow Checking in Rust GCC”. Beneath this are headshots for the two authors of the post: Philip Herron, Lead Maintainer of Rust GCC and Arthur Cohen, Maintainer of Rust GCC." title="Rust GCC" src="/img/news/2022-12-14-Implementing-Rust-Borrow-Checking-in-Rust-GCC/Rust GCC.png" />

&nbsp;

*Welcome to another installment in the Rust Foundation&nbsp;*<a target="_blank" rel="noopener" href="https://foundation.rust-lang.org/tags/guest%20blog%20series/">guest blog series</a>,*&nbsp;written by members of the Rust Foundation and/or community. Today, we are pleased to have a post from Philip Herron, Lead Maintainer of Rust GCC, and Arthur Cohen, Maintainer of Rust GCC— a community project supported by Rust Foundation Silver Members <a target="_blank" rel="noopener" href="https://opensrcsec.com/">Open Source Security, inc</a> and <a target="_blank" rel="noopener" href="https://www.embecosm.com/">Embecosm</a>. Read on to learn more about implementing borrow checking in Rust GCC*

---

[<u>gccrs</u>](https://github.com/Rust-GCC/gccrs/)&nbsp;is a community project adding the Rust language to the GNU toolchain. The project is currently supported by Rust Foundation Members <a target="_blank" rel="noopener" href="https://opensrcsec.com/">Open Source Security, inc</a> and <a target="_blank" rel="noopener" href="https://www.embecosm.com/">Embecosm</a>. With their help, it has boosted progress from being a part-time side project to one with two full-time resources. In this post, we discuss how gcc can implement and enforce borrow checking to ensure the compiler can prevent memory issues and data corruption.

### What is Rust GCC?

But first, a quick introduction to gcc. [<u>gcc</u>](https://gcc.gnu.org/)&nbsp;stands for “GNU Compiler Collection”. It was originally a C compiler (“GNU C Compiler”), but later became a collection of compilers for various additional languages, such as C++, Fortran, Ada, Go and D. These languages are implemented in the central GCC repository and rely on a common middle-end and back-end for code generation. This forms the basis for a very traditional compilation pipeline, and the tight integration here means there is overlap with other frontends and gives rise to code reuse. We see the potential for Rust to reuse existing work, in the C++ and Ada front ends.

We believe that adding an implementation for GCC will benefit the Rust ecosystem because it can…:

* Help with the formalization effort of the Rust language.

* Encourage wider adoption and deployment of Rust

  * Widespread use of GCC
  * Removing risk of a single implementation
* Benefit many organizations that already have investments in GCC with an upstream Rust frontend.

* This frontend can be backported to older versions of GCC, further extending the reach of Rust.&nbsp;

* Benefit Linux – Linux is built around a GCC toolchain, and having a GCC Rust compiler will facilitate the proposals to allow device drivers written in Rust within Linux.

* Allow us to benefit from the impressive experience of the GCC community, which we can draw from to produce a quality compiler.

### What is borrow-checking?

An integral part of Rust is the borrow checker, which is a static analysis pass preventing memory issues as well as data corruption in user code. Because this blog aims to illustrate how Rust GCC will also enforce borrow checking, I encourage you to read more about that [<u>here</u>](https://doc.rust-lang.org/1.8.0/book/references-and-borrowing.html) (or, if you're interested in a *deep* dive on the borrow-checker, [<u>here</u>](http://smallcultfollowing.com/babysteps/blog/2018/04/27/an-alias-based-formulation-of-the-borrow-checker/)).

In recent years, the official Rust compiler has been splitting itself up into reusable libraries. One of these is the [<u>P</u><u>olonius project</u>](http://github.com/rust-lang/polonius), which implements the borrow checking rules as a standalone project. We propose basing the GCC Rust borrow checker on Polonius. The obvious benefit is that we can reuse the same libraries that the Rust community has already implemented for one of the most complex parts of the compiler.

Another advantage of using Polonius is that it will allow gccrs to contribute back to the Polonius project, improving the cross-pollination of projects.&nbsp;

The challenge with using Polonius (or \`polonius-engine\`, the associated library) is that it is written in Rust. Therefore, it must be compiled using a Rust compiler. In other words, for gccrs to use Polonius as a borrow-checker, gccrs must first compile Polonius (a Rust program,) which relies on the borrow-checker gccrs would provide using Polonius. In the next section, we describe how we will solve the problem of bootstrapping Polonius.

### Bootstrapping Polonius

[<u>Bootstrapping</u>](https://en.wikipedia.org/wiki/Bootstrapping_&#40;compilers&#41;) refers to the process of using an existing, potentially incomplete, implementation of a programming language to compile its compiler. This is what \`rustc\` does, going through multiple stages of compilation using an old, pre-existing binary of rustc, before recompiling itself for the final binary.&nbsp;

Since \`g++\` or \`clang++\` are also written in the language that they implement, they also need to be bootstrapped and compiled by themselves. \`gccrs\` is not specifically a bootstrapping compiler: It is written in C++ but aims to compile Rust (this is similar to \`mrustc\`). However, we'd like to apply certain bootstrapping principles in order to benefit from Polonius so that we enforce the same rules as Rustc.

Our plan is that a first stage compiler, \`gccrs-stage1\`, which will not have a borrow checker since we don’t have a Rust compiler yet, would not link to Polonius. Once we get the working stage1 Rust compiler, we can do an initial compilation of Polonius, shown in this diagram as polonius-stage1.

<img src="/img/news/2022-12-14-Implementing-Rust-Borrow-Checking-in-Rust-GCC/Screen-Shot-2022-12-15-at-11.37.18-AM.png" width="600" height="343" title="Bootstrapping Polonius Diagram" alt="A diagram depicting the bootstrapping of Polonius" />

Now that we have a borrow checker, we can compile gccrs-stage2 and link against Polonius, which will enable the borrow-checking pass. This means the Polonius library will be installed whenever gccrs is installed..

Following the process above, Rust GCC will use a \`rustc\` compatible borrow checker and will enforce the same rules as rustc does.

### Acknowledgments&nbsp;

This project has been made possible by funding from Rust Foundation Silver Member Open Source Security Inc. and Embecosm and with the support of the Google Summer of Code program. It would also not have made so much progress without the support of the community of engineers who have contributed to code development. We would like to thank especially the various members of the GCC community who have been spending time on the project: [<u>Thomas Schwinge</u>](https://github.com/tschwinge), [<u>Marc Poulhi&egrave;s</u>](https://github.com/dkm), [<u>Mark Wielaard</u>](https://gnu.wildebeest.org/blog/mjw/) and [<u>David Faust</u>](https://github.com/dafaust), as well as [<u>Philipp Krones</u>](https://github.com/flip1995) and [<u>bjorn3</u>](https://github.com/bjorn3/) for their expert Rust advice.

If you are interested in contributing to the project or participating in Google Summer of Code alongside us, feel free to ping us on [<u>Zulip</u>](http://gcc-rust.zulipchat.com/)\! We have a large number of good first issues which we can direct you to and mentor you on.

You can find more information about the topics discussed in this blog post via the links below:

* [<u>https://github.com/Rust-GCC/gccrs/</u>](https://github.com/Rust-GCC/gccrs/)
* [<u>https://github.com/rust-lang/polonius</u>](https://github.com/rust-lang/polonius)
* [<u>https://gcc.gnu.org/</u>](https://gcc.gnu.org/)
* [<u>https://gcc.gnu.org/wiki/SummerOfCode</u>](https://gcc.gnu.org/wiki/SummerOfCode)
* [<u>https://doc.rust-lang.org/1.8.0/book/references-and-borrowing.html</u>](https://doc.rust-lang.org/1.8.0/book/references-and-borrowing.html)
* [<u>http://smallcultfollowing.com/babysteps/blog/2018/04/27/an-alias-based-formulation-of-the-borrow-checker/</u>](http://smallcultfollowing.com/babysteps/blog/2018/04/27/an-alias-based-formulation-of-the-borrow-checker/)
* [<u>https://github.com/Rust-GCC/Reporting/blob/main/2021-year-report.org</u>](https://github.com/Rust-GCC/Reporting/blob/main/2021-year-report.org)

---

*Thank you for reading this post in the Rust Foundation&nbsp;[guest blog series](https://foundation.rust-lang.org/tags/guest%20blog%20series/). Stay tuned for more installments in the future\!*