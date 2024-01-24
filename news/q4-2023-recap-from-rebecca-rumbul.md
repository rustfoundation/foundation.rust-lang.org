---
title: Q4 2023 Recap from Rebecca Rumbul
byline: Dr. Rebecca Rumbul - Executive Director & CEO
description: >-
  A review of the Rust Foundation’s activities in October, November, and
  December of 2023.
date: 2024-01-23T12:00:00Z
tags:
  - quarterly updates
  - foundation
index: false
layout: layouts/news.njk
---
After a busy and pivotal year at the Rust Foundation, I’m excited to share the final quarterly recap of Rust Foundation activities, priorities, and accomplishments in 2023.&nbsp;

As always, my intention with this series is to give the Rust community and our collaborators insight into Rust Foundation operations while giving you a detailed picture of how we direct our resources each quarter.&nbsp;

Here’s what the Rust Foundation team focused on in October, November, and December 2023…

## **HR & Administration**

In Q4, each member of the Rust Foundation’s staff received a review of their performance throughout 2023, which included goal-setting for the next 12 months. Results from the reviews were discussed at the November board meeting and helped inform our staffing plans including restructuring needs and expansion strategy.&nbsp;

We look forward to sharing updates on hiring plans soon!

## **Finance & Legal**

In Q4, our Finance and Legal team submitted the 2022 990 form to the IRS, which gathers information about tax-exempt organizations such as ours. Once we receive confirmation of receipt from the IRS, we will publish the form on our [<u>Resources page</u>](https://foundation.rust-lang.org/resources/). We also transferred $1.5m into interest-bearing bonds and completed and shared a budget for 2024 with the board for discussion at our December meeting. We look forward to learning more from Rust Project leadership about how we can serve Project priorities with earmarked funds in the coming weeks.&nbsp;

For a recap of our financial activities over the past year, please refer to pages 10-13 in our [<u>2023 Annual Report</u>](https://foundation.rust-lang.org/static/publications/annual-reports/annual-report-2023.pdf).

## **Membership**

In Q4, we were pleased to formally announce JetBrains’ membership with the Rust Foundation. We also created and announced a new Associate Membership tier and look forward to welcoming new organisations to this category in 2024.

If you work for or are otherwise connected to organisation that might be interested in becoming a member of the Rust Foundation, do not hesitate to get in touch with me at [<u>rebeccarumbul@rustfoundation.org</u>](mailto:rebeccarumbul@rustfoundation.org). The team would be delighted to walk prospective members through our benefits, also summarised in&nbsp;<a target="_blank" href="https://foundation.rust-lang.org/static/membership-overview-deck.pdf"><u>this</u></a>&nbsp;deck.

## **Technology & Infrastructure**

In Q4, building on the success of [<u>Painter</u>](https://github.com/rustfoundation/painter), the Technology Team released our second open source tool, [<u>Typomania</u>](https://github.com/rustfoundation/Typomania). The Typomania project is a port to Rust of typogard, originally by a team led by Matthew Taylor at the University of Kansas and published alongside the Defending Against Package Typosquatting paper, and [<u>adapted</u>](https://github.com/dangardner/typogard) by Dan Gardner at AWS for crates.io. Rather than being hard-coded to a specific registry, Typomania provides the same set of primitives that typogard uses to detect potential typosquatting as a reusable library that can be adapted to any registry by implementing the traits provided in this crate. Typomania is now integrated directly into the crates.io publishing pipeline

In Q4, Typomania caught three potentially typo-squatting crates, and Sandpit (soon to be open-sourced) caught six malicious crates. We look forward to these tools being further developed in the coming months.&nbsp;

Over the past three months, the Rust Foundation also began coordinating with other stakeholders and the Rust Project to improve supply chain security in the Rust ecosystem, starting with ensuring that Rust releases and crates can be verified in a secure, low-overhead manner. The Technology Team shared a [<u>statement</u>](https://hackmd.io/@LawnGnome/HylJ-4LUT) that proposes how we could unite with the Rust Project over a signing strategy to help make this a reality.

The Technology Team continued to make progress on our Security Initiative in Q4. The second of four proposed threat models has been [<u>published</u>](https://docs.google.com/document/d/10Qlf8lk7VbpWhA0wHqJj4syYuUVr8rkGVM-k2qkb0QE/) – it is geared towards the infrastructure that supports the Rust Project. This model will help guide our proposed security and infrastructure work for 2024.

In Q4, we also saw Fastly begin to serve 75% of Rust releases in addition to 95% of crates. After a successful proof of concept, we moved forward with Datadog as our infrastructure visualization platform. There is now a public Datadog [<u>dashboard</u>](https://p.datadoghq.com/sb/3a172e20-e9e1-11ed-80e3-da7ad0900002-973f4c1011257befa8598303217bfe3a) that shows the number of crates.io download requests for a given cargo version. The data clearly shows the number of crate download requests increasing with every new cargo version release. For the year, we have reduced AWS’ bandwidth burden by well more than our goal of 25% and we have also reduced what we call our cost-per-activity (CPA) as activity has grown steadily throughout the year, but costs have remained generally stable.&nbsp;

Finally, Rust Specification work officially began in Q4 with Joel Marcey (Director of Technology at the Rust Foundation) serving as Editor. The Rust Specification Team within the Rust Project is in the process of writing a sample specification chapter to present to stakeholders to get an idea of the specification’s structure and potential tooling.

## Communications, Marketing & Events

In Q4, our communications and marketing efforts were focused around creating and publishing high-quality content about Rust Foundation milestones, and sharing information about several new and developing areas of focus for the Rust Foundation.&nbsp;

### **News & Content:**

In Q4, we announced [<u>JetBrains</u>](https://foundation.rust-lang.org/news/member-spotlight-jetbrains/) as our newest Silver Member organisation. Although we will continue to share case studies from our members in 2024, the “member spotlight” style of announcement will be reserved for new Platinum members going forward with new Silver and Gold Members announced through joint release. In October, we shared the new template for Silver and Gold member announcements with the board and received approval to proceed. We are excited to utilize this new format for better organisation and more visible public announcements of gold and silver members.&nbsp;

We were also pleased to [<u>announce</u>](https://foundation.rust-l) the Rust Foundation’s three new Project Directors in Q4: Santiago Pastorino, Scott McMurray, and Jakob Degan. Our new Project Directors were selected through a newly developed election process which is described in [<u>this</u>](https://blog.rust-lang.org/2023/08/30/electing-new-project-directors.html) official Rust language blog from August.&nbsp;

### **Additionally in Q4, we announced:**

* The new [<u>Rust Foundation Associate Member tier</u>](https://foundation.rust-lang.org/news/inside-the-rust-foundation-s-associate-membership-tier/)&nbsp;
* Our intention to develop a [<u>Rust Foundation training and certification program</u>](https://foundation.rust-lang.org/news/the-rust-foundation-to-develop-training-and-certification-program/)\*
* The receipt of [<u>second-year funding</u>](https://foundation.rust-lang.org/news/alpha-omega-to-continue-support-of-rust-foundation-security-initiative-in-2024/) for our Security Initiative via OpenSSF’s Alpha-Omega project
* Upcoming Rust Foundation plans related to RustConf 2024 (see “Events”)&nbsp;

### **\* A note on Rust Foundation training communications:**

While our plans for a Rust Foundation training and certification program are still in an early stage, we wanted to share a memo about our upcoming plans publicly as early as possible in Q4. Our goal in sharing this note was to transparently disclose our intentions and spark important discussions in service of the program.&nbsp;

We received feedback from some members of the Rust Project in Zulip that they would like the opportunity to lend their perspectives – and that members could have been more proactively included before seeing our public memo. While we sought approval for this work through the board and looped the public in as early as possible, our team respects that additional touchpoints would have been appreciated earlier. We are excited to proceed with this work by holding two training-focused listening sessions in Q1: one session will be available to Rust Foundation member organisations and the other will be available to members of the Rust Project – particularly those who currently offer Rust education materials. We have not identified a date for these listening sessions but will be following up with firm plans very soon.&nbsp;

### **Publications & Media**

In Q4, Gracie Gregory (Director of Communications & Marketing) oversaw the creation of our Annual Report for 2023 which is available for download [<u>here</u>](https://foundation.rust-lang.org/static/publications/annual-reports/annual-report-2023.pdf). She also began working with Joel on our second Security Initiative Report, which will be released in the coming weeks.&nbsp;

Q4 was also the Rust Foundation’s busiest and most fruitful period for our new website to date. Gracie continued her collaboration with a contracted web designer and a web developer to begin migrating the old website over to a new system which will greatly improve our teams’ user experience upon launch. With the majority of the website designed and built, the last major task is to finalize web copy in collaboration with the rest of our senior management team. Gracie expects to be able to launch the new Rust Foundation website in Q1 2024.&nbsp;

### **Events:**

In Q4, I was invited to attend Open Source Summit Japan where I connected with members of the global open source community and supported OpenSSF by attending its co-located OpenSSF Day event. Other events attended by the Rust Foundation staff team include:

* [<u>PackagingCon</u>](https://packaging-con.org/) - An event dedicated to packaging management systems in Berlin, Germany (October)
* [<u>Tectonics</u>](https://tectonics.memorysafety.org/) – A memory-safety-focused event in San Francisco, CA (November)
* [<u>Open Core Summit</u>](https://opencoresummit.com/about-ocs/) – An event dedicated to discussions about commercial open source in San Francisco, CA (December)

### **RustConf 2024**

Towards the end of Q3, the Rust Foundation board approved the Rust Foundation staff team’s proposal to allocate more funding and staff resources towards playing a larger role in planning and managing RustConf in 2024.&nbsp;

After receiving a positive reaction to this news from our Project Directors, the Leadership Council, and a segment of the Rust Project via Zulip, our team began researching venues and dates. We secured a contract with an excellent venue in Montreal from September 10-13. We are currently in the process of solidifying our sponsorship offerings and will share an update with past and prospective sponsors in Q1. We will also begin building the 2024 website and intend to open the Call For Proposals (CFP) very soon. Before this can happen, however, we owe several groups updates on the RustConf Program Committee — the group that selects talks from the CFP to appear on the event program. We intend for the talk selection process to be more transparent and allow for a greater balance of voices making these important decisions going forward. Our team will share an update about the 2024 Program Committee process soon and, in the meantime, we plan to document our plans publicly and have discussions with the Leadership Council.&nbsp;

Please fill out [<u>this form</u>](https://docs.google.com/forms/d/e/1FAIpQLSfAIk1bcDlt5dDQtC19gifTJnjdka0gYcr7vKE9ncBN1eXPgw/viewform?usp=sf_link) if you would like to receive general attendee/speaker updates about RustConf 2024, if your organisation would like to express interest in sponsoring RustConf 2024, or if you have sponsored RustConf in the past and would like to share your perspectives to help inform our offerings. Please stay tuned for a more public announcement on RustConf!

### **Communications & Marketing Support**

While we made great strides towards a comprehensive marcomm strategy over the past year, more support in this area is needed. As such, we spent Q4 developing plans to expand our marketing team in 2024.&nbsp;

The Marketing Specialist role is now live and open for applications through February 7, 2024. If you are an experienced marketing professional with a passion for tech communications and event project management, we encourage you to [<u>review the position and apply</u>](https://app.beapplied.com/apply/hy66g5t8ro) if it sounds right for you!

The Marketing Specialist will be the first associate-level hire on the Foundation’s marketing and communications team. This person will contribute substantially to the output of high-quality communications we hope to achieve in 2024 and we look forward to introducing them soon!

## **Community Grants Program**&nbsp;

In Q4, we conducted a thorough assessment of the Community Grants Program in 2023. Here is a recap of our key observations for the program to date:&nbsp;

* Fellowships delivered the most impact for the Rust Project out of all grant categories.&nbsp;
* Our funding for grants in 2023 could not meet community demand – many applicants could not be selected due to high application rates.
* Our “Mentored Fellowship” roles introduced in 2023 are showing promise, as they directly support Rust Project teams in need.
* We faced difficulties in demonstrating the value of our program to prospective sponsors, in part because Project Grant applicants have historically selected their own areas of focus, making it challenging to align all Project Grants with Rust Project priorities.

Despite the challenges we faced over the past year, the Community Grants Program aligns with our mission and a continued Rust community demand remains.&nbsp;

### **For these reasons, we will continue the program in 2024 with some important changes…**

* Expanded “Mentored Fellowship” positions to increase the pipeline of contributors – in consultation with Rust Project leadership.&nbsp;
* The Rust Project Leadership Council will drive the process of identifying high-priority pieces of work for Project Grants with the community.
* We will open a rolling Project Grant application process for prospective grantees to apply to carry out these agreed-upon priorities.
* We will work with the Leadership Council to identify applicants to receive the Project Grant associated with each priority

---

That concludes the final Rust Foundation 2023 quarterly recap! Our team is looking forward to continuing the hard work outlined in this post in 2024. We’re also excited to tackle many new areas of focus in the months ahead.&nbsp;

To everyone who supported the Rust Foundation staff team in 2023, collaborated with us, or shared your perspectives: Thank you.&nbsp;

If you have any questions about the contents of this report, don’t hesitate to contact us at <u>contact@rustfoundation.org</u>. If you are interested in joining the Rust Foundation as a member, please email us at <u>membership@rustfoundation.org</u>.&nbsp;&nbsp;

You can find past Rust Foundation Quarterly Updates [<u>here</u>](https://foundation.rust-lang.org/tags/quarterly%20updates/).