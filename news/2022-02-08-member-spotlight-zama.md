---
layout: news
series: "Member Spotlight"
title: "Member Spotlight: Zama"
description: Introducing Zama, Rust Foundation Silver Member.
tags:
   - member spotlight
---

![Rand Hindi](/img/posts/2022-02-08-member-spotlight-zama/member_spotlight_rand_hindi.png)

As we settle into 2022, we’re excited to share the first member spotlight of the new year. Launched in September, the member spotlight series serves as a way of introducing our growing roster of silver member companies to the wider Rust community. We’re thrilled to welcome such an interesting and diverse group of companies to the Rust Foundation family, and we look forward to seeing the Silver Member ranks grow. In today’s post we hear from [Rand Hindi](https://twitter.com/randhindi), Co-founder and CEO of [Zama](https://zama.ai/). Read on to learn more.

## Tell us a bit about Zama.

At Zama, we are building an open source framework for homomorphic encryption, a new data encryption approach that enables users to compute on encrypted data. It allows for the blind manipulation of data, without allowing the user to see the actual data. Our framework, [Concrete](https://zama.ai/concrete/), is completely open source, built in Rust and is arguably the most advanced toolset in the space. We designed it specifically for non-cryptographers. Developers who want to use homomorphic encryption to secure the data in their applications can do that using the Concrete framework, even if they know nothing about cryptography or homomorphic encryption.

The Concrete technology is designed for building applications where sensitive data needs to be manipulated in the cloud. Think of medical products, facial recognition, blockchain, financial services, and so on. Imagine you are a company and want to use facial recognition to authenticate your users. The company that authorizes the facial recognition service would need your passport (or another official document) in a database to provide a visual match. With homomorphic encryption, you’d send an encrypted version of your passport to the facial recognition provider, they would not have the ability to decrypt it, but they could run their facial recognition algorithms on it and do a match between an encrypted photo and the encrypted passport. The user experience isn’t impacted at all, but the provider of the service no longer has access to your sensitive information – everything is truly encrypted end-to-end. To learn more and stay up to date with everything we do at Zama: [subscribe to our newsletter](https://zamafhe.substack.com/).

## How does Rust fit into your work?

I’ve been personally involved with Rust since 2015, when my previous company was using it in embedded machine learning. Rust was very young at the time and not as widely supported as it is today, but it was still a no-brainer for us. In fact, when I first discovered Rust, it was love at first sight because it fit our needs perfectly. When we started Zama, Rust was a natural choice, and we use it for almost everything – the cryptographic library, the backend, and the web services we’re working on.

## What about Rust made you fall in love? What are your favorite features?

As a cryptography company, we’re all about providing privacy and security and we don’t want to worry about things like bugs in the code or memory leaks. Rust is the safest language you can use for high performance, sensitive code. For me, the safety piece was a crucial part of why Rust was such a perfect fit. Rust also provides the system level performance needed for high-performance computing and mathematical computing, which is also necessary for our business.

## What made you interested in joining the Rust Foundation?

We just wanted to get more involved in the community in general. For us, using Rust has been great for many reasons and we want to contribute whatever we can. We’re also interested in open source in general, and I feel the Rust and open source communities are closely linked. I could say the same for the privacy community – the Rust community is very privacy-centric, which is obviously important. The Foundation ticked a lot of boxes, and I enjoy having the opportunity to be a part of a community where I can have good conversations and think productively with other members.

## Where would you like to see the Foundation go in the coming years?

I’d like to see Rust replace C++. I think the Rust Foundation has an important role to play in helping Rust graduate from advanced engineering to mainstream engineering. Five or six years ago when I started with Rust, it was sort of “hipster,” something the cool people were using. Then it became a productive language, as the tooling started catching up and people started using it and online courses started catching up. Now it’s becoming approachable. The next step is making it ubiquitous and the number one language everyone uses. Why would you want to use something that is clearly inferior in terms of developer experience? A lot of contemporary thinking has gone into building Rust, and it’s time to get the language out there even more.

## Has Rust helped with any specific challenges? 

In my experience, you can make things work in any language, but sometimes it’s much more painful than it needs to be. Rust gives us a lot of peace of mind on the security side, which was a challenge with some other languages. It’s also fun to use, and it works in a very elegant way. One collateral benefit of being a Rust shop was that it has helped us recruit good talent – we were able to attract a lot of great engineers because we offered the opportunity to work in Rust. In my experience, the engineers who want to work in Rust are better than the average engineer, so it’s been a great tool for hiring talented employees. The best engineers want to use the best technologies, and Rust certainly falls into that category.

## If you had to describe Rust in just three words, what would they be?

Secure, fast, and fun.


To learn more about the Rust Foundation, check out our [website](https://foundation.rust-lang.org/), [learn about becoming a member](https://foundation.rust-lang.org/info/become-a-member/) and follow us on [Twitter](https://twitter.com/rust_foundation) and [LinkedIn](https://www.linkedin.com/company/rust-foundation/) to stay up to date.
