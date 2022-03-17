---
layout: news
title: Rust Community Grants Program - Survey Responses
description: 
tags:
  - community grants
  - plans
---

Thank you to everyone who responded to our survey about the <a href="/grants/">Community Grants Program</a>. We are very grateful that you took the time to provide us with your thoughts and ideas. We are now busy working on the final details of the Program in order to open for applications next month, and we wanted to share the results of the survey with you to demonstrate how your input has influenced our thinking.

## Background

In January 2022 the Rust Foundation opened a survey with the objective of gathering the views of the Rust maintainer community about the issues that concerned them and the areas that they felt were most in need of financial support. The aim of this exercise is to help inform the Community Grants Program and to ensure that, as far as is possible within our operational constraints, the funding streams that we launch will go some way to meeting the needs of the community.

## Who responded

In total 122 completed responses to the survey were received, breaking down by language as follows:

- English: **102**
- Chinese (including simplified): **4**
- Russian: **8**
- German: **3**
- French: **6**
- Portuguese: **1**

The high proportion of responses to the English language version of the survey somewhat belies the geographic diversity of those who responded. Of those 102 only 44 came from the USA/UK, the remainder were spread across 27 different countries.

In terms of the level of engagement with the Rust Project, a third of respondents described themselves as active contributors. It is interesting to note, however, that breaking out the results into those who completed the English version of the survey, and those who completed the non-English version reveals significant differences, with fewer than one in seven in the latter group considering themselves to be active contributors.

This trend was continued with memberships of Rust teams, with markedly higher levels of engagement from those who responded in English compared to those who did not. This is perhaps unsurprising, given that English is the default technical language of these teams. What is significant is that almost two thirds of the non-English respondents expressed a desire to be a member of a team, project group, or working group.

![Breakdown of respondents by self-description](/img/news/2022-03-17-community-grants-program-survey-responses/respondents.png)

## What do people want us to fund?

Each respondent was asked to select five options from a list of potential funding priorities, with the additional option to add in free-text responses to encompass anything missed out. Again we thought that it would be useful to show both the total results and the English/non-English splits:

![What funding priorities the respondents selected](/img/news/2022-03-17-community-grants-program-survey-responses/funding-priorities.png)

Documentation was top across the board. The English responses largely mirrored the overall totals, due to their share of the sample size, and the non-English responses broadly aligned as well. It was interesting to see, however, that Educational Materials indexed significantly higher for the non-English group, and Performance Enhancements were also somewhat higher, with New Features being less significant.

## What/How should things be funded?

Respondents were asked to rate on a scale of 1-9 a number of different funding options, with the scores summed to enable ranking. Again, this is shown as both a total and split by response languages.

![How respondents said things should be funded](/img/news/2022-03-17-community-grants-program-survey-responses/funding-methods.png)

The most popular options clustered fairly tightly together in terms of scoring, with the funding of projects and individuals (in the latter case either through direct sponsorship or a Fellowship) scoring highly. There was fairly close alignment again in the language splits, though for the non-English respondents there was higher indexing both for the support of infrastructure and the funding of organisations, than was the case for those who completed the survey in English.

## Potential points of focus

A number of common themes arose in the text responses, and these are outlined below:

### Rust is difficult to learn

Rust’s steep learning curve has significant consequences for the growth of the community. It limits the number of people learning, and then using, the language, and this then means that the potential population of people who may become contributors, reviewers, and so on is similarly limited. It can also limit the adoption and usage of the language by organizations who may be minded to provide financial, or in-kind, support to the project in the future.

From the survey results the highest scoring response to the question relating to funding priorities was “Documentation” with 50% of respondents listing that as a priority. Similarly, 28% of respondents listed “producing educational materials” as a priority (and as noted above, this indexed much more significantly among the non-English respondents). Specific write-in priorities include more activities like Rustbridge, a new website, and generally better books/documentation. Comments included:

