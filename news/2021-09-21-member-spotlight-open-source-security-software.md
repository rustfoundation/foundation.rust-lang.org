---
layout: news
series: "Member Spotlight"
title: Open Source Security
byline: Joel Marcey, Rust Foundation Member Director, Facebook
description: Introducing Open Source Security, Rust Foundation Silver Member.
tags:
   - member spotlight
---

![Brad Spengler Open Source Security](/img/posts/2021-09-21-member-spotlight-open-source-security-software/member_spotlight_brad_spengler.png)

The Rust Foundation has been building some great momentum since our launch earlier this year, and we’re excited to share that our member roster is growing. Over the coming few months, we’ll be doing some deep dives with our new member companies so you can get to know our community a bit better. We’ll share some background on what they do, why they chose to join the Rust Foundation and what they hope to accomplish going forward.

To kick things off, [Brad Spengler](https://twitter.com/spendergrsec), president at [Open Source Security](https://opensrcsec.com/), answered some of [my](https://twitter.com/JoelMarcey) questions. Here’s what he had to say:

### Marcey: For those who don’t know, tell us a little about Open Source Security.

**Spengler**: Open Source Security, Inc. develops and maintains grsecurity®, a secure drop-in replacement for the Linux kernel.  Our team has created the technologies behind DEP, ASLR, CFI, and many other defensive measures adopted in one form or another by all modern operating systems. We combine our deep expertise with swift and detailed support, acting as a trusted advisor and an extension of our customers' security and kernel engineering teams.

Our primary customer base involves companies with products or services that require a higher level of security assurance for Linux than is typically available elsewhere, with a specific focus on the kernel itself. One obvious example is the web hosting industry, particularly in shared hosting, where one webapp compromise or fraudulent customer grants access to the attack surface of the Linux kernel.  A compromise of the kernel is capable of defeating nearly all other security in place, putting the sensitive information of other customers on the same system at risk.

### Marcey: Tell us about Open Source Security’s use of Rust. How are you using it currently and how might that evolve? 

**Spengler**: We are interested in Rust, but are not (yet) using it ourselves in services offered to customers.  That will certainly change given that support for Rust is going to be merged in the upstream Linux kernel, and we believe it will be critical to more widespread adoption.  This is actually what led us to begin supporting (in collaboration with Embecosm) the full-time development of a GCC front-end for Rust last year, which we announced here: https://opensrcsec.com/open_source_security_announces_rust_gcc_funding

The work, being headed by Philip Herron with help from two Google Summer of Code students and a surprising number of members of the Rust community, has accomplished an impressive amount in just its first year. We're so pleased with the progress being made that we're extending and expanding that support for the upcoming year.

### Marcey: What was Open Source Security’s motivation to join the Rust Foundation?

**Spengler**: When we heard about the formation of the Rust Foundation, we wanted to make sure we were involved to help support the broader goals and initiatives of Rust, rather than just the GCC-specific work we're funding. We also wanted to demonstrate that there is both interest and funding for a broader Rust ecosystem that we believe will be crucial to its widespread adoption.

### Marcey: What do you hope the Rust Foundation will accomplish going forward?

**Spengler**: Long-term, we'd like to see the Rust Foundation help break down barriers to Rust adoption, support the entire Rust ecosystem, and help publicize Rust's strengths and successes to a wider audience.

### Marcey: When and how did you personally get involved with Rust itself and how has your involvement evolved?

**Spengler**: I've followed Rust with interest for some time now.  For the past 20 years of grsecurity development, our strategy has always been closing down entire classes of vulnerabilities and avenues of attack, so a language that can accomplish the same for new code is closely aligned with our vision. While I've been critical in the past of mass-rewriting of existing codebases in memory-safe languages as a viable security strategy, I absolutely believe the greatest good can be achieved when the barriers to entry for Rust are broken down and the "mixed-binary" problem mentioned above is resolved. That would provide Rust the equal footing and ease of adoption that will allow it to thrive on its substantial merits. I'm eager to see what's in store for Rust in the future, and I’m happy to play a tiny part in enabling others to pursue work on Rust that will benefit everyone.

To learn more about the Rust Foundation, and how we plan to fulfill some of the goals mentioned here, check out our [website](https://foundation.rust-lang.org), [introductory video](https://www.youtube.com/watch?v=AI4lPN0BqGc) and [recent blog posts](https://foundation.rust-lang.org/posts/), and follow us on [Twitter](https://twitter.com/rust_foundation) and [LinkedIn](https://www.linkedin.com/company/rust-foundation/) to stay up to date.  
