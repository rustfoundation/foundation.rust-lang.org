---
layout: news
series: "Getting to know the board"
title: Introducing Josh Stone
byline: Josh Stone, Project Director, Reliability
description: Introducing Josh Stone as the Project Director for Reliability. Part of the "Getting to know the board" series.
date: 2021-04-22
tags:
   - getting to know the board series
---

_Over the next five weeks, we'll be running a series called "Getting to know the board", publishing blog posts from each member of the Rust Foundation [Board of Directors](/board), introducing them to the community. You can view the posts in this series [here](/tags/getting%20to%20know%20the%20board%20series/)._

My name is Josh Stone, and I’m serving on the Rust Foundation board as a Project Director in the area of reliability. When I’m not thinking in Rust, you might find me riding my bike, playing video games with my kids, or learning the next skill in my pandemic-initiated woodworking. But for now I’d like to share just a little bit about how I got started with Rust.

My favorite way to tinker with a new programming language has been to solve [Project Euler](https://projecteuler.net/) problems. My day job was all in C and C++, but I would tinker with other languages when I could, and for a while my main preference was Python. In line with the site’s policy, I won’t share all my solutions. However, the [first problem](https://projecteuler.net/problem=1) has been spoiled many times, asking you to “Find the sum of all the multiples of 3 or 5 below 1000”, so here’s what I had in Python:


```
def solve(U=1000):
    def sum_multiples(n):
        m = (U - 1) // n
        return n * m * (m + 1) // 2
    return sum_multiples(3) + sum_multiples(5) - sum_multiples(15)
```


Rust had been on my radar for a while, but I was only reading about it here and there. In April 2014, I finally gave it a real try, and my very first Rust program was just a translation of that problem 1 solution:


```
fn solve(u: uint) -> uint {
    let sum_multiples = |n| {
        let m = (u - 1) / n;
        n * m * (m + 1) / 2
    };
    sum_multiples(3) + sum_multiples(5) - sum_multiples(15)
}
```


I barely needed to change anything at all, but it gave me a fully compiled and optimized program, which was very exciting to me. In fact, if this is called with constant input, it will even get inlined and optimized down to the final answer, statically. This code still works with modern Rust too, if we fix the pre-1.0 `uint` -- just change that to `usize` or perhaps `u32`.

That little example doesn’t really even scratch the surface of the power of Rust though. The easy closure is nice, but you could write that with a C++11 lambda too, or even a GCC nested function in C if you’re a little sadistic. This was just a tiny learning exercise, and the exciting promise it carried was that my Rust code would be **safe**, statically and continuously checked by the compiler.

Memory safety and thread safety, without sacrificing performance and productivity, what a dream! I’m not exactly sure what pushed me over the edge to try it at that time, but I had certainly seen a fair share of nasty bugs in both userspace and the kernel while working on [SystemTap](http://sourceware.org/systemtap/). (Coincidentally, Graydon Hoare also worked on that project, but before my time.) Not all of those bugs I experienced would be caught if written in Rust, but certainly some would. It really does feel like rustc is a big step toward the mythical [Sufficiently Smart Compiler](http://wiki.c2.com/?SufficientlySmartCompiler), letting you write nice code without worrying about a suite of low-level gotchas.

So I went on porting more of my code to Rust, and when the num crates were pulled out of std before Rust 1.0, I was happy to volunteer as a maintainer, being directly useful to my Project Euler tinkering. As I started applying parallelism to some of those harder problems, I got involved in Rayon, and so on I’ve been happy to contribute to other crates as well. Then 4 years ago I changed teams at Red Hat to start maintaining the Rust toolchain for Fedora and RHEL full time, making Rust _officially_ “what I work on.” Now with the Foundation, I’m excited to be in a position to enable more people to share in that work!

Within the Rust project, I’m currently a member of the release team, the security response working group, and compiler team contributors with a focus on the LLVM working group. I hope these roles have prepared me well to serve as Project Director for reliability. We always want Rust to “just work”, so you’re free to update to the latest release without fear of regressions. Our track record is good, but of course not perfect, and I’ll be looking for ways to track and improve this. Services like crates.io and docs.rs are important too, not just in general uptime but also broad accessibility. I have less experience in this kind of infrastructure, but I am definitely open to suggestions. Let me know how the Rust Foundation can make Rust more reliable for you!
