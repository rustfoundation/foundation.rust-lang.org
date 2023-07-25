---
title: 'The Power of Rust Adoption: Lessons From Google'
byline: Rust Foundation Staff
description: Rust adoption insights from Rust Foundation Platinum Member Google
date: 2023-07-25T12:00:00Z
tags:
  - membership
  - member stories
  - adoption
index: false
layout: layouts/news.njk
---
<img src="/uploads/lars-bergstrom-graphic.png" width="580" height="326" alt="The Power of Rust Adoption:  Lessons From Google" title="[Heading] The Power of Rust Adoption:  Lessons From Google [Sub-heading] With Lars Bergstrom  Director of Engineering at Google for Android Platform Programming Languages,  Rust Foundation Board of Directors Chair" />

Rust Foundation Platinum Member, Google recently published a [<u>valuable blog</u>](https://opensource.googleblog.com/2023/06/rust-fact-vs-fiction-5-insights-from-googles-rust-journey-2022.html) by Lars Bergstrom, Ph.D. (Director of Engineering at Google for Android Platform Programming Languages and Chair of the Rust Foundation Board of Directors) and Kathy Brennan, Ph.D. (Low-Level Operating Systems Sr. User Experience Researcher at Google).&nbsp;

In the post entitled “[*<u>Rust Fact vs. Fiction: 5 Insights from Google's Rust Journey in 2022</u>*](https://opensource.googleblog.com/2023/06/rust-fact-vs-fiction-5-insights-from-googles-rust-journey-2022.html)”, Lars and Kathy share key insights gleaned from the experiences of over 1,000 Google developers who have used Rust in some part of their work in 2022. They also cite data from the early days of Rust at Google to address some common claims about adopting Rust, including rumors like “Rust takes more than 6 months to learn” (debunked!) and “Rust code is high-quality” (confirmed!).&nbsp;

Organizations like Google ultimately decide to become members of the Rust Foundation because they believe in the current power and promise of this incredible programming language and see its potential. Rust Foundation Members also know that the Rust community and Project continue to do amazing things with the language – and because of this, they understand the value of investing engineering time in contributing to a global effort to build memory-safe, efficient, and scalable technology.&nbsp;

But of course, it’s not just Rust Foundation Members that believe in Rust – its widespread popularity amongst developers and other organizations has [<u>climbed</u>](https://survey.stackoverflow.co/2023/?utm_source=so-owned&amp;utm_medium=blog&amp;utm_campaign=dev-survey-results-2023&amp;utm_content=survey-results#technology-admired-and-desired) in recent years and we have every reason to believe this growth will continue. Even so, the Rust Foundation understands that deciding to learn a new language is a significant decision for any developer, just as adopting new technology is for organizations.&nbsp;

This data shared by Google makes a strong case for Rust adoption, despite these universal considerations when evaluating any new tool. To quote Lars in the blog:&nbsp;

> *“Developer satisfaction and productivity are correlated with both code quality and how long it takes to get a code review. If Rust is not only better for writing quality code but also better for getting that code landed, that’s a pretty compelling set of reasons beyond even performance and memory safety for companies to be evaluating and considering adopting it.”&nbsp;*

## We recently chatted with Lars about [<u>the findings</u>](https://opensource.googleblog.com/2023/06/rust-fact-vs-fiction-5-insights-from-googles-rust-journey-2022.html) of this 2022 survey of Rust developers at Google and asked him for some more context around Google’s initial decision to adopt Rust, how Google supported its developers using Rust in the early days, and more. Here’s what he had to say during this mini-interview:&nbsp;



### Q: What were some of Google’s questions and concerns about adopting Rust in the early days? How do you feel about those things several years into Google’s Rust adoption?&nbsp;

First, it’s important to note that while some projects at Google such as Android are [<u>very far along</u>](https://security.googleblog.com/2022/12/memory-safe-languages-in-android-13.html) in their journey to Rust adoption, other projects such as Chromium are [<u>just beginning their support</u>](https://security.googleblog.com/2023/01/supporting-use-of-rust-in-chromium.html). But despite the timing differences across all of these Google projects, there’s a commonality in terms of technical concerns (“*Can Rust support our specific needs?”*, *“Will adopting Rust enable interoperability across languages?”* , *“How will Rust integrate with not only existing build systems but all of the deployment infrastructure?”*) and business concerns (*“How do I hire, train, and manage my Rust team?*”, “*How long will it take to onboard new developers?”*, *“Once fully up to speed, how productive are they at delivering and supporting features relative to existing languages?”*).&nbsp;

Several years into the Android team’s adoption of Rust, we’re very confident that Rust provides encouraging answers to those technical concerns. We’ve found Rust to be competitive with C++ and in some cases even competitive with Java in terms of tooling support and developer productivity. However, various teams at Google are still evaluating those business concerns.&nbsp;

This is why Dr. Kathy Brennan and I decided to formally evaluate the state of Rust adoption at Google and where we can improve. Today, we’re very confident that Rust is ready for production use in many projects at Google.

### Q: You shared some interesting details about Google developers’ experiences using Rust. In general, Rust seems to have improved developer satisfaction while providing tremendous value for Google. Now that your team is taking a data-informed Rust victory lap, can you share how Google supported its developers learning Rust, especially in those early days?&nbsp;

There’s a sort of half-joke in the community that there is a “Rust Evangelism Strike Force,” and there’s some truth to it. Just like any language or technology, there are always early advocates, and from a Google perspective, we’ve tried to channel that enthusiasm into direct support for the teams doing their first project. Having a direct channel to someone who is both enthusiastic and plugged into the broader Rust project community helped us see early success.

Once you have a successful project or two, it’s essential to evangelize that success internally to build confidence both amongst other engineers and management. A former colleague of mine, Dave Herman, used to say “Nothing succeeds like success.” That’s especially true in our modern data-oriented world. Showing a record of good performance, reliable updates, and a lack of security vulnerabilities to users is hard to argue with.

As Kathy and I mentioned in our blog, demonstrating that management is *investing* in this initiative is a great way to build confidence within a team – especially in a corporate setting. Paying to bring in top training staff (as we did with Ferrous Systems) as well as hiring staff or funding work in the Rust ecosystem demonstrates a commitment from the executive team.&nbsp;

Hopefully, at some point in the open source adoption journey, you will create momentum to sustain your efforts. These days at Google, I have to argue more about how to *slow down* adoption in new projects and to maintain the same testing diligence!

### Q: Do you have any advice for other organizations who see the value in Rust but are weighing the typical considerations of adopting a new tool or language?&nbsp;

At the organizational level, I’m a huge fan of starting small and building confidence over time and with numbers. When it comes to evaluating how Rust will work for your team, I recommend starting with a *tiny* change to your codebase that’s not user-facing. However, when preparing to make even the smallest change to your codebase, you need to predetermine how you will gather data about the project’s deployment and use and how you will track this over time. Having a plan for collecting data and success metrics for the project you’re evaluating is critical.&nbsp;

### Q: In just a few words, how would you describe Rust's impact on Google?

I like to say that Rust has the safety and productivity of Java but with the performance of C++, because that phrasing really captures how we’re seeing Rust deployments play out in practice.&nbsp;

The reason Rust has been so revolutionary on my team at Google is that it helps ensure code safety and security while avoiding many downstream costs like patching security issues, crashing, and the resource-intensive dynamic mitigations we are enabling around C++ code to protect our users.

To sum it up, Rust is enabling many teams at Google to write high-performance code more easily and efficiently without the additional costs and challenges they would otherwise encounter.&nbsp;

---

Thank you to Lars Bergstrom for sharing further insights into Google’s experience with Rust. We highly recommend reading his recent Google blog authored with Kathy Brennan, Ph.D. (Low-level Operating Systems Sr. User Experience Researcher,) entitled “[<u>Rust Fact vs. Fiction: 5 Insights from Google's Rust Journey in 2022</u>](https://opensource.googleblog.com/2023/06/rust-fact-vs-fiction-5-insights-from-googles-rust-journey-2022.html)“. In it, you’ll find key insights gathered from over 1,000 Google developers that used Rust in 2022.&nbsp;

*Click* [*<u>here</u>*](https://foundation.rust-lang.org/members/) *to learn more about how you can support the Rust ecosystem through Rust Foundation membership.*