---
title: 'Member Spotlight: Helsing'
byline: Rust Foundation Team
description: Introducing Helsing, a Rust Foundation Silver Member organization.
date: 2023-08-22T12:00:00Z
tags:
  - member spotlight
  - announcement
index: false
layout: layouts/news.njk
---
*Welcome to another installment of the Rust Foundation Member Spotlight series! These blogs aim to introduce our community to various Rust Foundation Member organizations and their leaders. In this installment, we spoke with two leaders at* [*<u>Helsing</u>*](https://helsing.ai/) *— the newest Rust Foundation Silver Member. Keep reading to learn about Helsing from Dr. Robert Fink (CTO) and Dr. Jon Gjengset (Principal Software Engineer).&nbsp;*

## **Tell us about Helsing. What do you do and who do you serve?**

<u>Robert:</u> Helsing is a new type of defense company. We believe that software, in particular artificial intelligence, will be the key to protecting our democracies. Our teams design technology products that transform the operational capabilities of both new and existing defense platforms, to deliver faster and more accurate decision-making at the tactical, operational, and strategic levels.

Helsing is a pan-European, multi-domestic company with national entities in Germany, the UK, and France. As a result, we can access the widest pool of European talent for technology infrastructure and capabilities. Our domain experience means we are attuned to the most difficult problems faced by our governments. Helsing has had a pretty exciting ride so far, growing from 4 to 200 employees (140 of which are on the engineering team) in the course of two years.

## **How is Helsing using Rust?**

<u>Robert:</u> We have several different categories of Rust use cases at Helsing.

First, the core components of our software platforms are written in Rust, particularly at the data layer. Since these applications are designed to run in resource-constrained environments (think Jetsons or other embedded systems,) we value execution efficiency and the control Rust gives us on memory management and concurrency.

Second, a growing share of our AI stack relies on Rust, from data loaders and inner loop code during model training to GPU-centric inference engines and non-ML algorithms.

Finally, we love Rust for cross-language use cases. For example, we cross-compile knowledge graphs into TypeScript/WebAssembly and Python so that all developers and applications can use the same functionality. Similarly, we generally wrap third-party C and C++ code in Rust bindings in order to contain the expanse of non-core languages and artisanal build systems.

The bottom line is that about 50% of our code is Rust-native and the other half (Python, C++, TypeScript) is slowly but surely getting replaced with Rust.

## **Why did Helsing decide to join the Rust Foundation?**

<u>Jon:</u> Helsing, like most companies that make extensive use of Rust, is able to do so in large part due to the amazing (and often volunteer-based) work of the Rust community. And while we are establishing a culture internally of contributing back to that community whenever possible, we recognize that there is a lot more to community work than technical contributions. Infrastructure costs money to run, communities need stewards to thrive, and maintainers need support so they can dedicate time to their projects. We believe that working with the Rust Foundation is a great way to support all those other aspects of Rust.

But for Rust to truly flourish, we need advocates who can bring Rust into new spaces and help the language work well everywhere it has the potential to. We believe that Helsing can be one such advocate.&nbsp;

We can — and already are — bring Rust into entirely new environments and expose it to organizations that may otherwise not have thought that Rust could be for them. And in those interactions, we often encounter idiosyncratic requirements in regard to supply chain security, machine learning toolchains, and specialized hardware and embedded systems. Through our involvement with the Rust Foundation, we can harness those experiences and share them with the broader community.

Beyond supporting Rust and being more plugged into the community going forward, we also believe that we work on super unique, difficult, and important problems that are worth sharing. If our work inspires any of you fellow Rustaceans, please get in touch with us — we'd love to welcome you to the Helsing family!

## **What are your hopes for the future of Rust?**

<u>Jon:</u> I have many hopes for Rust! In the context of Helsing, there are three priorities that stick out to me.&nbsp;

First, even with the wide and rapid adoption of Rust over the past few years, I still think we’re in the early days. Rust is rapidly proving itself as a language with sufficient value to penetrate industries that have traditionally made conservative technology choices. Widespread adoption will not happen quickly, due to the slow and deliberate nature of those industries (often by necessity,) but we’re seeing the early signs. Helsing itself is proof of that.

As this adoption continues, I hope we will see Rust improve its appeal to more risk-averse audiences. That entails work on a number of less language-centric aspects of the project, such as supply chain security, build isolation and reproducibility, and a stable and well-oiled organizational structure. And maybe throw some formal verification in there for good measure. All of these are work-in-progress and will require both attention and investment in the years ahead.

Second, at Helsing, we are all-in on Rust for cloud-native and embedded applications. We’re also increasingly betting on Rust for ML training and runtimes. However, we still find that the available tools and libraries are lagging behind what our ML researchers have come to expect from Python. We hope to directly contribute toward improving this situation.

Third, there is still a significant talent gap between Rust and more established languages. While so many of the Rust developers we’ve met and worked with have been excellent, there are few of them overall. This is largely a pipeline problem where the situation will naturally improve over time, though we also believe that further investments in educational materials to soften the learning curve will be key to growing the Rust talent pool.

## **What message would you like to share directly with any members of the Rust community reading this blog?&nbsp;**

<u>Jon:</u> First and foremost, to the community: thank you, thank you, thank you. Not only have I personally gotten a lot of value from being part of and contributing to the Rust community, but I have also seen the extensive impact of all you do at scale at AWS and now at Helsing. Without you all, we would all still be writing high-performance, security-critical systems in C++ and Java, and paying the price.

To enterprise leaders: Rust is here to stay. While it is a young language with room to grow and pain points to overcome, it has already proven its value again and again across a wide variety of domains and companies, including some of the most sensitive, security-minded, and high-risk domains on Earth). It maintains the performance characteristics and low-level control of languages like C and C++, but adds correctness guarantees that, in our opinion, are essential to safely maintain innovation and development velocity in high-risk environments. Ultimately, we don't consider Rust a bet — quite to the contrary; we think it is the only reasonable and responsible choice that meets the requirements of our industry.&nbsp;

