---
title: 'Community Grantee Spotlight: Sebastian Thiel'
byline: Rust Foundation Team
description: >-
  Meet Sebastian Thiel: Gitoxide Core Developer and the first subject of our new
  Rust Foundation Community Grantee Spotlight series. 
date: 2022-11-17T16:00:00Z
tags:
  - grantee spotlight
  - community grants
  - programs
index: false
layout: layouts/news.njk
---
<img src="/img/news/2022-11-17-grantee-spotlight-sebastian-thiel/sebastian.png" width="580" height="326" />

> *<u>About this series</u>*
>
>
> *Welcome to the Rust Foundation’s first installment of the Community Grantee Spotlight series – a collection of blogs that will highlight the accomplishments and experiences of individuals who received a &nbsp;*[*<u>Project Grant</u>*](https://foundation.rust-lang.org/grants/project-grants)*&nbsp; or &nbsp;*[*<u>Rust Foundation Fellowship</u>*](https://foundation.rust-lang.org/grants/fellowships)*&nbsp; as part of our &nbsp;*[*<u>Community Grants Program</u>*](https://foundation.rust-lang.org/grants)*.&nbsp; Each installment will feature an interview with an individual grantee about their progress, goals, and experiences in the program.&nbsp;*
>
>
> *Our intention for this series is to celebrate our hardworking grantees while shedding light on the wide breadth of work they are collectively doing to benefit the Rust ecosystem. We hope you enjoy getting acquainted with these amazing individuals\!*
>
>
> *<u>Note:</u>&nbsp; &nbsp;The Community Grantee Spotlight series will not function as a comprehensive catalog of all our grants/amazing grantees, but instead will highlight a handful of individuals who expressed interest. Please stay tuned for a new page our team is working on that will include info on the grants we’ve issued to date. In the meantime, you can find our most recent announcement of Rust Foundation grants &nbsp;*[*<u>here</u>*](https://foundation.rust-lang.org/news/2022-06-14-community-grants-program-awards-announcement)&nbsp; *– with more to be announced soon\!&nbsp;*

---

## <u><strong><em>The Grant:</em></strong>&nbsp;</u>

Rust Foundation Project Grant (Awarded in June 2022)&nbsp;

### [**<u>&gt;&gt;Learn more about this grant</u>**](https://foundation.rust-lang.org/grants/project-grants)

## ***<u>The Grantee:</u>***

<u>Name:</u>&nbsp; &nbsp;Sebastian Thiel

<u>Location:</u>&nbsp; &nbsp;Xi'an, China & Berlin, Germany

<u>Pronouns:</u>&nbsp; &nbsp;He/him

<u>Fun fact:</u>&nbsp; &nbsp;*“Tried to rewrite Git in multiple languages, succeeding only with Rust.”*

<u>Connect with Sebastian on:</u> [<u>Twitter</u>](https://twitter.com/theelbasian), [<u>GitHub</u>](https://github.com/Byron), or [<u>KeyBase</u>](https://keybase.io/byronbates)

### Special thanks to &nbsp;[<u>Pascal Kuthe</u>](https://github.com/pascalkuthe)&nbsp; & &nbsp;[<u>Sidney Douw</u>](https://github.com/SidneyDouw)&nbsp; for their hard work on the&nbsp; `gitoxide`&nbsp; project\!

## ***<u>The Work:&nbsp;</u>***

Improving the `gitoxide` project (a Rust implementation of Git) with a special focus on [<u>supporting shallow clones</u>](https://github.com/Byron/gitoxide/issues/450) in Cargo.

### **You can find &nbsp;`gitoxide`&nbsp; on GitHub <a target="_blank" rel="noopener" href="https://github.com/Byron/gitoxide">here</a>. &nbsp;**

**<img src="/img/news/2022-11-17-grantee-spotlight-sebastian-thiel/quote-sebastian.png" width="580" height="326" />**

## ***<u>The Conversation:&nbsp;</u>***

### **<u>Q: Tell us a bit about your background with Rust prior to the Community Grants Program</u>**

I’ve been with Rust from the very beginning – before it went 1.0. I don't remember how I discovered it, to be honest\! But when I did, I realized that it was something really special and different. When I discovered Rust, I saw an entirely new paradigm in front of me.&nbsp; This is why I was willing to really hit a brick wall with my head over and over to learn it back then when there were far fewer resources than today.&nbsp;

At the time, there were a great number of missing education gaps and the compiler wasn’t as helpful in telling you what was wrong with the program. The borrow checker was also less powerful at that time, requiring many workarounds that aren't needed nowadays.

I started out with Rust in 2015 –&nbsp; a crazy seven years ago. Since then, I've stuck with it.

### **Q: Tell us about the background of &nbsp;**`gitoxide `**\! How did this project come to be?**

Since&nbsp; &nbsp;`gitoxide`&nbsp; is a big project (one I’ve been with for two and a half years, mostly full-time\!) I think it’s important to start with talking about why there’s a need for &nbsp;`gitoxide`&nbsp; at all.

It started with a “eureka\!” moment that I had when I first discovered Git about 15 years ago. Git was a total eye-opener for me. I thought, “this is what simplicity and ingenuity looks like. This is what version control should be”.&nbsp;

A few years into using Git, I became interested in having programmatic access to write applications that leverage Git as a data structure. I was using Python at the time, so I found a project called GitPython that I started contributing to early on in its history. I just threw myself in it, rewrote it in the process and became the last remaining maintainer to this day .&nbsp;

I now consider this to be a “sin of my youth” in a way because I really didn't know how to do these things properly. And a LOT of people use it. When I first looked into the numbers, the PyPi download statistics were at around a million per day. When I discovered this, I got a little freaked out – I realized that I had to be a bit more careful when I did new releases, because people were actually affected by this.&nbsp;

So I was sitting at the intersection of Python and Git, but I knew I would never be able to write the applications I had in mind. I kept trying to write Git in Go and in C++, but both dead ends. I started thinking “what’s the benefit of this pursuit if the best possible level I can hope for is the bar that Git sets?” A high bar to be sure, but I thought there had to be a higher level to reach.&nbsp;

Now, even though Git is dominating version control, it's written in C. In terms of adapting to the needs of modern computers, this is a big disadvantage. To rewrite Git in another language and reach my goal, I had to be able to accommodate the current reality of computing. Rust seemed like the only answer. Even so, I was daunted by the scale of such a project.&nbsp;&nbsp;

By this juncture, I had moved to China and that’s when COVID-19 hit. As we now know, China enforced rigorous lock downs, so I was literally locked in a house. It seemed like the perfect time to really give &nbsp;`gitoxide`&nbsp; a go.&nbsp;

### <u><strong>Q: Can you explain &nbsp;</strong><code>gitoxide</code></u>**<u>&nbsp; for the uninitiated?</u>&nbsp;**

I think it’s easiest to say what &nbsp;`gitoxide`&nbsp; is *not*. &nbsp;`gitoxide`&nbsp; is not libgit2. It is the de facto API to write applications that interact with Git. But by now, it's kind of dormant and in maintenance mode. Many new features are not actually implemented.&nbsp;

`gitoxide`&nbsp; provides users with a nice API with the power to rewrite Git. It allows you to write your own tools for Git that act as naturally as they possibly can. And despite giving you all that power, the levers are below the surface and there if you need them. If you don't, &nbsp;`gitoxide`&nbsp; functions exactly as Git would.&nbsp;

### <u><strong>Q: What are some of the larger benefits and impacts you expect to see from &nbsp;</strong><code>gitoxide </code><strong>?</strong></u>

`gitoxide`&nbsp; makes it so much more convenient to work with Git repositories and write applications that interact with it. Plus, thanks to Rust, it's safe by default.

Similar to the Rust compiler itself, if there’s something preventing &nbsp;`gitoxide`&nbsp; from working, you will see a beautiful error message that shows you exactly what went wrong. It’s not only good for the user, but also good for you as a software developer.&nbsp;

`gitoxide`&nbsp; is also vastly more efficient with your computer’s resources than Git is. It grows with your computer, because it just uses all cores efficiently by default – that makes a huge difference.&nbsp;

I think in the long term, Git will have trouble matching the efficiency and experience of &nbsp;`gitoxide`&nbsp; – even though I wish it would because more efficiency is good for everybody.&nbsp;

### <u><strong>Q: What prompted you to apply for the Rust Foundation&rsquo;s Community Grants Program?</strong></u>

As an open source software developer, a father, and as a family man, I have to constantly figure out how to reach my programming goals without exhausting my own resources. This is why I’m always on the lookout for grants to fund my work, but I’m careful to choose them wisely.

When I heard about the [<u>Rust Foundation&rsquo;s Community Grants Program</u>](https://foundation.rust-lang.org/grants), I was in the midst of asking myself what I could do to produce value for the Rust community *right now.* I was thinking deeply about the effort that would be the lowest hanging fruit for the Rust Project, the highest value for the cost, while still being sponsorable. Given the relationship between this program and the Rust community, there was no question in my mind that the Community Grants Program was worth applying to.

### <u><strong>Q: What are you most proud of having accomplished under the program so far?&nbsp;</strong></u>

`gitoxide`&nbsp; can clone repositories typically 1.5x faster than what you can do with Git, which I consider to be a game-changer. You can learn more about this exciting development [<u>here</u>](https://github.com/Byron/gitoxide/discussions/579).&nbsp;

### <u><strong>Q: What are your top areas of focus for the next phase of the program?&nbsp;</strong></u>

Currently, I believe it’s massively important to finish the integration of &nbsp;`gitoxide`&nbsp; into cargo and completely remove the dependency to the git2 crate, which would complete the work done in this phase.

### <u><strong>Q: What has your experience as a Rust Foundation grantee been like so far?&nbsp;</strong></u>

Even though I see the Rust Foundation as a stakeholder that is easily approachable, they are definitely as quiet as you allow them to be. This is an advantage in my case because I’m pretty self-driven when it comes to reaching my goals. That said, I’d like to gain more insight into the experiences of other grantees as it would help build upon the community feeling – that’s why I’m excited for the Community Grants Spotlight series\!

### <u><strong>Q: Name one new thing about Rust that you&rsquo;ve learned from your work under the program.</strong></u>

I finally picked up \`cargo-fuzz\` as a simple way to let a fuzzer find input that exercises all code-paths, even the ones I thought were impossible to encounter. This typically adds another layer of quality to make Rust code even better. It’s worth noting that the fuzzer never finds exploitable input, just input that can be handled more gracefully.

### <u><strong>Q: What would you tell someone who is interested in applying for the Grants Program but is unsure about whether or not they &ldquo;should&rdquo;?&nbsp;</strong></u>

From my perspective, most developers have a knack for analytical thinking. If there’s any kind of fear you’re experiencing that’s preventing you from applying for a grant like this one, try to squash it with analysis and a focus on the greater benefit of what you’d like to accomplish. If you find yourself getting down on your own knowledge or doubting your worthiness of a grant to fund your work, remember that even those you put on a pedestal doubt themselves. You’re not in this alone.

I’d also like to say that I think we as an industry need to do a better job of copping to our own fears and perceived weaknesses publicly. This would help the community almost as much as our open source contributions.&nbsp;

### <u><strong>Q: Any advice for the next round of applicants to our program?</strong></u>

From my experience, the Rust Foundation makes sure to pick projects with a wide set of goals and your idea might be just right despite being off the beaten path. It won’t hurt to fill in the form and see where it takes you, knowing that the Rust Foundation will be supporting you along the way no matter the outcome.

### **<u>Q: If you had to pick one word (or maybe a few!) to describe your experience under the Community Grants Program, what would it be?</u>&nbsp;**

**Transparent. Trusted. Trusting**. I do what I set out to do while receiving financial support. There is basically no overhead for me to be part of the Community Grants Program, and I can funnel all my energy towards my goals, which now are a part of the goals of the Rust Foundation, too.

### <u><strong>Q: What excites you most about Rust/the future of Rust?&nbsp;</strong></u>

Rust is being adopted at such a rapid pace despite being barely more than a toddler in computer-language age. Rust redefines software quality and what’s possible with our hardware, breaking performance records ranging from multiple orders of magnitude performance increases to multiples of it. This makes it an absolute game-changer, as it puts this power into the hands of people that previously would not have been able to accomplish such feats with existing technology, like C and C++.

---

### **Thank you to Sebastian for taking the time to chat with our team about his work under the Community Grants Program so far\! We’re excited to publish more installments of our Grantee Spotlight Series in the near future. You can follow the development of the series <a target="_blank" rel="noopener" href="https://foundation.rust-lang.org/tags/grantee%20spotlight"><u>here</u></a>.&nbsp;**

---

<u>About the Rust Foundation Community Grants Program</u>

The Rust Foundation &nbsp;[<u>Community Grants Program</u>](https://foundation.rust-lang.org/grants)&nbsp; provides access to new resources for the Rust community to maintain, innovate, collaborate over, and further develop the Rust programming language. While the Community Grants Program provides financial backing across several different categories (Events Support Grants, Rust Foundation Fellowships, Hardship Grants, and Project Grants) the overall mission is shared: to support the continued expansion of Rust and address key areas for development across the Rust ecosystem.

### &nbsp;

> ### *The Rust Foundation Community Grants Program is made possible by AWS, Huawei, and Google. Learn more about the program &nbsp;*[*<u>here</u>*](https://foundation.rust-lang.org/grants)*.&nbsp;*
>
> ### *If your organization is interested in supporting the program, we'd love to hear from you\! Please reach out to us at [grants@rustfoundation.org](mailto:grants@rustfoundation.org) to inquire about donation/support options.&nbsp;*