---
title: Q1 2024 Recap from Rebecca Rumbul
byline: Rebecca Rumbul, Rust Foundation Executive Director & CEO
description: >-
  A review of the Rust Foundation’s activities in January, February, and March
  of 2024.
date: 2024-04-25T12:00:00Z
tags:
  - quarterly updates
  - foundation
index: false
layout: layouts/news.njk
---
It has been a busy start to 2024 here at the Rust Foundation! During the first quarter of 2024, our team has delivered a successful program of work with a number of achievements to celebrate. I’m pleased to report on the staff team’s areas of focus and points of progress during January, February, and March 2024.

As always, I hope that this information gives our community insight into where the Foundation’s resources and efforts were channeled over the past several months

## **HR & Administration**

We kicked off 2024 with a reinvigorated emphasis on supporting global Rust community events and meetups – in particular, connecting with user groups, meet-ups, and learning communities, and proactively developing new relationships with corporate adopters and users. In early Q1, a part-time Global Rust Coordinator started at the Foundation and is helping us develop and support Rust events all over the world, champion diversity, and support better representation and engagement from under-represented communities.

During Q1, we conducted a recruitment exercise for a marketing support role. We are thrilled to have found a new Marketing Program Manager who joined us on April 22. Having additional support in mar-comms will allow us to scale our current programs and efforts, improve our rate of communication with both members and the community, and develop new initiatives. The successful candidate’s background encompasses developer relations as well as marketing and communications, and we felt that their skillset was an excellent fit for our role. Announcement to come!

Using the additional funding that arrived towards the end of Q4, we also advertised for two additional roles: a second full-time engineer to support Rust’s Infrastructure team, and a pivotal role to lead our new initiative focused on improving the interop experience between C++ and Rust. These roles have now closed to new applicants and the selection process has begun. We hope to make offers in the coming weeks, and onboard both engineers over the coming months.

Andrew Wafaa’s two year term as Silver Member Representative came to an end in February, and as such we conducted an election for a new representative. We welcomed our new Silver Member Representative to the Board in February: Alexandru Radovici.

## **Finance & Legal**

In Q1, we accomplished several key financial and legal tasks with oversight from Paul Lenz, Director of Finance & Funding, and Abi Broom, Operations Manager.

In addition to transitioning our financial management and reporting systems from Quickbooks to Xero, completing the IRS reporting for our 2023 form 990 submission, and conducting a review of performance against budget for 2023 (shared with the board), we introduced more granular financial reporting and tracking to better reflect how the resources of the Foundation are spent in support of the Project.

In Q1, the Rust Foundation also carried out funding allocation work in response to the generous donations we received in late 2023 from both Google and Microsoft. The Foundation has been in close collaboration over the past three months with our Project Directors to develop a plan for Microsoft’s unrestricted donation of $1M in Q4 of 2023, as $325k has been earmarked to fund Rust Project priorities. We look forward to sharing a blog in the coming weeks with more details.

We ended 2023 with an operating surplus of $139.6k, which has been invested into interest-bearing certificates of deposit on a rolling basis to maximise returns. The rate of surplus accrual will reduce as we hire new team members into the open positions described above.

&nbsp;

## **Membership**

In Q1, the Foundation gained three new Silver Members: Trace Machina, Veecle, and Devolutions and two Associate Members: OpenUK and the Institute of Software Chinese Academy of Sciences. Associate Members are non-profit organisations, open source foundations, government entities, and not-for-profit educational institutions, which pay no fees but bring high profile alignment with the Rust Foundation’s mission.

A program of membership acquisition is ongoing, which includes identifying high-priority membership targets and connections to/outreach methods for those targets, and engaging with those targets about Rust Foundation membership. Our expectation is that these efforts will ramp up in Q2.

