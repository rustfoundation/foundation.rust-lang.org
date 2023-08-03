---
title: 'Member Spotlight: Turbofish'
byline: Rust Foundation Staff
description: Introducing Turbofish, a Rust Foundation Silver Member organization.
date: 2023-08-03T12:00:00Z
tags:
  - member spotlight
index: false
layout: layouts/news.njk
---
*Welcome to another installment of the Rust Foundation Member Spotlight series! These blogs aim to introduce our community to various Rust Foundation Member organizations and their leaders. In this installment, we spoke with Judd Keppel, CTO of* [*<u>Turbofish</u>*](https://www.turbofish.org/) *— the newest Rust Foundation Silver Member organization. Judd chatted with the Rust Foundation team about the work of Turbofish, how they use Rust, and more.&nbsp;*

## **Tell us about Turbofish. What do you do and who do you serve?**

[<u>Turbofish</u>](https://www.turbofish.org/) is a team of Rust developers building open-source blockchain technology. We founded [<u>Nomic</u>](https://www.nomic.io/), a Bitcoin bridge for the Cosmos ecosystem, and [<u>Orga</u>](https://github.com/turbofish-org/orga), a fully custom blockchain stack that we use to develop Nomic.

We aim to serve the developers and users of applications built with Orga. We work like a video game studio, where Orga is like our game engine. By building Orga up to meet the needs of Nomic, we’re working to make it the perfect state machine engine for developers to build their own applications in the future.

## **How is Turbofish using Rust?**

Everything we build is in Rust. Our goal is to build software that’s fast, reliable, and correct. Rust lets us do this without sacrificing succinctness and developer experience. We push the language to its limits to allow developers to write blockchain apps in their purest form, reasoning only about the problem domain.

We have three core traits in Orga: \`State\`, \`Call\`, and \`Query\`. \`State\` manages the mapping between a user-defined type and its location in the backing database. \`Call\` defines a state machine transition, some action that can be triggered by a network participant. \`Query\` describes efficient, Merkle-proven, application-specific data requests by clients.

We use Rust’s macro system to generate impls of these traits for a custom type while maintaining the flexibility to support hand-implementation.

\`Call\` messages are derived from the signatures of methods with mutable receivers annotated \#\[call\]. Ditto for \#\[query\] on a method with an immutable receiver. \`State\` types are self-describing schemas for data in the underlying KV-store. Clients can be automatically generated and used in the browser via WASM.&nbsp;

The result is that writing the production blockchain-ready version of an app is barely different from its vanilla Rust form.

## **Why the name Turbofish?**

At Turbofish, we just really love Rust and wanted to pay homage to Rust in our name. We’ve always been amused by the quirky name of the turbofish syntax. Shout-out to [<u>Anna Harren</u>](https://github.com/iirelu), who first used ‘turbofish’ to describe the ::&lt;&gt; syntax and sadly passed away a few years back.&nbsp;

## **Why did Turbofish decide to join the Rust Foundation?**

As maintainers of open-source projects, we know the importance of the communities behind them. We joined to help the Rust Foundation support the community, and so we can give back and stay connected to those contributing to the Rust project.

## **What are your hopes for the future of Rust?**

So much effort and love is being put into async and we hope it really starts to feel like a first-class citizen of the language. It feels like we're getting closer every day.

In the nearer future, we’re hoping for the stabilization of features like specialization, trivial bounds, and auto traits / negative impls. The Rust contributors are ambitious in their continuous evolution of the language, and I hope that never fades.

## **What message would you like to share directly with any members of the Rust community reading this blog?&nbsp;**

Crypto isn’t all bad.

The eye-watering valuations of useless coins and streak of shady characters have overshadowed the natural value alignment between crypto and open-source. Many of us got into the technology because we value decentralization, online communities, and interesting technical problems. As part of the Rust community working on crypto projects, we hope we can help change this over time.

## **What is your personal favorite thing about Rust?**

For me, the answer is procedural macros – easily. The combination of Rust’s type system with crates like syn, quote, and darling make metaprogramming in Rust so fun. This is a hugely underrated part of the Rust experience.

*Judd Keppel is the co-founder and CTO of Turbofish. Judd co-founded Turbofish in 2018 after departing from Tendermint where he worked on Cosmos. Turbofish is building Nomic, a Bitcoin bridge for the Cosmos ecosystem. Judd leads the Rust-based engineering team contributing to Nomic and Turbofish’s other projects.*

---

### Welcome to the Rust Foundation, Turbofish!

You can learn more about Turbofish on their [<u>website</u>](https://www.turbofish.org/) and [<u>blog</u>](https://www.turbofish.org/blog)&nbsp;and connect with their team on [Twitter](https://twitter.com/turbofish_org) and [LinkedIn](https://linkedin.com/company/turbofish).&nbsp;