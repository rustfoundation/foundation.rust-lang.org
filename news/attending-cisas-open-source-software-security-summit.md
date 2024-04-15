---
title: 'Guest Blog: Attending CISA’s Open Source Software Security Summit'
byline: Carol Nichols, crates.io team member
description: >-
  The Rust Foundation sponsored Carol Nichols from the crates.io team to attend a CISA summit on Open Source Software Security, concentrating on package repositories. This is her experience report.
date: 2024-04-15T12:00:00Z
tags:
  - guest blog series
  - security
  - security initiative
  - crates.io
  - rust project
index: false
layout: layouts/news.njk
---

I was honored to be invited to represent the crates.io team and the Rust ecosystem at the U.S. Government's [CISA Summit on Open Source Software Security](https://www.cisa.gov/news-events/news/cisa-announces-new-efforts-help-secure-open-source-ecosystem). It was held March 5-6, 2024, and the discussion focussed on package repositories like crates.io. I'm grateful to the Rust Foundation for sponsoring my travel to the event! I learned a lot and had some great conversations, and I would like to share my experiences with the community.

The summit gathered maintainers of package repositories from different programming language and operating system ecosystems, people representing foundations that support various aspects of open source software, people from large tech companies, and people from the U.S. government. Often, one person would be representing more than one of these areas! Everyone there deeply understood the value of collaborating on open source as well as the challenges that maintainers and users of open source face.

On day 1, there was a keynote by CISA Director Jen Easterly, panel discussions from package repository maintainers, government folks from various agencies' Open Source Program Offices (OSPOs), and breakout discussions on the [Principles for Package Repository Security](https://repos.openssf.org/principles-for-package-repository-security) that the OpenSSF and people from CISA have been working on.

On day 2, we were divided into small groups to work through [a tabletop exercise (available from this CISA blog post)](https://www.cisa.gov/news-events/news/lessons-xz-utils-achieving-more-sustainable-open-source-ecosystem) featuring a hypothetical series of security-related incidents with an open source software component. Imagine Heartbleed, Log4j, and other Very Bad Times that have happened in regards to software security in the last 10 years, but they all happen at once, and you'll get an idea of the proposed scenario! It was super useful to discuss and think through what crates.io and the Rust Foundation would do without the pressure of the events actually happening.

One action item we took away from the exercise was the need for the Foundation to make (and keep up-to-date) a printed-out list of emergency contact information like emails and phone numbers of everyone involved with Rust security, in case of device or email account compromise, to have alternate methods of getting in touch.

Another action item I'm going to take on is making a resource on crates.io for OSS crate authors detailing how the crates.io Team and the Rust Foundation can help if they get a report that their library has a high-severity, high-impact security vulnerability. The Rust Foundation employs experts in security who can help with a fix, and experts in communication who can help with fielding inquiries and publishing updates. Foundation member companies also have vast computing resources and additional people with expertise who would be glad to help in a security crisis that affects the whole community. The people from the US government in our group also discussed the resources they would have at their disposal such as assessing impact and investigating exploitations, and the Rust Foundation can facilitate those collaborations. We should document this sort of information on crates.io now so that crate authors know these resources are available for WHEN a security incident happens.

Overall, the workshop was the start of conversations and collaborations between people from many different areas who all care about helping to improve the security of open source software. Obviously, we didn't solve the immense challenges facing us all, but this is a step in a productive direction. It also highlighted for me how much the [Rust Foundation’s Security Initiative](https://foundation.rust-lang.org/tags/security%20initiative/) has improved the security of the Rust ecosystem– many of the discussions I had involving crates.io’s security posture would have been very different just a few years ago!

Many thanks to CISA for hosting this summit, and I'm looking forward to continuing these discussions and improvements.