If you work for or are otherwise connected to organisation that might be interested in becoming a member of the Rust Foundation, do not hesitate to get in touch with me at [membership@rustfoundation.org](). The team would be delighted to walk any prospective member through our benefits, which are also summarised in [this](https://foundation.rust-lang.org/static/membership-overview-deck.pdf) deck.

## **Technology & Infrastructure**

Also in Q1, the Foundation continued coordinating with the Rust Project and other stakeholders to address supply chain security needs in the Rust ecosystem.

Our Technology Team, led by Director of Technology Joel Marcey, released the [first](https://github.com/rust-lang/rfcs/pull/3579) of a series of expected RFCs associated with an artifact signing strategy. This RFC covers having a base PKI and CA for the Project, and the initial model for storing and accessing said keys utilizing a quorum model for ownership. A followup to this RFC around crate-signing and mirroring is being drafted. The Zulip channel for this discussion is [\#tbd-signing](https://rust-lang.zulipchat.com/#narrow/stream/417663-tbd-signing/). Our Technology Team is pleased by this development, as it is a big milestone for Rust and the result of coordination between members of the Project and the Foundation.

Security Engineer Walter Pearce has completed all four of the promised security threat models - [Infrastructure](https://docs.google.com/document/d/10Qlf8lk7VbpWhA0wHqJj4syYuUVr8rkGVM-k2qkb0QE/), [crates ecosystem](https://drive.google.com/file/d/1YxpJ0W5eqat2Y3ZfbdwKm_AoNhX3hIj_/), [crates.io](https://docs.google.com/document/d/1krEL8zccid44ojS2vqxH4HRCD-bPzC7tLfcDhc5QekI/), [Rust Project](https://docs.google.com/document/d/1kpUUYekiiZRARk_EDQ7merBLmwp301yCE28MkQH-x8k/). These threat models highlight potential areas where malicious actors can strike and are being used in discussions with Security Initiative stakeholders as well as guiding various pieces of work around Rust security.

Sandpit (our tool to be open-sourced later this year that scans available crates to try to detect malicious crates based on available heuristics,) was deployed to production on Google Cloud Platform (GCP) in Q1 and is now running at a regular cadence. Between Sandpit, [Typomania](https://github.com/rustfoundation/typomania), and associated Foundation-developed tools, nine (9) malicious crates have been detected and resolved (e.g., via yanking).

Software Developer Adam Harvey continues to work on adding crates.io admin functionality. A recent [PR](https://github.com/rust-lang/crates.io/pull/8210) adds a concept of "sudo mode" for admins logged into crates.io. Actions that require admin privileges will be disabled by default unless the admin explicitly turns on admin actions from the user menu, at which point they will be given privileges for six hours or until they disable admin actions again from the user menu. With the user functionality and the ability to delete crates, that is about 95% of the rapid response scenarios covered.

The Rust Foundation’s Cloud Compute Program continued to be an understated success in Q1. Running on four cloud machines (2 AWS and 2 Azure), the Cloud Compute Program is used daily by many Rust Project maintainers to help their work. Given the user and use case increases, our lead Infrastructure Engineer, Jan David Nose, created a script for our Cloud Compute dev desktops that automatically cleans up older build and target directories, and this script will run as a cronjob on the cloud compute infrastructure. This will save storage space and credit usage.

Software Engineer Tobias Bieniek’s work on CDN, log-based crates download counting has been running in production since March 2023. In Q1, Tobias added functionality in Rust that provides support for URL rewriting for crate download requests and allows the CDNs to handle crate downloads directly instead of the previous custom backend. This is now allowing cargo to download crates directly from static.crates.io, which means if crates.io has issues the downloads will keep working and the whole system will scale a lot better than before. A blog [post](https://blog.rust-lang.org/2024/03/11/crates-io-download-changes.html) was published describing these changes.

Work on the Rust language specification increased in pace in Q1, with the spec team now meeting once a week, with Joel Marcey serving as editor. A [GitHub project](https://github.com/orgs/rust-lang/projects/45/views/1) was established with work items and several milestones. The team has settled on an [outline](https://github.com/rust-lang/spec/issues/43) for the specification itself. Now the work of adding real prose and content to produce a first draft can begin. The community can follow discussion about the Rust language specification on Zulip at [\#t-spec](https://rust-lang.zulipchat.com/#narrow/stream/399173-t-spec/).

Also in Q1, the Foundation’s Technology Team began hiring for two new engineers- an Infrastructure Engineer, reporting directly to our Lead Infrastructure Engineer, Jan David Nose (JD), and an Interop Software Engineering Lead, funded by Google’s donation to support an Interop Initiative. Applications are now closed and applicant assessments are being finalized.

The second Security Initiative [report](https://foundation.rust-lang.org/news/second-security-initiative-report-details-rust-security-advancements/) was published in Q1, which details all of the program’s work and accomplishments. The latest updates on Security Initiative progress can also be found in the [monthly updates](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/Rust%20Foundation) our Technology Team provides to [OpenSSF’s Alpha-Omega](https://openssf.org/community/alpha-omega/) Project, which continues to generously help fund our work in this area.

## Communications, Marketing & Events

**Publications:**

In Q1, we announced two sets of new members: Lynx, XFusion, and SpruceID in [January](https://foundation.rust-lang.org/news/rust-foundation-new-member-announcement-xfusion-lynx-spruceid/) and Trace Machina and Veecle in [February](https://foundation.rust-lang.org/news/rust-foundation-new-member-announcement-trace-machina-veecle/). We followed a new format for both member announcements, which has made the process more streamlined and efficient overall.

As mentioned above, in February, we had the pleasure of [detailing](https://foundation.rust-lang.org/news/second-security-initiative-report-details-rust-security-advancements/) the many accomplishments realised through our Security Initiative in a second Security Initiative Report, available [here](https://foundation.rust-lang.org/static/publications/security-initiative-report-february-2024.pdf). Thank you to OpenSSF’s Alpha-Omega Project and Platinum Member AWS for their support of this effort to advance the state of security in the Rust language ecosystem. Additional thanks to our many collaborators within the Rust Project.

As described above, we also [announced](https://foundation.rust-lang.org/news/google-contributes-1m-to-rust-foundation-to-support-c-rust-interop-initiative/) Platinum Member Google’s $1M donation in Q1. This funding is underwriting a new Rust-C++ interoperability initiative. Learn more [here](https://foundation.rust-lang.org/news/google-contributes-1m-to-rust-foundation-to-support-c-rust-interop-initiative/). We look forward to sharing a similar announcement of how the $1M donation from Platinum Member Microsoft will be used in Q2.

We published [a new guest blog](https://foundation.rust-lang.org/news/zama-and-the-future-of-privacy-applications-using-rust/) by Silver Member, Zama in Q1, which focuses on how Zama is involved with the Rust community and specifically about TFHE-rs: Zama’s cryptographic library. Guest blogs are a benefit of Rust Foundation membership and are an excellent way for our community to get to know our members and their fellow community members better. We are also exploring new ways to offer guest blogging opportunities to members of the community.

Finally, we had the honor of [amplifying the news](https://foundation.rust-lang.org/news/rust-x-google-summer-of-code-2024/) that the Rust Foundation was selected as a mentoring organisation for Google Summer of Code 2024 (as a representative in this instance of the Rust Project). While the Foundation submitted the application on behalf of the Project and will act as a liaison, the opportunity was surfaced by members of the Project who will be the active party in the mentoring process.

**Training Program Updates:**

Our plans for a Rust Foundation training and certification program remain in an early stage, however, in March, we hosted two listening sessions which gave us deeper insight into key Project and Member priorities as we take the next steps towards content development. These sessions were attended by a handful of participants in each group and over the course of each hour, many valuable questions and considerations were raised. Our intention remains to explore all possible ways to offer Rust language course material in a way that benefits the entire ecosystem and does not take business away from our members. To accomplish this, we would like to offer our courses for free and charge for a certification. More details will be released as progress is made. We are very willing to host additional listening sessions in the future!

**Website:**

In January and February, we made significant progress on the new website, however there is currently a progress bottleneck with only one full-time mar-comms team member at the Rust Foundation in Q1. We anticipate completion of this ongoing project in the very near future, as the remaining tasks to launch are primarily rote and content migration-related and a new full-time mar-comms team member is joining in Q2.

**Events:**

In Q1, the Rust Foundation staff team was present at several community events:

* [FOSDEM](https://fosdem.org/2024/)
* [State of Open Con](https://stateofopencon.com/)
* [CISA]()'s Open Source Software Security Summit
* [Rust Nation](https://www.rustnationuk.com/) – The majority of our staff team was present at Rust Nation, where the Foundation acted as a sponsor. Lead Infrastructure Engineer JD presented a talk at Rust Nation on the complex infrastructure behind the Rust programming language and the resources needed to keep the language thriving.

CISA’s Security Summit gave me and Rust Project Leadership Council and crates.io Team Member, Carol Nichols, a better understanding of how we can improve our future response to crates.io security threats. To learn more about the CISA Security Summit from Carol directly, please read her recent [Rust Foundation guest blog](https://foundation.rust-lang.org/news/attending-cisas-open-source-software-security-summit/).

**RustConf 2024:**

We hit the ground running with RustConf planning in Q1, having updated the conference branding, relaunched the [website](https://rustconf.com) with 2024 information, developed a sponsorship prospectus, began recruiting new sponsors, opened the call for talk proposals (closed as of April 25), and opened registration. We look forward to announcing speakers and releasing the program in Q2.

Special thanks to the community members who accepted our invitation to participate on the RustConf 2024 Program Committee where they are helping select talks from the CFP and shape the program. As the new host of this Rust community event, our team felt it was necessary to develop new policies around the Program Committee and ensure the process of selecting talks is representative of many sub-groups within Rust. You can learn more about our Program Committee [here](https://drive.google.com/file/d/1b0EOTABqlSwdFD4YF5fw9AgB5wimPRnw/view).

As a reminder, the Rust Foundation will be hosting RustConf from September 10-13, 2024 in Montreal, Canada and online! Learn more at [rustconf.com](http://rustconf.com) and reserve your spot today. We would love to see you there!

If your organisation is interested in supporting this long-running and beloved Rust community event, we have many different sponsorship opportunities available. Take a look at our [sponsorship hub](https://rustconf.com/become-a-sponsor/) on the website and reach out to us at [rustconfsponsors@rustfoundation.org](mailto:rustconfsponsors@rustfoundation.org) if you are interested or have any questions. Special thanks to [Devolutions]() for coming aboard as our exclusive Diamond Sponsor!

RustConf will also feature Rust Global – a Rust Foundation-hosted mini conference on Friday, September 13. Rust Global will feature conversations about the professional use of Rust in global governments and the enterprise. To grab a spot at Rust Global, please claim a RustConf “Industry/Government” ticket at [registration](https://www.eventbrite.com/e/rustconf-2024-tickets-865842106047?aff=oddtdtcreator) and add on the free Rust Global option.

The RustConf “UnConference” will also take place on Friday, September 13. As per tradition, the UnConference will be a less-structured chance for attendees to discuss key Rust Project priorities. Registration will take place separately in Q2. More details to come!

## **Community Grants Program**

As mentioned in our Q4 2023 recap, we conducted a thorough assessment of the Community Grants Program late last year with Fellowship awards emerging as a key priority. In Q1, we initiated discussions with the Leadership Council about our Fellowship awards to hone our plan and offerings. We are looking forward to announcing the 2024 cohort later this year with input from the Leadership Council to be reflected in the overall strategy. Stay tuned for more details!

---

That concludes the first Rust Foundation quarterly recap blog for 2024. If you have any questions about the contents of this report, don’t hesitate to contact us at <u>contact@rustfoundation.org</u>. If you are interested in joining the Rust Foundation as a member, please email us at <u>membership@rustfoundation.org</u>.

You can find past Rust Foundation Quarterly Updates [here](https://foundation.rust-lang.org/tags/quarterly%20updates/).

&nbsp;