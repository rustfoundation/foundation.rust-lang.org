---
title: 'Making a Career Move with Rust: A Developer’s Approach'
byline:
description: 'Guest Blog Series: Dotan Nahum'
date: 2022-06-21T17:00:00Z
tags:
  - guest blog series
index: true
layout: layouts/news.njk
---

![Dotan Nahum](/img/news/2022-06-21-guest-blog-series/dotan-nahum.png "Dotan Nahum - Founder and CEO, Spectral")

You can have a career in Rust. That said, the most important thing to know is that Rust is still a relatively young programming language. For example, if you come across Rust job openings that require 10 years experience, or even 5 years "production" experience, it might be that these posts were written by "converting" some Java or C++ roles to their Rust counterparts.

It's *possible* that companies just don't know how to hire Rust developers.

> Remember, just as candidates sometimes don't pass interviews, companies aren’t always equipped to *conduct* a strong interview. For example, some companies may not have enough of a technical foundation to give you a proper Rust interview, and a smart thing to do as a candidate is to ask the employer how employees are learning to become experts at the language.

Another thing to remember is that other than the usual backend, infrastructure, and systems programming areas Rust is widely known for, it has also been dominant in the cryptocurrency world. There are many crypto oriented [open source projects](https://github.com/rust-in-blockchain/awesome-blockchain-rust) to learn from, which is fantastic. Not by chance, the number of open Rust jobs in crypto currently outnumber those in other fields.

And lastly, when a programming language is relatively new and is not dominating a market, there will naturally be less focus on the language itself during the interview. Instead there will be a focus on pure programming experience, software design, and common sense, which I think is a good thing. This means candidates' overall engineering skills can be the main focus of the interview, versus their ability to memorize some esoteric programming language feature.

## **You may not have to look for a new job**

Sometimes not switching jobs is the smartest thing to do if you can promote Rust in your current company. You can do this by convincing decision makers to understand the value of Rust. Then you can propose Rust be used for a new project or to replace parts of your existing codebase. In these cases, the areas where introducing Rust will have the most impact and be the most efficient investment include:

* Performance critical bits, which you'll want to replace but still tie those to your existing Node.js, Go, Ruby, Python or other codebases. You can do that with [Neon](https://neon-bindings.com/) (Node.js), [ffi](https://spectralops.io/blog/rust-vs-go-why-not-use-both/) (Go), [Rutie](https://github.com/danielpclark/rutie#using-rust-in-ruby) (Ruby, [Helix](https://github.com/tildeio/helix) used to be popular too), and [pyo3](https://github.com/PyO3/pyo3) (Python).
* Another area which has great potential is CLI utilities. There's already a vast array of high quality tools built in Rust such as [ripgrep](https://github.com/BurntSushi/ripgrep), [delta](https://github.com/dandavison/delta), [bat](https://github.com/sharkdp/bat) and more. Chances are your colleagues already use some of these, so building tools for your own company would seem just natural. After all, there's a good reason these tools were written in Rust, right?

## **What if I'm coming from backend or Web?**

Coming from Web and services can be the hardest to justify in terms of moving to Rust. Often, the "competition", such as your go-to Node.js and React stack, is just too big (e.g. ecosystem) and too valuable (e.g. sharing code between backend and frontend) to beat.

While frameworks like [yew](https://github.com/yewstack/yew) will feel great for developers who build React based apps, yew is still a niche framework which is not as widely adopted or sought-after as your typical React and Typescript stack.

Check out [*<u>Are we Web yet?</u>*](https://www.arewewebyet.org/) to get inspired for where to start and what to look for.

On the other hand, wasm (Web Assembly) specific use cases are taking off. Checking out how [Figma](https://www.figma.com/blog/rust-in-production-at-figma/) is using Rust is shockingly inspiring. This [wasm category](https://www.arewewebyet.org/topics/webassembly/) on *Are we Web yet?* is particularly exciting.

But there's a lot of hope still. Tooling and infrastructure for the web is taking off in Rust. Examples are [Rome](https://github.com/rome/tools) (built by Facebook/Meta), and [swc](https://github.com/swc-project/swc) which aim to replace Babel, eslint, and similar tools completely, and you can be sure it's jaw-dropping fast.

Rust is a great candidate when building simple APIs or APIs with a specific requirement for performance, safety and simplicity that do one thing well. These include download or upload handlers, image resizing, fast A/B testing APIs, mission-critical and latency sensitive APIs, and more. This is why you'll find Rust jobs in CDN and cloud infrastructure companies, such as [Cloudflare](https://blog.cloudflare.com/tag/rust/).

Other sweet spots can revolve around real-time processing of data: text, audio, streaming, as well as resource-constrained services in an environment such as IoT or cost-sensitive server farm processing. Cryptography is another category where Rust brings a lot of value over other programming languages. You'll find your typical cloud providers such as [Amazon](https://www.amazon.jobs/en/jobs/1639811/software-development-engineer-rust) with these kinds of Rust jobs.

## **I'm coming from C++**

C++ devs enjoy an easy bridging of their mental model of Rust and C++. And so it's natural to first start finding Rust jobs inside their company, as many explore transitioning C++ codebases to Rust.

Another direction to look at is crypto and trading. Where the intuition for low overhead and zero-cost will be highly appreciated. While gaming is not completely taken over by Rust, the speed at which Rust is growing within the gaming ecosystem is amazing. Stockholm-based [Embark](https://www.embark-studios.com/) is famous for adopting and advocating Rust and is worth [following](https://embark.dev/). Either way, I recommend exploring [macroquad](https://github.com/not-fl3/macroquad) and [Bevy](https://bevyengine.org/).

## **I'm coming from infrastructure**

While Go dominates infrastructure jobs, as thinking about Cloud-Native is almost the same as thinking about Go, Rust is growing in these areas as well.

Crypto (blockchain), as a domain, has a lot of Rust. Depending on your interest areas, this may be very appealing and it's very well-known that there are a lot of openings for hiring Rust developers in this domain. Since crypto is thriving, this is one application that does need *a lot* of infrastructure, and it needs to be cost effective, as well as secure and accurate: all natural spots for Rust.

Replacing python utilities and infrastructure is already a popular thing to do. Python is a perfect target for this because many times it's used for data processing and analysis, and that's how a company starts: a smart ML model and a horrible UI slapped over it -- and that's a good thing (MVPs and all).

When that company grows, and if it happens fast, it's most probably they'll keep using Python for everything, including Web services, infrastructure, and tooling -- and that will create a lot of bottlenecks. This naturally happens when you use the same tool for everything. Rust found a sweet spot in these kinds of companies replacing these kinds of workloads, being used to optimize hot paths, most often with [pyo3](https://github.com/PyO3/pyo3). Here is [one example](https://github.com/ijl/orjson) of this in the real world.

## **How do I start?**

The common knowledge that Rust is hard to learn, or that it has a steep learning curve, is actually less true today. Granted, it has a different mental model than most modern languages-- but it does have a *correct* mental model; this means that if you think about how programming languages work, and how computers work, Rust will make sense.

Or in other words, if you tried programming in C, C++, or Assembly during school, or even just played around with them, Rust will make sense.

But what if you have no experience with any of those languages? That's what the Rust community has been assuming, and has put as a target to tame. Over the many years of following Rust - the amount of Rust documentation, books, and guides that were created free and open by the community is staggering.

Since I get that "Yes, but, how do I *start*?" question a lot, I decided to create a community driven Github repo which answers it: [rust-how-do-i-start](https://github.com/jondot/rust-how-do-i-start). You can visit this repo and follow the track outlined there to get started in Rust in no time.And if you want some starting points for who may be hiring in Rust, you can check out the jobs section of the [<u>This Week in Rust newsletter</u>](https://this-week-in-rust.org/) or with [<u>this Reddit search</u>](https://www.reddit.com/r/rust/search?q=flair_name%3A%22%F0%9F%92%BC%20jobs%22&amp;restrict_sr=1).

Best of luck on your Rust journey.

*To learn more about the Rust Foundation, check out our [website](https://foundation.rust-lang.org/), [learn about becoming a member](https://foundation.rust-lang.org/info/become-a-member/) and follow us on [Twitter](https://twitter.com/rust_foundation) and [LinkedIn](https://www.linkedin.com/company/rust-foundation/) to stay up to date.*
