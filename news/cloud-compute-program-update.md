---
layout: news
title: Cloud Compute Program Update
description: Alpha testing of Cloud Compute shows positive results
date: 2022-06-09T16:00:00Z
tags:
  - cloud compute
  - programs
---
In November 2022, The Rust Foundation [announced](https://foundation.rust-lang.org/news/2021-11-16-news-announcing-cloud-compute-initiative/) the Cloud Compute Program, an initiative to provide free compute infrastructure for Rust Project maintainers around the world. Through the generous provision of cloud credits from Amazon Web Services (AWS), Google Cloud and Microsoft Azure, the Foundation has worked with the Rust Project [Infrastructure team](https://www.rust-lang.org/governance/teams/infra) and other maintainers to configure the machine images necessary to support the access and usage of these systems for Rust development.

Over the last few months, the cloud infrastructure has been undergoing initial testing. A small test group of Rust Project maintainers have been using the service to do real work in order to both understand its benefits and provide feedback for its improvement.

The cloud compute infrastructure has been used for three primary purposes. One was to verify those that *should* have access *can* access the available machines, whether through a shell or, for example, VS Code and its [remote access extension](https://code.visualstudio.com/docs/remote/remote-overview). Another was to ensure all of the appropriate software is available to begin doing Rust development (e.g., git, all of the compiling prerequisites, etc.). And finally, the infrastructure was used for the actual development and testing of the Rust language, particularly around the compiler and code generation.

The feedback on the service has been positive. Since there was only one machine available for this test phase, the biggest issue was latency. However, that should be alleviated as more machines are spun up globally. There were also cases of users having local machines that were just as or more powerful than what is currently available by the cloud offering. That said, after some initial hiccups around access and having the necessary tooling, the actual development work provided noticeable efficiency wins for those that had less powerful development machines (e.g. i3 based laptops), from 2-3x, or even on the order of 10x, build time improvement for certain workloads. In addition, these efficiency gains allowed users to iterate on changes faster, running test suites locally instead of relying on continuous integration (CI) systems in order to find and fix bugs.

[Jane Losare-Lusby](https://github.com/yaahc), the first tester of the service, said, “*It's been fantastic to finally have access to a beefy machine for rustc builds that I don't have to spend time managing personally. It's 2-3 times faster than my laptop and helps me stay focused on fewer tasks for longer with shorter interruptions from test cycles.*”

[Oğuz Ağcayazı](https://github.com/ouz-a), another tester of the service, said, “*With cloud computing, I don't have to contemplate the meaning of life while waiting for compiler tests to finish, it finishes the task quicker and I can use my computer while tests are running.*”

While there are still some improvements we can make to the default machine images that are provided by this service (e.g., additional software and tooling, better user-data state persistence, targeted documentation on how to accomplish some tasks, etc.), we will soon open the Cloud Compute Program more broadly across the Rust Project. More machines will be brought online, across all three cloud compute platforms, around the world, so that other Rust maintainers can reap the benefits of this service.

We will let those on the various Rust Project governance teams know when they have access, and we look forward to observing how well this program scales.

Stay tuned for even more updates as we continue to expand the Cloud Compute Program offering.