## **What is your personal favorite thing about Rust?**

<u>Robert:</u> I had spent the majority of my pre-Rust programming career in Java. When I first started playing with Rust around 2015/2016, I was obviously hit by the steep learning curve, but I also realized that my particular style of Java was directionally very compatible with the constraints Rust imposes on you “qua language”: strong encapsulation and ownership, immutable data, concurrency via message passing rather than locks over shared mutable data.&nbsp;

So while I definitely struggled at the outset, I was always very aligned with the rationale behind Rust’s design decisions and appreciated that the compiler would point out where I was lazy or not quite understanding things.&nbsp;

Since learning Rust, I have come to love the simplicity of the development infrastructure and the fact that Rust has straightforward - and reasonable - opinions on topics that nobody should really spend time arguing about (for example, docs are always formatted like they are on[<u> docs.rs</u>](https://docs.rs/), there is one canonical code format and a tool that enforces it, dependencies are always declared and then locked, etc).

I am also deeply impressed by the quality of the ecosystem. Rust has attracted an amazing community of developers who are generally comfortable with the “modern way” of coding, favoring quality and testing, and automation over simply hacking things together. Rust feels like a community of software engineers — not merely “coders”. The quality of the tooling and library ecosystem is generally very, very high.

Finally, I love that code generation is a first-class experience in Rust, both via macros and build.rs. Code-gen is a powerful feature, but the experience is subpar in many other languages.

### **About Dr. Robert Fink**

*Dr. Robert Fink is Helsing’s CTO and responsible for all aspects of technology and software development, including recruiting, platform architecture, engineering culture, and education. Prior to joining Helsing, Robert was a distinguished software engineer at Palantir Technologies and the founding engineer and chief architect of Palantir’s Foundry Platform. Robert holds a Ph.D. in database theory (University of Oxford, UK) and degrees in physics and computer science (University of Munich, Germany).*

### **About Dr. Jon Gjengset**

*Dr. Jon Gjengset is a principal engineer at Helsing who recently joined the company to support, reinforce, and expand the company’s use of Rust. He is also well-known in the Rust community for developing educational resources like the [<u>Crust of Rust</u>](https://www.youtube.com/watch?v=rAl-9HwD858&amp;list=PLqbS7AVVErFiWDOAVrPt7aYmnuuOLYvOa) video series and the [<u>Rust for Rustaceans</u>](https://nostarch.com/rust-rustaceans) book. Prior to Helsing, Jon maintained the Rust internal build tooling at Amazon Web Services. He is originally from, and now based in, Norway, but was awarded his Bachelor's degree, Master's degree, and Ph.D. from Australia (Bond University), England (University College London), and the US (MIT), respectively.*

---

## Welcome to the Rust Foundation, Helsing!

You can learn more about Helsing on their [<u>website</u>](https://helsing.ai/) and [<u>blog</u>](https://blog.helsing.ai).&nbsp;