> Improving the tooling ecosystem (test runner, crates.io (lib.rs offers some features missing from crates.io IMO), cargo, official support/guidance for common build environments like Docker (see cargo-chef) Complete WIP "rust books" and update older ones. Continuing improving the tooling and accessibility of the rust core to solicit new active contributors. Try to improve the language by simplifying or consolidating language features

> Developing intermediate/advanced educational content for Rust developers. Building commonly-needed low-level data structures and concurrency primitives for the Rust ecosystem.

> More rust books for different examples/better more explicit examples

### The Project Teams are overstretched

It is clear that the volunteer-led (and run) project teams are all, to some degree, overstretched. This results in delays in reviewing and merging, pull requests (i.e. code review - cited by 40% of respondents as a key priority); limits their ability to mentor and develop people who could become valuable contributors to the project, carry out development work themselves, and so on. It also places undue stress upon team members, bringing with it the risk of burnout. Comments from the survey include:

> Keeping contributors that I mentor able to keep contributing so the teaching work I put into said mentoring keeps benefiting the project. Funding the unpaid team members so they have more time to review the ever growing list of open pull requests.

> I also want the foundation to focus on supporting the overall health of the Rust project. Making sure we have enough maintainers to review PRs and mentor other contributors.

> Reviewing and triaging pull requests. Helping understaffed teams grow carefully. Helping teams get a handle on their large volume of incoming PRs.

> help maintain important projects whose maintainers are missing or overwhelmed...am thinking stuff like chrono, dotenv, and mdbook

### Coordination/organisation could be improved

A number of people responding to the survey raised the issue of the lack of overall coordination of the project, and/or the lack of resources that are dedicated to the overall management of the project. This is due in no small part to the volunteer-led nature of the project teams that are, as previously mentioned, already overstretched. Comments from the survey include:

> We don't have a functional website team, vision for how our online assets should tie together, or designers on staff. This work is crucial, but entirely unfunded.

> We have lots of people doing work, and not nearly enough people helping to do organizational and process work. Building and maintaining tools that help implement that process. Better overall product management (building consensus about relative priorities across the Rust project/product)

> Designing better processes for tracking and managing large numbers of issues. Picking up the follow-through after people develop new features, such as stabilizing nightly features and making sure they fit with other features. Reviewing and triaging pull requests. Helping understaffed teams grow carefully. Helping teams get a handle on their large volume of incoming PRs. Designing lower-friction processes for teams to collaborate when development projects cross the jurisdiction between teams. Finding and mentoring development of critical features that will unlock many other things.

### More resource required to address bugs, compiler speed, technical debt etc.

Many of the respondents to the survey highlighted technical debt, unfixed bugs, and also the speed of the compiler. Specifically, 41% of respondents cited bug fixes as a key priority, and 41% noted performance issues. Comments from the survey include:

> QA in general. Someone who leads a team of hired hands to provide sustained downward pressure on total bug count, integration cycle time, compiler slowness. Measurable goals, universally valued, with long term investment in staffing for improvement.

> Lots of bug fixes, performance fixes and feature implementations require massive refactorings before they become feasible. Several contributors have given up on such projects because of the amount of technical debt we have accrued. We should have a focussed and paid group to deal with such major refactorings that unblock a lot of people.

> Compiler Speed. I work for a company that is interested in Rust and potentially sponsor Rust with a lot of money. But they currently don't like the compiler speed.

> It's important to me that getting funding for internal cleanups and organizational stuff is straightforward . . .Other areas I care about even if they aren't my main focus are diagnostics, performance improvements and bug fixes. 

> Compiler speed so it can be used in web projects and perform quicker deployments when -cargo build -release is called.

## Further insights that will help shape our approach to the Grants Program

There were lots of responses that have been useful in helping us develop our approach to the grants program. Examples include:

> Communicate, communicate, communicate. Make the application process simple, feature updates from the recipients, publish guidance on how to apply and how to improve one's chances of a successful application, report on the website from the Foundation on what worked, what didn't work and any changes to the program. Be excessively transparent so that the impression that having relationships with members of the Foundation or of Rust leadership aren't determinant on receiving grants.

We are very keen to respect this view in terms of how we approach both the processes and the reporting of the grants program. Making the scoring system open and transparent will be key to this. We also recognise that there are a number of different views on how we achieve the goals of the Program and recognise work in the Project:

> We should fund people who have done great work for Rust and who we expect to continue to do great work for Rust. We shouldn't pay on the expectation of specific future work, but rather, on the expectation that their work overall will be valuable to the Rust community.

> If I receive some support, I would like some stability in it. I'm a student, with this I'm able to review and contribute most of the year. However, there are two or three months when my studies take priority and I have to reduce my time-commitment. If the payout would always be a result of the activity last month, it could lead contributors to contemplate if they can take a break from the project. As a solution, I think the support should be based on a larger time frame, like two or three months.

> …don't hire anonymously or through a ghost-work / piece-work system. Hire from the community and ensure it's people who do actually care about helping the project for its own sake. There's a threshold of routine-work-for-low-pay below which the overhead of interpreting and absorbing the work outweighs its value to the recipient. An army of anonymous bug-closers with no meaningful connection to the project would be disruptive to the community.

These, and many other responses have been hugely useful as we develop our approach to funding people who work on Rust.

## Other factors in how we shape the Community Grants Program

The results of the survey have been incredibly useful in shaping our thinking, and we will be adding this input to considerations from other sources. We have taken advice from other individuals and organisations that have experience with funding in this space. Importantly, we have had some excellent input from our key donors to the Program to understand their interests and ambitions for the Program and what we need to do to ensure it is considered a success. We very much want to ensure that we are able to provide funding to the community year on year, and this means that we need to demonstrate the value and impact to our corporate donors, and deliver strong arguments to provide funding in future years.

## What happens next?

Over the next couple of weeks we will be finalising our plans, so that we will be ready to launch at the start of April. 

Watch this space for more updates, and be sure to follow us on [Twitter](https://twitter.com/rust_foundation) and [LinkedIn](https://www.linkedin.com/company/rust-foundation/) for all the latest.
