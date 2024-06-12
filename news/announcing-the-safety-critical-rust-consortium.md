---
title: Announcing the Safety-Critical Rust Consortium
byline: Rust Foundation Team
description: >-
  The Rust Foundation, AdaCore, Arm, Ferrous Systems, OxidOS, Synopsys, HighTec
  EDV-Systeme GmbH, TrustInSoft, Veecle, and Woven by Toyota have formed a new
  group dedicated to the responsible use of Rust in safety-critical software.
date: 2024-06-12T12:00:00Z
tags:
  - announcement
  - foundation
  - security
index: false
layout: layouts/news.njk
---
DOVER, DELAWARE, USA, June 12, 2024 – The Rust Foundation, <a href="https://www.adacore.com/" title="AdaCore" target="_blank" rel="noopener">AdaCore</a>, <a href="https://arm.com/" title="Arm" target="_blank" rel="noopener">Arm</a>, <a href="https://ferrous-systems.com/" title="Ferrous Systems" target="_blank" rel="noopener">Ferrous Systems</a>, <a href="https://hightec-rt.com/en/" title="HighTec EDV-Systeme GmbH" target="_blank" rel="noopener">HighTec EDV-Systeme GmbH</a>, <a href="https://www.lynx.com/" title="Lynx" target="_blank" rel="noopener">Lynx Software Technologies</a>, <a href="https://www.oxidos.io/" title="OxidOS" target="_blank" rel="noopener">OxidOS</a>, <a href="https://techfund.jp/" title="TECHFUND" target="_blank" rel="noopener">TECHFUND</a>, <a href="https://trust-in-soft.com/" title="TrustInSoft" target="_blank" rel="noopener">TrustInSoft</a>, <a href="https://www.veecle.io/" title="Veecle" target="_blank" rel="noopener">Veecle</a>, and <a href="https://woven.toyota/en/" title="Woven by Toyota" target="_blank" rel="noopener">Woven by Toyota</a> are thrilled to jointly announce the Safety-Critical Rust Consortium. The primary objective of this group will be to support the responsible use of the Rust programming language in safety-critical software — systems whose failure can impact human life or cause severe environmental or property harm.

Safety-Critical Rust Consortium Membership is open to Rust Foundation member organizations and other invitees, such as industry, academic, and legal experts.

Work under the consortium will begin with the creation of a public charter and goals, and meeting minutes will be published on an ongoing basis. The Safety-Critical Rust Consortium will liaise with the Rust Project through Rust Foundation Project Directors and members of Rust Project teams. The Consortium’s scope, which will be fully delineated in the charter, may include the development of guidelines, linters, libraries, static analysis tools, formal methods and language subsets to meet industrial and legal requirements. The Consortium’s deliverables will be developed and licensed in a manner compatible with other Rust Project endeavors.

The group may further shepherd Rust Foundation-funded implementation work, including grants to existing academic teams or FOSS projects. Any Rust Foundation-funded work will be submitted upstream, licensed as FOSS, and any specifications will be freely available. The group will further attempt to coordinate with and expand on existing safety-critical projects and standards including <a href="https://www.sae.org/standards/content/ja1020/" title="SAE JA1020" target="_blank" rel="noopener">SAE JA1020</a>.

*“This is exciting! I am truly pleased to see the Rust Foundation and anyone in the safety-critical space coming together on this topic”* said Graydon Hoare, creator of the Rust programming language.

*"Safety is our foremost priority in vehicle software development. Traditionally, achieving the highest levels of safety has been a complex and lengthy endeavor, requiring the use of specialized tools and processes beyond the programming language. We are therefore pleased to collaborate with leading experts in the safety industry to integrate new tools such as Rust into our safety-critical systems,"* said JF Bastien, Distinguished Engineer at Woven by Toyota.

*“Rust has already established itself as a safe and secure programming language with developers in open source, industry and governments. Now is the time to use that momentum towards bringing Rust as a mainstream language in safety-critical areas, providing processes and specifications that allow Rust to be certified in this space,”* said Joel Marcey, Director of Technology at the Rust Foundation.

Below, the founding members of the Safety-Critical Rust Consortium have addressed several anticipated questions about this effort.

## What is “safety-critical”? Rust is already safe!

Programming language safety refers to a language’s ability to prevent errors or undefined behaviors at compile time or runtime. On the other hand, "safety-critical" refers to a system’s ability to operate without causing accidents or catastrophic failures that will result in harm to people, property or the environment. So, while safety-critical systems rely on languages that emphasize safety and security, such as Rust, programming tools are only one component of the overall strategy.

## Which industries are considered safety-critical?

Industries that are particularly concerned with functional safety include transportation (such as automotive, aviation, space), energy, life sciences, and more. Because of their potential impacts, these industries are often regulated, have liability considerations, and are guided by standards such as IEC 61508, ISO 26262, IEC 62304, and DO-178C. These industries have decades of experience delivering products, learning from iterating based on real-world feedback, and improving processes. An ecosystem of tools and tool vendors have evolved, and best practices have been learned to create a safety culture around tooling.

## Why Rust?

Rust offers particular advantages in terms of developer ergonomics, productivity and software quality; however, it lacks a deep and established well of safety-processes and collective industry knowledge of safety-critical systems.

