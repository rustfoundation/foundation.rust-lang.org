---
title: >-
  New SLSA++ Survey Reveals Real-World Developer Approaches to Software Supply
  Chain Security
byline: Rebecca Rumbul
description: >-
  New report from Chainguard, the Eclipse Foundation, the Open Source Security
  Foundation, and the Rust Foundation details software supply chain security
  survey findings
date: 2023-03-15T09:00:00Z
tags:
  - announcement
  - security
  - research
  - publications
index: false
layout: layouts/news.njk
---
<img src="/img/news/2023-03-15-slsa-survey/slsa-social-card.png" width="580" height="304" title="SLSA++ — A Survey of Software Supply Chain Security Practices &amp; Beliefs" />

By: David A. Wheeler, The Linux Foundation; John Speed Meyers, Chainguard; Mikaël Barbero, Eclipse Foundation; and Rebecca Rumbul, Rust Foundation

Answering even basic questions about software supply chain security has been surprisingly hard. For instance, how widespread are the different practices associated with software supply chain security? And do software professionals view these practices as useful or not? Easy or hard? To help answer these and related questions, the Rust Foundation,&nbsp;<a target="_blank" rel="noopener" href="https://www.chainguard.dev/">Chainguard</a>, the [<u>Eclipse Foundation</u>](https://www.eclipse.org/org/foundation/), and the [<u>Open Source Security Foundation</u>](https://openssf.org/) (OpenSSF) [<u>partnered to field a software supply chain security survey</u>](https://uploads-ssl.webflow.com/6228fdbc6c97145dad2a9c2b/640b6a455617000890bd79ba_SLSA%2B%2BWhitepaper_Design_Final.pdf). The questions were primarily, but not exclusively, derived from the security requirements associated with the [<u>Supply-chain Levels for Software Artifacts</u>](https://slsa.dev/) (SLSA) supply chain integrity framework version 0.1 (the version when the survey was conducted), hence SLSA++.&nbsp;

In light of the recent [<u>White House National Cybersecurity Strategy</u>](https://www.whitehouse.gov/briefing-room/statements-releases/2023/03/02/fact-sheet-biden-harris-administration-announces-national-cybersecurity-strategy/), which emphasizes organizations use best practices and frameworks for secure software development, it's important to understand how individual contributors responsible for this work–like developers, open source maintainers and security practitioners–are adopting software supply chain security practices and guidelines. The new SLSA++ survey provides insights into these trends, what’s working and what’s not working.&nbsp;

The survey, conducted in the summer and fall of 2022, includes data from nearly 170 respondents at a wide range of organizations, large and small, some security-focused in their role and others not. All respondents answered a series of questions for ten different software supply chain security practices. Three key findings stand out:

### **Some software supply chain security practices are already widely adopted.**

Many practices already have strong or moderate adoption. For instance, over half of the respondents report always using a centralized build service. Other practices, such as digital signatures, were practiced less often: only 25% of respondents reported that their team always signs built artifacts. These findings are consistent with Google’s 2022 State of DevOps [<u>report</u>](https://cloud.google.com/blog/products/devops-sre/dora-2022-accelerate-state-of-devops-report-now-out).

<img src="/img/news/2023-03-15-slsa-survey/slsa-graph.png" width="580" height="304" title="Prevalence of Selected Software Supply Chain Security Practices" />

### **Most practices are considered helpful though there is surprisingly little variation in the perceived level of helpfulness.**

For each software supply chain security practice in the survey, at least 50% of the respondents labeled the practice as either extremely helpful or very helpful. Surprisingly though, the perceived helpfulness varies only slightly from practice to practice among the practices surveyed. Finally, the extent to which a participant views a particular practice as helpful is positively correlated with the likelihood that the participant’s organization adopts that practice. Whether these practices are viewed as helpful and then used or whether used practices are used and then viewed as helpful can’t be determined from the survey data.&nbsp;

### **Some SLSA practices are considered substantially more difficult than others.**

Hermetic builds and reproducible builds were considered much more difficult than the other practices. Over 50% of respondents stated that those practices were either extremely difficult or very difficult. Other practices, such as scanning container images, were considered relatively easy. Additionally, the perceived difficulty of these practices had no statistically significant relationship with adoption.

In summary, the survey results suggest that software supply chain security practices are not an unattainable ideal. Some software supply chain security practices already enjoy widespread adoption. Also importantly, because perceived usefulness, not difficulty, appears to currently explain trends in adoption of these practices, parties interested in promoting these practices should consider explaining the benefits of these different practices rather than simply focusing on better tools.

### A report detailing the survey, including its methodology, can be found [<u>here</u>](https://uploads-ssl.webflow.com/6228fdbc6c97145dad2a9c2b/640b6a455617000890bd79ba_SLSA%2B%2BWhitepaper_Design_Final.pdf).&nbsp;

---

If you're interested in learning more about the findings and how organizations can implement the SLSA framework, join the Rust Foundation, Chainguard, OpenSSF, and Eclipse Foundation for a virtual discussion on March 22, 2023 from 11-12 PM ET / 8-9 AM PT. Sign up for a calendar reminder [<u>here</u>](https://www.crowdcast.io/c/slsa-practice).