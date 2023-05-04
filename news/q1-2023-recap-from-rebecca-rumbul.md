---
title: Q1 2023 Recap from Rebecca Rumbul
byline:
description: >
  Here’s a look at what the Rust Foundation accomplished in January, February,
  and March of 2023
date: 2023-04-26T12:00:00Z
tags:
  - quarterly updates
  - foundation
index: false
layout: layouts/news.njk
---
<img width="580" height="326" alt="Heading: Q1 2023 Recap &amp; Reflection Sub-heading: from our Executive Director &amp; CEO, Rebecca Rumbul. Headshot of Rebecca Rumbul appears in a circular frame." title="Q1 2023 Recap" src="/img/news/2023-04-26-q1-2023-recap/quarterly-recap-q1.png" />

Last year, I began sharing recaps of the activities, projects, and accomplishments of the Rust Foundation staff at the end of each quarter. Although this post is slightly belated, I am happy to continue the practice of sharing quarterly updates about the Foundation in 2023 with much to report on.&nbsp;

As with all my previous [<u>quarterly recaps</u>](https://foundation.rust-lang.org/tags/quarterly%20updates/), the goal of this post is to provide insight into the areas our team focused on and highlight the many projects our small (but growing!) team brought to completion in the first quarter of 2023. While there will always be room for growth and many areas of need within the Rust ecosystem to address, I am proud of the Foundation team for the quality and breadth of their work in Q1.&nbsp;

If you would like to see a comprehensive overview of Rust Foundation activities and areas of focus last year, I highly recommend downloading our [<u>annual report</u>](https://foundation.rust-lang.org/news/rust-foundation-annual-report-2022/). It will provide valuable context as I delve into our progress during the first three months of 2023.&nbsp;

Please note that <u>this blog only details our completed projects and activities in Q1</u>. A recap of Q2 is forthcoming.&nbsp;

---

## **Staffing & Admin**

Recruitment and staff onboarding occupied much of our administrative focus in Q1 of 2023. We saw a flurry of applications to our two Software Engineer job listings in Q4 — 61 applications across the two positions. Candidate assessment and interviewing took place during January and February, resulting in two new hires on the Foundation Technology Team. In March, [<u>Adam Harvey</u>](https://foundation.rust-lang.org/news/welcoming-software-engineer-adam-harvey-to-the-rust-foundation-team/) started his role as Software Engineer focused on our [<u>Security Initiative</u>](https://foundation.rust-lang.org/news/2022-09-13-rust-foundation-establishes-security-team/). Toward the end of March, we completed our hiring process for a Software Engineer role focused on supporting crates.io (we welcomed&nbsp; [<u>Tobias Bieniek</u>](https://foundation.rust-lang.org/news/welcoming-software-engineer-tobias-bieniek-to-the-rust-foundation-team/) into the role in April). [<u>Walter Pearce</u>](https://foundation.rust-lang.org/news/welcoming-our-new-security-engineer-walter-pearce/) (hired in Q4) started in January as our Security Engineer and together with Adam has already made meaningful contributions to our Security Initiative.

In Q1, we also began working with the Rust Project’s Moderation Team to explore how the Foundation can best support their work, utilizing the services of a contractor to help develop policies, processes, and best practices. Through this process, we have gained more insight into how we can deliver value to the mod team going forward. We also sought counsel from our attorneys about how we can extend legal protection to volunteers in case of a dispute, and we intend to have similar conversations with our insurers.

We also welcomed three “Distinguished Advisors” to the Rust Foundation in Q1. These advisors are people I have consulted with for some time, largely due to their policy-related knowledge in respective areas of open source business, law, and community. We created these unpaid advisor roles to remain transparent about executive counsel received from outside of the Rust Project.&nbsp;

In late March, the Rust Foundation Board of Directors formed a People Committee (composed of Foundation staff, Member Directors, and Rust Project Directors,) which held its first meeting. Key responsibilities of this committee include evaluating my performance as Executive Director and the Rust Foundation overall. This committee is critical, as it will help ensure the board has the necessary skills to govern the Foundation effectively and provide support on staffing matters.

## **Finance & Legal**

In Q1, we got to work on a number of important financial and legal housekeeping tasks including completing and submitting the 1024 form to the IRS and completing and preparing the preparation work for the 990 form for 2022. We also <a target="_blank" rel="noopener" href="https://foundation.rust-lang.org/resources/"><u>published our public filings on our website</u></a> in the form of our 990 form for 2021. As soon as our 2022 form is available, we intend to list it on our website as well.&nbsp;&nbsp;

In Q1, the Rust Foundation team also collaborated with Rust Foundation Project Directors, a Trademark Working Group, and our legal counsel to develop an initial draft of an updated Rust Trademark Policy. In March, we created a plan to share it with the public for feedback during an open consultation period in April.&nbsp;

*Note: We know many members of the community are eager for updates related to the Rust Trademark Policy draft. Please refer to &nbsp;*[*<u>this blog</u>*](https://foundation.rust-lang.org/news/rust-trademark-policy-draft-revision-next-steps/) *from Q2 for the latest information about the feedback review process and the next steps for implementation. A careful review of all feedback is ongoing — we are dedicated to updating and improving upon the initial draft of this policy and we appreciate your patience.&nbsp;*

With the support of Infrastructure Engineer Jan David Nose and Director of Technology Joel Marcey, we also initiated an analysis and forecast of infrastructure costs to identify possible financial risks and mitigation measures.

In Q1, the Rust Foundation had an operating surplus of $79k USD –&nbsp; a review of performance v.s. budget is currently underway to assess the likely full-year outcome.&nbsp;

## **Technology**

Q1 was primarily spent on two strategic technology initiatives - infrastructure efficiency and Rust security.&nbsp;

Over the past three months, we saw two major infrastructure-related developments.&nbsp;

First, 50% of crates.io is now running on Fastly infrastructure with this figure set to reach 95%. Initial results show some bandwidth savings. As a next step, we intend to migrate the more bandwidth-heavy Rust release downloads to Fastly where we will look for significant efficiency increases. We thank Fastly for supporting the Rust Foundation through our [<u>Cloud Compute Program</u>](https://foundation.rust-lang.org/policies/cloud-compute-program/).&nbsp;

Second, we have outlined a collection of infrastructure efficiency strategies and goals for 2023 to understand where our infrastructure is being taxed and what mitigation actions can be taken. We will be looking for further compression and caching opportunities while seeking to improve data visualization so that we can make faster and more proactive decisions.

As mentioned above, our [<u>Security Initiative</u>](https://foundation.rust-lang.org/news/2022-09-13-rust-foundation-establishes-security-team/) began in earnest in Q1 with the arrival of our Security Engineer and two Software Engineers. The Rust Foundation’s Technology Team will work closely with the Rust Project and other ecosystem partners to understand potential threats and work to try to mitigate them. There are four separate threat models being developed focusing on crates.io, the crates ecosystem, the Project infrastructure, and the Rust programming language itself. These assessments have spurred engineering efforts such as an admin console for crates.io and crates ecosystem scanning.&nbsp;

Finally, in Q1 we partnered with GitHub as a [<u>secret scanning integrator</u>](https://github.blog/changelog/2023-01-19-the-crate-io-registry-is-now-a-github-secret-scanning-integrator/) for crates.io and were pleased to see Rust [<u>added</u>](https://foundation.rust-lang.org/news/rust-identified-as-safer-coding-tool-by-nist/) to the [<u>NIST List of Safer Languages</u>](https://foundation.rust-lang.org/news/rust-identified-as-safer-coding-tool-by-nist/) with administrative support from our Director of Technology.

## **Membership**

In Q1, the Rust Foundation was pleased to welcome the following new Corporate Members:

* [<u>Adacore</u>](https://foundation.rust-lang.org/news/member-spotlight-adacore/)
* [<u>HighTec</u>](https://foundation.rust-lang.org/news/member-spotlight-hightec/)
* [<u>Red Badger</u>](https://red-badger.com/)

Additionally, our team built a new strategy for growing our member base in 2023 in order to expand our available resources, grow the foundation, and benefit the communities we serve. This process is ongoing and will continue throughout the year in collaboration with our Board of Directors.&nbsp;

## **Community Grants Program**

We began Q1 on a very positive note by announcing our latest round of [<u>Project Grant</u>](https://foundation.rust-lang.org/grants/project-grants/) recipients. As a reminder, Project Grants are financial awards ranging from $2,500-$15,000 USD, housed under the Rust Foundation’s [<u>Community Grants Program</u>](https://foundation.rust-lang.org/grants/) umbrella. Project Grants fund Rust-focused packages of work carried out by both individuals and teams across the wider community.&nbsp;

## **Communications & Events**

During the first three months of 2023, we continued our work to capture member stories by publishing new [<u>Member Spotlight</u>](https://foundation.rust-lang.org/tags/member%20spotlight/) blogs featuring both existing and new members.

The Rust Foundation also forged several industry partnerships in Q1, which will enable us to conduct collaborative research with other organizations and allow us to share resources with one another. The Rust Foundation is now an&nbsp;[<u>Associate Member</u>](https://foundation.rust-lang.org/news/rust-foundation-joins-open-infrastructure-foundation-as-associate-member/)&nbsp;of the Open Infrastructure Foundation and we collaborated with Chainguard and several other organizations on a [<u>SLSA++-focused study</u>](https://foundation.rust-lang.org/news/new-slsa-survey-reveals-real-world-developer-approaches-to-software-supply-chain-security/).

The Rust Foundation team was present at several Rust community events in Q1 including [<u>State of Open Con</u>](https://stateofopencon.com/) where I spoke on the topic of the role of foundations in securing open source. We were also a primary exhibiting sponsor of [<u>Rust Nation UK</u>](https://www.rustnationuk.com/) where I provided opening remarks. At Rust Nation UK, our team also hosted the official welcome reception and participated in an open forum onstage in London. Our team provided [<u>RustConf 2023</u>](https://rustconf.com/) support, assisting with early-stage communication for the September event, which will continue over the next two quarters.&nbsp;

In Q1, we provided administrative and communications support for the Rust Project for their annual survey – an extension of support from last year.&nbsp;

Finally, as mentioned above, we also kicked off Q1 by announcing our latest round of Community Grants Program Project Grantees on social media and [via our blog](https://foundation.rust-lang.org/news/community-grants-program-awards-announcement-introducing-our-latest-project-grantees/). We intend to continue highlighting the work of our grantees in Q2-4 via our [<u>Grantee Spotlight Series</u>](https://foundation.rust-lang.org/tags/grantee%20spotlight/) which began in Q4 of 2022.&nbsp;

---

Thank you for reading this recap of the Rust Foundation’s completed activities in Q1 of 2023. We’re looking forward to more exciting work to come over the next few months including an update on the Community Grants Program, celebrating the arrival of new members, attending <a target="_blank" rel="noopener" href="https://events.linuxfoundation.org/open-source-summit-north-america/?creative=655069989359&amp;keyword=open%20source%20summit%20north%20america&amp;matchtype=e&amp;network=g&amp;device=c&amp;pi_ad_id=655069989359&amp;utm_term=open%20source%20summit%20north%20america&amp;utm_campaign=&amp;utm_source=adwords&amp;utm_medium=ppc&amp;hsa_acc=8666746580&amp;hsa_cam=19979196448&amp;hsa_grp=148939734478&amp;hsa_ad=655069989359&amp;hsa_src=g&amp;hsa_tgt=kwd-776964337628&amp;hsa_kw=open%20source%20summit%20north%20america&amp;hsa_mt=e&amp;hsa_net=adwords&amp;hsa_ver=3&amp;gclid=CjwKCAjwl6OiBhA2EiwAuUwWZSNktBC2Nh6jQsbRD0NgWbtZZlfc8u9MEwj6FBqOdbqyGVXkXCPaohoCExoQAvD_BwE">Open Source Summit North America</a> (with three members of our team set to speak), and more! I look forward to recapping all of that and much more in my Q2 update. &nbsp;*Find more Rust Foundation Quarterly Updates&nbsp;<a target="_blank" rel="noopener" href="https://foundation.rust-lang.org/tags/quarterly%20updates/"><u>here</u></a>.*

\- Rebecca Rumbul — Executive Director & CEO of the Rust Foundation