Without closing this gap, a developer must primarily rely on best practices and normative precautions, which can limit innovation. Rust developers who stray from the well-trod path can find themselves facing an inquiry were an accident to occur. In these circumstances, anything that seems unusual will be investigated for fault. This risk creates a disincentive to widespread Rust adoption, leaving developers unable to reap all its advantages while potentially facing financial, reputational and moral costs.

The gap in safety-critical resources within the Rust programming language ecosystem is also an exciting opportunity. By rapidly incorporating lessons learned from years of careful development and past mistakes in the wider open source ecosystem, Rust can become a valuable component of a safety toolkit adaptable to various safety-critical industries and severity levels.

### What does this development mean for Rust?

Aspiring to meet safety-critical needs has costs, just as aspiring to security or quality needs does. Some of those costs can be distributed across multiple priorities, such as verification and validation through code review, writing a specification, identifying properties of a “software bill of materials,” etc. The Rust programming language can bear some reasonable costs with the participation of interested parties, but such costs cannot be imposed to Rust the ecosystem thoughtlessly. Indeed, a hobby open source project on crates.io cannot suddenly be made safety-critical, cannot be told that lives depend on the project’s correctness, without serious consideration and buy-in from community members.

## Why this effort, under the Rust Foundation?

There are existing efforts in this space, most notably <a href="https://www.sae.org/standards/content/ja1020/" title="SAE JA1020" target="_blank" rel="noopener">SAE JA1020</a>. The efforts are laudable, and will likely meet the needs of their target audience. However, we hope that a wider effort under the Rust Foundation can meet the needs of the Rust community at large, rather than a subset of industries, groups and/or use cases. Moreover, the needs of specific groups are sometimes at odds with the needs of others in the community. This can either lead to tensions in adopting stringent requirements, or cause friction in the specific groups significantly lagging behind in the evolution of the language and tools surrounding it. By working under the auspices of the Rust Foundation, the Safety-Critical Rust Consortium can minimize the risk of such fracturing.

## How will this group work with the Rust Project?

The expectation is that the Safety-Critical Rust Consortium attracts many participants who are not currently Rust users. The initial group members understand that the Rust Project operates in particular ways and is wary of external entities aggressively promoting their own goals. The hope of the initial group members is to listen to the Rust Project members’ inputs and understand how to best broaden the user base and applicability of Rust without adversely affecting existing Rust users and Rust Project participants. The Safety-Critical Rust Consortium should collaborate with the Rust Project Language Specification Team and the Formal Methods team. It should also perform work as the Rust Project does – through Zulip and virtual meetings with public minutes. The consortium plans to hold its first in person meeting at <a href="https://rustconf.com" title="RustConf 2024" target="_blank" rel="noopener">RustConf 2024</a> out of a desire to integrate into and work closely with the Rust Project.

The Safety-Critical Rust Consortium intends to keep all stakeholders updated on its work, suggesting modification or additions to how the Rust language and libraries are created and addressing how different safety levels adopt the language and libraries. Doing so will create room for a variety of tooling to support safety activities, verification and validation, and quality assurance within Rust. The work would, in turn, create best practices, which can then be discussed with safety assessors and governments to more officially establish the best practices as recommendations.

## What is the expected impact outside of the Rust Foundation and Project?

Work such as SAE’s would not become obsolete through a Safety-Critical Rust Consortium, it would however become narrower in tuning the wider work to their specific audience, after informing the safety-critical Rust group about their needs. The safety-critical Rust Consortium, and the wider Rust Foundation, would then pursue an industry adoption and advocacy role, with users of Rust as well as with external entities such as governments and international standards groups. The Rust Foundation is committed to ensuring that funding and support are available where needed, including both community volunteers and funded initiatives, such as for this safety initiative.

## Why participate?

In short, your help is needed!

We want the Safety-Critical Rust Consortium to reflect a wide variety of perspectives, including various safety industries, representatives from standards groups guiding these industries, tooling providers who cater to such industries, and Rust community members from the language and library spaces which are interested in collaboration.

### How can I ask another question and/or get involved?

Interested organizations, individuals, and Rust Foundation Members are invited to express interest in joining or submit further questions via email at [contact@rustfoundation.org](contact@rustfoundation.org).

---

## About the Rust Foundation

<a href="https://rustfoundation.org/" title="The Rust Foundation" target="_blank" rel="noopener">The Rust Foundation</a> is an independent nonprofit dedicated to the safety, security, sustainability, and health of the Rust Programming language and the people who use it. Through close partnerships with organizations passionate about Rust and the growing Rust Project and community, the Rust Foundation is helping forge a better open source future with Rust.

Visit the Rust Foundation <a href="https://rustfoundation.org/" target="_blank" rel="noopener">website</a> to learn more. Follow the Rust Foundation on <a href="https://x.com/rust_foundation" title="Rust Foundation Twitter" target="_blank" rel="noopener">X (formerly known as Twitter)</a> and on <a href="https://www.linkedin.com/company/rust-foundation" title="Rust Foundation LinedIn" target="_blank" rel="noopener">LinkedIn</a>.

&nbsp;