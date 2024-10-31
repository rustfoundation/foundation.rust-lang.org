---
title: Q3 2024 Recap from Rebecca Rumbul
byline: Rust Foundation Team
description: >-
  A review of the Rust Foundation's activities in July, August, and September of
  2024.
date: 2024-10-31T12:00:00Z
tags:
  - 'quarterly updates '
  - foundation
index: false
layout: layouts/news.njk
---
I’m pleased to have a number of exciting achievements from the Foundation and staff team to reflect on in this quarterly recap for July, August, and September of 2024. Thank you for your patience with us in assembling this recap – following the flurry of activity in Q3, many members of our team took time off to regroup which delayed this post.

## Summary

During the third quarter of 2024, the Rust Foundation achieved several significant milestones. The Foundation convened the first meeting of the [<u>Safety Critical Consortium</u>](https://foundation.rust-lang.org/news/announcing-the-safety-critical-rust-consortium/), establishing the scope and interest areas for this important initiative. Four new members joined the Foundation, and substantial progress was made in software supply chain engineering, including advancements in crate provenance tracking and agreement on using The Update Framework (TUF) for crate signing and mirroring.

The Foundation's growing influence was reflected in 15 organic media mentions across global industry outlets. Staff actively engaged with the community through speaking engagements at significant events, including [RustConf](https://rustconf.com/),[<u>Rust Global</u>](https://rustconf.com/programs/#rust_global), [<u>Open Source Congress Beijing</u>](https://www.opensourcecongress.org/), and [<u>Open Source Summit Vienna</u>](https://osseu2024.sched.com/).

Notable achievements included:

* Successfully onboarding a new Infrastructure Engineer,
* Awarding 19 new fellowships for 2024-25, and
* The continued progression of the Rust Specification work.

## Q3 Goals

During the July 2024 Board Meeting, we set several ambitious goals for the third quarter. These included awarding and onboarding 2024 Fellows, organizing RustConf and associated events, including Rust Global, holding an in-person board meeting, defining the C++/Rust interop strategy, and implementing Foundation-driven malicious crate detection tooling in GCP. Substantial staff time was devoted to RustConf 2024 organization and Community Grants Fellowship Awards.

## HR & Administration

In the third quarter, we saw good progress in HR and administration. Marco Ieni joined as Infrastructure Engineer on July 15, substantially impacting the Infrastructure Team's capacity. Plans were made for a week-long staff offsite in Iceland, focusing on team cohesion and future planning. The Board's People Committee began preparations for annual reviews, including the Executive Director's evaluation process.

## Technology & Infrastructure

The Foundation made substantial progress across multiple technical initiatives in Q3. The [<u>Safety-Critical Rust Consortium</u>](https://foundation.rust-lang.org/news/announcing-the-safety-critical-rust-consortium/) held its first meeting in Montreal, attracting over 30 participants interested in Rust's safety-critical applications. The meeting established subcommittees for coding guidelines, tooling, and education, with the next meeting scheduled at Rust Nation in early 2025.

A significant breakthrough occurred at RustConf 2024 when Foundation and Rust Project members agreed to implement [<u>The Update Framework (TUF)</u>](https://theupdateframework.io/) for crate signing and mirroring, replacing the original [<u>PKI RFC</u>](https://github.com/rust-lang/rfcs/pull/3579) proposal. The team is addressing technical challenges, particularly implementing [<u>TAP16</u>](https://github.com/theupdateframework/taps/blob/master/tap16.md) to reduce metadata payload sizes using Merkle trees.

The C++/Rust Interop strategy is nearing completion, with plans to join the INCITS C++ specification committee to enhance collaboration between languages. Security infrastructure advanced with Walter Pearce and Adam Harvey leading the migration to Google Cloud Platform (GCP), implementing regular security scans using tools like Painter and Typomania, with results stored in a neo4J database.

Tobias Bieniek led substantial improvements to crates.io, including:

* Implementation of the [<u>crate deletion RFC</u>](https://github.com/rust-lang/rfcs/pull/3660)
* [Email notifications](https://github.com/rust-lang/crates.io/pull/9341) for new crate versions
* Migration of download archive data to static.crates.io
* Move to CrunchyBridge database
* RSS feeds for crate publications
* Updated install instructions for binary crates

Tobias has provided an update on the progress of crates.io's development on the [<u>Rust Blog</u>](https://blog.rust-lang.org/2024/07/29/crates-io-development-update.html).

Infrastructure updates accelerated under Marco Ieni's leadership, including [<u>updating Terraform providers</u>](https://github.com/rust-lang/simpleinfra/issues/437), implementing crate and release backups, and completing server cataloging. The Foundation renewed its DataDog partnership for infrastructure monitoring.

Specification work progressed with Connor Horman joining as a contractor, focusing on migrating and reformatting the Reference documentation.

Walter Pearce presented ["Dude, Where's My C?"](https://rustconf.com/programs/#1083) at our Rust Global event at RustConf. Using [<u>Painter</u>](https://github.com/rustfoundation/painter) data, this talk discussed the statistics and implications of externally-linked code across the crates ecosystem.

Adam Harvey continued his work on project sustainability and gave a Python-specific version of his [<u>Quantifying Nebraska talk</u>](https://www.youtube.com/watch?v=QMHpy_mcx0Q) at [<u>North Bay Python</u>](https://pretalx.northbaypython.org/nbpy-2024/talk/9EXJ7T/).

## Communications, Marketing & Events

In Q3, our communications and marketing efforts were largely focused on planning and executing RustConf 2024, which took place from September 10 to 13 in Montreal. We were pleased with the event's results and look forward to hosting it again in 2025.

Major announcements included a [<u>$100,000 donation from LambdaClass</u>](https://foundation.rust-lang.org/news/lambdaclass-donates-100k-to-the-rust-foundation/) and the publication of [<u>a Rust Foundation report on our technical activities</u>](https://foundation.rust-lang.org/news/latest-rust-foundation-report-details-technical-accomplishments/). This "Rust Foundation Technical Report" details the accomplishments and focus areas of our Technology Team, led by Joel Marcey, in concert with our many collaborators in the Rust community. This report series expands upon our "Security Initiative Reports" to include updates and notes on all technical initiatives at the Rust Foundation.

The Foundation also completed its website overhaul for its upcoming launch and received approximately 15 media mentions across industry outlets. Staff participated in key events, including [<u>RustConf</u>](https://rustconf.com/),[<u>Rust Global</u>](https://rustconf.com/programs/#rust_global),[<u>Open Source Congress Beijing</u>](https://www.opensourcecongress.org/), and[<u>Open Source Summit Vienna</u>](https://osseu2024.sched.com/).

## Community Grants Program

The Program awarded and onboarded the [<u>2024 Fellowship cohort,</u>](https://foundation.rust-lang.org/news/announcing-the-rust-foundation-s-2024-fellows/) consisting of 3 Community Fellows, 6 Project Goal Fellows, and 10 Project Team Fellows. Two event support grants and four travel grants for Rust Project team members were also awarded and distributed.

---

As always, I hope that this information gives our community insight into where the Foundation’s resources and efforts were channeled over the past several months. If you have any questions about the contents of this report, don’t hesitate to contact us at contact@rustfoundation.org. If you are interested in joining the Rust Foundation as a member, please email us at [membership@rustfoundation.org](mailto:membership@rustfoundation.org).

You can find past Rust Foundation Quarterly Updates [here](https://foundation.rust-lang.org/tags/quarterly%20updates/).

&nbsp;