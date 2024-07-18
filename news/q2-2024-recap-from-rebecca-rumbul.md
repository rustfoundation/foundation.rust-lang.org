---
title: Q2 2024 Recap from Rebecca Rumbul
byline: Rebecca Rumbul
description: A review of the Rust Foundation’s activities in April, May, and June of 2024.
date: 2024-05-07T12:00:00Z
tags:
  - quarterly updates
  - foundation
index: false
layout: layouts/news.njk
---
The Rust Foundation staff worked hard in Q2 of 2024 on a number of exciting packages of work. I'm pleased to share this recap of our team's areas of focus over the past three months.

## Summary

During the first quarter of 2024, the Rust Foundation celebrated numerous achievements and made significant strides in its program of work. One of the highlights was the agreement and launch of the new [Safety Critical Consortium](https://foundation.rust-lang.org/news/announcing-the-safety-critical-rust-consortium/), marking a pivotal step in advancing Rust's application in safety-critical industries. The Foundation also welcomed three new members and successfully developed tooling that identified and mitigated 28 potentially malicious crates. The Rust Foundation was organically mentioned in 27 news stories across global industry media, reflecting growing interest and recognition of its initiatives.

The Rust Foundation team was present at various events in the Rust ecosystem. Staff attended and delivered speeches at the [Open Source Summit North America](https://events.linuxfoundation.org/open-source-summit-north-america/), [RustNL](https://2024.rustnl.org/), RSA, Linux Executive Security Consortium, [AWS Re:Inforce](https://reinforce.awsevents.com/), and the [SOSS EU Policy Summit](https://events.linuxfoundation.org/soss-policy-summit-europe/). In addition, the Foundation successfully recruited three new staff members, with two already onboarded, further strengthening its team. The ongoing development of the Quarterly CGP Fellowship reviews and the Fellowship grant strategy for 2024, along with significant progress in the Rust Specification work, underscore the Foundation's commitment to fostering a robust Rust ecosystem. The Rust Foundation also became a formal founding member of the [OSS Stewards EU CRA Standards](https://foundation.rust-lang.org/news/rust-foundation-joins-cra-compliance-collaboration/) partnership, reinforcing its role in shaping the future of open-source software security standards.

During the second quarter, the RustConf Call for Proposals (CFP) closed. We also announced of [speakers](https://rustconf.com/speakers/), began securing [sponsors](https://rustconf.com/our-sponsors/), and set the stage for a successful conference.

Substantial staff time in the second quarter was devoted to the recruitment and onboarding of new staff, as well as the organization of RustConf logistics and the RustConf CFP. Progress continued on the website overhaul. We are now aiming for a launch in the third quarter, which promises to enhance the accessibility and engagement of the Rust Foundation's online content. This new timeline reflects a delay in our former goal of a Q2 launch due to constraints on staff time.

## Q2 Goals

During the April 2024 Board Meeting, we set forth several ambitious goals for the second quarter. These included completing the recruitment and onboarding of three new staff members, opening the 2024 Fellowship applications, and attending key industry events such as the OSS Summit North America, DAC San Francisco, RustNL, and the SOSS EU in Brussels.

The Foundation also aimed to organize a safety-critical industry forum, make further progress on training program content development, and launch its new website, although the latter two have been delayed.

## HR & Administration

The second quarter saw significant progress in HR and administration. [Christina Gorton](https://foundation.rust-lang.org/news/welcoming-marketing-program-manager-christina-gorton-to-the-rust-foundation-team/) joined the Foundation as the new Marketing Program Manager on April 22 and has already made a notable impact. She is actively supporting the delivery of RustConf, scaling marketing and membership activities, and initiating the development of a training program. The Foundation also completed the recruitment process for two other key roles: an Infrastructure Engineer to support JD Nose and an Interoperability Engineer to lead the Rust/C++ interop initiative. [Jon Bauman](https://foundation.rust-lang.org/news/welcoming-rust-c-interoperability-engineer-jon-bauman-to-the-rust-foundation-team/), who started on May 31, has begun orienting himself in the Rust/C++ landscape and is set to present a strategy proposal in the coming weeks. [Marco Ieni](https://foundation.rust-lang.org/news/welcoming-infrastructure-engineer-marco-ieni-to-the-rust-foundation-team/), joined the Rust Foundation on July 15 as its second Infrastructure Engineer, reporting to JD. Marco will provide much-needed support to the Rust project and its infrastructure.

## Finance & Legal

The Foundation transitioned its financial management and reporting systems from QuickBooks to Xero, introducing more granular financial reporting and tracking. This shift aims to better reflect how resources are allocated in support of the [Rust Project](https://www.rust-lang.org/). The Foundation completed the reporting for its 2023 990 form submission and continues to invest surplus funds into interest-bearing certificates of deposit to maximize returns. A review of performance against the 2023 budget was conducted, showing a year-to-date effective operating surplus of $139,600.

## Membership

In Q2, we were pleased to welcome several new members to the Rust Foundation. Wyeworks LLC, Accelerant Limited, and Zed Industries joined as new Silver Members and new Associate Members: Stichting Rust Nederland (RustNL) and the Brazilian Pontifícia Universidade Católica do Paraná.

If you work for or are otherwise connected to organisation that might be interested in becoming a member of the Rust Foundation, do not hesitate to get in touch with me at [membership@rustfoundation.org](https://foundation.rust-lang.org/news/q1-2024-recap-from-rebecca-rumbul/). The team would be delighted to walk any prospective member through our benefits, which are also summarised in [this](https://foundation.rust-lang.org/static/membership-overview-deck.pdf) deck.

## Technology & Infrastructure

The Rust Foundation's Technology team made significant progress in the second quarter. [Jon Bauman](https://foundation.rust-lang.org/news/welcoming-rust-c-interoperability-engineer-jon-bauman-to-the-rust-foundation-team/), the new software engineer lead, has started planning a proposed Rust/C++ interop strategy after meeting with stakeholders. The team also hired a new infrastructure engineer to support the growing needs of the Foundation and the Rust Project, with the name of the engineer to be announced in July.

A major highlight was the launch of the [Rust Safety Critical Consortium](https://foundation.rust-lang.org/news/announcing-the-safety-critical-rust-consortium/), which attracted nine founding members and substantial interest from over twenty more organizations eager to join or collaborate. At [RustConf](https://rustconf.com/), the consortium aims to define its charter and goals, and establish a mechanism to efficiently add new members.

The Foundation's focus on security has intensified following the XZ backdoor vulnerability. Efforts are now geared towards supply chain security, with initiatives such as provenance tracking to verify crate associations and the implementation of quarantine measures for malicious crates. Walter has made substantial improvements to Painter, enhancing its capabilities in unsafe statistics, call graph pruning, FFI boundary mapping, and CVE categorization. The security infrastructure is being migrated to Google Cloud Platform (GCP), enabling regular security scans and improved result analysis.

Progress on the [Public Key Infrastructure (PKI)](https://github.com/rust-lang/rfcs/pull/3579) RFC has encountered delays, with ongoing debates about the best approach for signing across the project. The Foundation is exploring the potential adoption of [The Update Framework (TUF)](https://theupdateframework.io/) instead of PKI, which would necessitate revising the current RFC.

Fastly continues to provide the majority of bandwidth for Rust releases and crates, supported by AWS. The Foundation has applied for AWS credits for 2025, demonstrating efficient use of resources. Collaboration with Microsoft has secured an additional $10,000 in Azure credits for the Cloud Compute Program.

Significant improvements have been made to [crates.io](http://crates.io), including the migration of the test suite to async tests, optimization of the database through data export to S3, and implementation of token expiry notifications to ensure continuity of workflows. Joel has been appointed as the team lead for the Rust specification, with plans to hire a contractor to accelerate the writing and content development.

The Foundation renewed its subscription to DataDog for infrastructure visualization and analysis and downgraded its Papertrail subscription, resulting in cost savings. Staff participated in various events, including the[Open Source Summit North America](https://events.linuxfoundation.org/open-source-summit-north-america/) and the [RSA conference](https://www.rsaconference.com/), highlighting the Foundation's active role in the open-source community.

## Community Grants Program

The [Community Grants Program](https://foundation.rust-lang.org/grants/) continued to engage with the 2023 cohort of Fellows and developed an initial plan for the 2024 Fellowship program which is now open for applications and features updates such as increased monthly stipend and a combined travel, training, and equipment budget. More information on our open Fellowship application [here](https://foundation.rust-lang.org/grants/fellowships/). Four Event Support Grants were awarded in Q2, supporting meet-ups in India, Turkey, and Kenya, as well as the virtual meet-ups of the Games Dev group. The feedback from Fellows has been positive, although some have expressed concerns about burnout. The Foundation has assured Fellows that they can take time off without pressure, maintaining their support and funding.

## Communications, Marketing & Events

In the second quarter, the Rust Foundation focused on onboarding the new [Marketing Program Manager, Christina Gorton](https://foundation.rust-lang.org/news/welcoming-marketing-program-manager-christina-gorton-to-the-rust-foundation-team/), advancing [RustConf](https://rustconf.com/)planning, and developing the upcoming website which has unfortunately been further delayed, though we now plan to release it in Q3. The Foundation also announced several collaborations and developments, including a[$1 million donation from Microsoft](https://foundation.rust-lang.org/news/1m-microsoft-donation-to-fund-key-rust-foundation-project-priorities/)and the launch of the [Safety-Critical Rust Consortium](https://foundation.rust-lang.org/news/announcing-the-safety-critical-rust-consortium/).

The Foundation's communications efforts resulted in increased media coverage, with 27 mentions across industry outlets. Highlights included articles in [The New Stack](https://thenewstack.io/rust-the-future-of-fail-safe-software-development/) and [TechCrunch](https://techcrunch.com/2024/04/02/open-source-foundations-unite-on-common-standards-for-eus-cybersecurity-resilience-act/).

### RustConf 2024

Planning for [RustConf 2024](https://rustconf.com/) reached several critical milestones, including closing the call-for-talk-proposals and opening [registration](https://www.eventbrite.com/e/rustconf-2024-tickets-865842106047?aff=oddtdtcreator) for RustConf, Rust Global, and [the UnConference](https://www.eventbrite.com/e/rustconf-2024-post-conference-unconference-tickets-923376803877). The Foundation secured sponsorships from major organizations, including Silver Member [Devolutions](https://devolutions.net/) as a Diamond sponsor. The event promises to be a significant gathering for the Rust community, with a range of talks and activities planned.

For more information and to register, visit the [RustConf website](https://rustconf.com/).

---

As always, I hope that this information gives our community insight into where the Foundation’s resources and efforts were channeled over the past several months. If you have any questions about the contents of this report, don’t hesitate to contact us at contact@rustfoundation.org. If you are interested in joining the Rust Foundation as a member, please email us at [membership@rustfoundation.org](mailto:membership@rustfoundation.org). You can find past Rust Foundation Quarterly Updates [here](https://foundation.rust-lang.org/tags/quarterly%20updates/).

&nbsp;
