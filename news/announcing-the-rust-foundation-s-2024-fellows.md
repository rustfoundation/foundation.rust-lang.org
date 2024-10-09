---
title: Announcing the Rust Foundation’s 2024 Fellows
byline: Rust Foundation Team
description: The Rust Foundation is thrilled to introduce our 2024 Fellowship cohort
date: 2024-10-14T12:00:00Z
tags:
  - announcement
  - foundation
  - community grants
index: false
layout: layouts/news.njk
---
The Rust Foundation's<a href="https://foundation.rust-lang.org/grants/" target="_blank" rel="noopener"> <u>Community Grants Program</u></a> supports Rust programming language maintainers, community members, and organizers via financial awards, travel stipends, and training support. Through the Community Grants Program, we aim to reward and support innovative ideas that will benefit the Rust ecosystem for an increasingly global and diverse set of users.

Our<a href="https://foundation.rust-lang.org/grants/fellowships/" target="_blank" rel="noopener"> <u>Fellowship award</u></a> is a grant given annually to active members of the Rust programming language who have made meaningful contributions to the Rust Project. During their time in the program, Fellows receive a monthly stipend, support for additional training, and funding for travel to relevant events.

This year, three categories of Fellowship were awarded:

* Community Fellowships: 12-month awards for people working to build Rust communities outside of Western Europe and North America to support work such as organizing communities and events and creating content and training materials for their communities.
* Project Goal Fellowships 6-month awards (with the potential to extend) for people working on the Rust Project's agreed-upon <a href="https://rust-lang.github.io/rust-project-goals/2024h2/proposed.html" target="_blank" rel="noopener">goals</a> (and sub-goals).
* Project Fellowships: 12-month awards for members of the Rust Project Teams and Working Groups to support contributions that serve the goals of the Rust Project Teams and Working Groups

Today, the Rust Foundation is thrilled to introduce our 2024 Fellowship cohort! Please join us in welcoming…

## Community Fellowships

### Promise Reckon (<a href="https://github.com/promiseReckon" target="_blank" rel="noopener">@PromiseReckon</a>)

Promise Reckon is an Embedded system Engineer and a Robotics Instructor at Profix in Canada. He has been a passionate Rustacean since 2022.

His focus during the Fellowship year will be promoting Rust adoption in Nigeria through building a vibrant and sustainable Rust Developers Community. This will include arranging meetups and workshops; organising and running Rust training sessions; and collaborating with local technology businesses.

### Kostiantyn Mysnyk (<a href="https://github.com/Wandalen" target="_blank" rel="noopener"><u>@Wandalen</u></a>)

With a decade of experience in software engineering, I'm a Rust developer who loves to hammer out solutions with precision and efficiency. Known for my no-nonsense approach, I tackle challenges head-on and deliver rock-solid software. Whether coding or organizing community events, I bring a straightforward and impactful style to everything I do. I find great fulfillment in contributing to the global Rust community. By sharing knowledge and collaborating on innovative projects, I aim to enhance my skills while supporting the community's growth. My work is guided by a passion for creating value and building connections that make a meaningful impact. I'm an engineer at heart, passionate about crafting precise solutions in Rust. I also enjoy organizing community events that bring people together. By combining my technical skills with my organizational abilities, I aim to foster collaboration and advance the Rust community.

As part of my Fellowship with the Rust Foundation, I will focus on organizing Rust boot camps and events in Ukraine to foster community engagement and education. Additionally, I will explore opportunities to integrate Rust into higher education curricula, aiming to broaden its adoption and usage among students and educators.

### Mordecai (<a href="https://github.com/martcpp" target="_blank" rel="noopener">@martcpp</a>)

Mordecai, also known as Mart, is a software developer from Nigeria who has contributed to several open-source projects, including AI (MetaGPT) and others. He is a student at the University of Benin, studying Marine Engineering, focusing on autopilot systems and zero-knowledge proofs (ZKP) in the maritime sector.

Mordecai aims to grow Rust within Africa and help drive the adoption of Rust into university systems.

## Project Goal Fellowships

### Alejandra González (<a href="https://github.com/blyxyas" target="_blank" rel="noopener">@blyxyas</a>)

I'm a programmer, cat lover, and environmentalist. I'm obsessed with performance because I don't think a user should spend hundreds just to enjoy your apps, and the planet shouldn't suffer, either. I joined the open source collective about four years ago, two and a half of those being part of the Rust project and the Clippy team.

I will optimize the linting side of things, the diagnostics that the Rust compiler is famous for, and Clippy, our linter. This includes making algorithms to preview the lints that will emit and execute just those to checking that our L1 cache and type sizes are not monstrously slow.

### **Nick Cameron (**<a href="https://github.com/nrc" target="_blank" rel="noopener">@nrc</a>**)**

Nick is a freelance engineer and consultant. He's been involved with the Rust project since 2014 and is a former core team member. He has worked in many different areas, most recently as part of the async working group.

Nick will improve the documentation of async Rust for developers of all experience levels and backgrounds. That should include revitalizing the async book, improving library and reference docs, and perhaps providing other learning material.

### **Predrag Gruevski** <a href="https://github.com/obi1kenobi" target="_blank" rel="noopener">(obi1kenobi)</a>

Predrag is an independent software researcher working at the intersection of dev tools, compilers, and databases. He is the author of the cargo-semver-checks linter for semantic versioning in Rust and its underlying Trustfall query engine.

Accidental breaking changes in new crate releases are a lose-lose situation: they sap the time and energy of both maintainers and downstream users. The cargo-semver-checks linter can catch many kinds of such breakage and is planned to become part of "cargo publish" itself. Let's resolve the remaining merge blockers so running "cargo update" can become fearless!

### **Manuel Drehwald (**<a href="https://github.com/ZuseZ4" target="_blank" rel="noopener">@ZuseZ4</a>**)**

Manuel Drehwald cares about High-Performance Computing, Scientific Computing, and Machine Learning. He works on compiler optimizations and features to support those fields. He is currently a Master's student at the University of Toronto.

During the first half of his Fellowship, Manuel will focus on enabling rustc to automatically differentiate Rust code (in the calculus sense). In the second half of his Fellowship, he will work on running Rust functions on GPUs. New LLVM features enable both projects and should support almost arbitrary Rust code, including std and no-std code, basic Rust types, user-defined types, and most dependencies from <a href="http://crates.io/" target="_blank" rel="noopener">crates.io</a>.

### **Benno Lossin** <a href="https://github.com/y86-dev" target="_blank" rel="noopener">(@y86-dev</a>**)**

I learned Rust in a university project in 2021; the expressive type system instantly hooked me. At the start of 2022, I noticed the Rust for Linux effort. After viewing the code, I was shocked to see that Mutexes and other kinds of locks needed to be initialized via \`unsafe\`. I then solved \[<a href="https://rust-for-linux.com/the-safe-pinned-initialization-problem" target="_blank" rel="noopener">The Safe Pinned Initialization Problem</a>\] by creating the \`pinned-init\` crate we still use today. Afterward, I continued reviewing code and contributing to various other areas. In 2023, I joined the core team of Rust for Linux, working on making Rust a first citizen language in the Linux kernel.

I am primarily working on making Rust more ergonomic in the Linux kernel. I see great potential in adding \[Field Projections\] to the Rust language; they come up very often in Rust for Linux. In addition, they allow us to turn currently \`unsafe\` APIs into safe ones. I will be working on creating and implementing the RFC.

### **binarycat (**<a href="https://github.com/lolbinarycat/" target="_blank" rel="noopener">@lolbinarycat</a>**)**

I'm a self-taught programmer with experience in many high- and low-level languages. Most of my previous open source contributions have been to \`nixpkgs\`. I am working on improving the accessibility, discoverability, and ergonomics of rustdoc search.

## Project Fellowships

### **Onur Özkan (**<a href="https://github.com/onur-ozkan" target="_blank" rel="noopener">@onur-ozkan</a>**)**

I am a self-taught computer scientist specializing in distributed systems, operating systems, and compiler engineering. I am one of the lead maintainers of the Rust Language project, and my responsibilities are mostly related to compiler bootstrapping. On GitHub, you can explore my contributions to open-source projects and organizations (such as Rust Language, libp2p, Fedora Infrastructure, etc.) at <a href="https://github.com/onur-ozkan" target="_blank" rel="noopener">https://github.com/onur-ozkan</a>. Additionally, I share my thoughts on various topics on my website, <a href="http://onurozkan.dev/blog-posts" target="_blank" rel="noopener">onurozkan.dev/blog posts</a>.

I will be working on fixing the download-rustc/ci-rustc issues so we can enable it by default, which will speed up the CI pipelines and shorten compile times for developers. Over the last 5-6 months, I already fixed tens of problems related to it (for ref, you can check all the mentioned PRs from this PR <a href="https://github.com/rust-lang/rust/pull/122709" target="_blank" rel="noopener">https://github.com/rust-lang/rust/pull/122709</a>). After that, I will focus on improving the LSP/rust-analyzer experience for the library and compiler teams (see <a href="https://github.com/rust-lang/rust/pull/120611" target="_blank" rel="noopener">https://github.com/rust-lang/rust/pull/120611</a>) and improve the bootstrap experience by any means (e.g., fixing bugs, working with other teams, cutting down the external dependencies, etc.).

### **Jiayan (**<a href="https://github.com/roife" target="_blank" rel="noopener">@roife</a>**)**

I'm a graduate student at Nanjing University in China, with an interest in programming languages, compilers, and program analysis. I started learning Rust in 2021, and it has been my primary language for research projects since last year. I've also been contributing to Rust for a year and am a member of the rust-analyzer contributors team.

The focus of my Fellowship year will be contributing to rust-analyzer, improving its stability, and refactoring some modules. I also plan to get involved in rustc development and work on driving some interesting proposals forward.

### **Jason Newcomb (**<a href="https://github.com/Jarcho" target="_blank" rel="noopener">@Jarcho</a>**)**

I've been a maintainer of Clippy since 2022 and have contributed for quite a while longer than that. Most of that time has been spent lowering the false-positive rate and internal refactorings.

The fellowship will focus on reducing Clippy's false-positive rate. Notably, this includes interfacing Clippy with the borrow checker and preventing it from making suggestions that violate lifetime rules.

### **Noah Lev Bartell-Mangel (**<a href="https://github.com/camelid" target="_blank" rel="noopener">@camelid</a>**)**

Noah Lev Bartell-Mangel has been involved with Rust since 2020 and is a member of the Rustdoc and Compiler Contributors teams. He also enjoys the research side of programming languages and systems. He is an undergraduate student at UMass Amherst and part of the PLASMA (Programming Languages and Systems at Massachusetts) lab.

During his Fellowship, Noah Lev is excited to continue his contributions to Rustdoc, const generics, and the project as a whole. With Rustdoc, he will be working to improve its user interface, performance, and reliability. His focus for const generics will be on making const parameters and arguments more powerful as part of the expanded const generics project goal. He is also developing a research idea related to Rust generics.

### **Boxy (**<a href="https://github.com/boxyuwu" target="_blank" rel="noopener">@BoxyUwU</a>**)**

Boxy is a compiler engineer who has been working on the Rust compiler since early 2021. Their work has largely focused on the type system, particularly const generics.

As part of Boxy's fellowship, they will primarily work on stabilizing the \`adt\_const\_params\` feature and reworking the \`generic\_const\_exprs\` feature so that it can be stabilized at some point in the future. They will also help release new versions of Rust as part of the release team and introduce better documentation for how the type system is implemented in the compiler.

### **Chen (**<a href="https://github.com/eth3lbert" target="_blank" rel="noopener">@eth3lbert</a>**)**

I'm the latest <a href="http://crates.io/" target="_blank" rel="noopener">crates.io</a> team member. My contributions have primarily focused on enhancing performance and the user experience on <a href="http://crates.io/" target="_blank" rel="noopener">crates.io</a>. Specifically, I've been working on optimizing the database queries that power <a href="http://crates.io/" target="_blank" rel="noopener">crates.io</a> and improving rendering times on the front end, which aims to reduce the load on the database and make the website faster for everyone.

The focus of my Fellowship year will be to support the implementation of pagination for the crate versions page. This will hopefully resolve the long loading issue caused by rendering for those crates with too many versions. Additionally, I will strive to optimize the search functionality and explore possible improvements to the search experience on <a href="http://crates.io/" target="_blank" rel="noopener">crates.io</a>. This could include incorporating additional metrics for crates and leveraging them to prioritize search results. Finally, I will continue assisting with other Rust-lang projects and contributing to other Rust-related projects whenever possible. Ref blog link: <a href="https://blog.rust-lang.org/2024/07/29/crates-io-development-update.html#database-performance-optimizations" target="_blank" rel="noopener">https://blog.rust-lang.org/2024/07/29/crates-io-development-update.html#database-performance-optimizations</a>

### **Rémy Rakic (**<a href="https://github.com/lqd" target="_blank" rel="noopener">@lqd</a>**)**

Rémy Rakic has been interested in Rust since 2013 and started contributing to the project and ecosystem in 2016. He's a member of the compiler contributors team, the compiler performance and polonius working groups, and was involved in the NLL working group.

The focus of Rémy's Fellowship year will be to work on the Polonius 2024H2 project goal, continue working on compiler performance and triage as well as the rustc-perf tool itself, but also PR reviews and regular compiler maintainership activities, like issue triage, bisections and minimizations.

### **Chris Denton (**<a href="https://github.com/ChrisDenton" target="_blank" rel="noopener">@ChrisDenton</a>**)**

I first became interested in Rust around the time 1.0 was released, but I didn't start using it in earnest until a couple of years later. In 2019, I began contributing to Rust itself, which led to becoming a member of the Library Contributors, Crate Maintainers, and Rustup teams. During my Fellowship, I'll continue to contribute to and help maintain Rust's standard library, rust-lang crates, and Rustup, with a focus on Windows support.

### **Deadbeef (**<a href="https://github.com/fee1-dead" target="_blank" rel="noopener">@fee1-dead</a>**)**

I've been contributing to the Rust compiler for about three and a half years now, working on implementing language features and pushing them toward stabilization. I've picked up work on const traits since 3 years ago and am continuing my work on it. As part of my fellowship, I will continue to push const traits toward feature completion, aiming for a future where we can use const trait methods on stable.

### **Eric Huss (**<a href="https://github.com/ehuss/" target="_blank" rel="noopener">@ehuss)</a>

Eric Huss has been involved with the Rust project since 2017. He was drawn to Rust due to its welcoming community and the attraction of a safe systems language that exposed him to new language concepts and can be very productive to use. Eric is currently the lead of the Cargo team (representing the Devtools team on the Leadership Council) and the lead of the lang-docs team. He maintains and works on a variety of projects and infrastructure around the Rust project.

The focus of Eric's Fellowship year will be leading the Cargo team and continue to assist with maintenance and new development; continuing participation in other teams, such as the Devtools team and as lead of the Language Documentation team; continuing maintenance of other Rust-lang projects, such as Rust-enhanced, mdBook, cargo-bisect-rustc, rustfix, the RFC repo, and triagebot, continuing assisting other Rust-related projects when possible.

*Congratulations to these well-deserving grant recipients!*

### **Hardship Grants and Event Support Grants Are Available Year-Round**

Hardship Grants are financial awards ranging from $500 to $1,500 made to active Rust Project maintainers facing financial hardship. Event Support Grants are financial awards ranging from $100 to $500 made to support events (both physical and virtual). Both categories of grants are open for applications year-round. You can learn more <a href="https://foundation.rust-lang.org/grants/" target="_blank" rel="noopener">here</a>.

## **Community Grants Program Support**

If your organization is interested in supporting the Rust language community, donating to the Community Grants Program is a wonderful way to do so. You can inquire about supporting the program by emailing us at grants@rustfoundation.org. We accept donations from organizations for the Community Grants Program in any amount. Additionally, individuals can support the Community Grants Program through our<a href="https://github.com/sponsors/rustfoundation" target="_blank" rel="noopener"> <u>GitHub Sponsors</u></a> page.

*You can learn more about the Community Grants Program* <a href="https://foundation.rust-lang.org/grants/" target="_blank" rel="noopener"><em>here</em></a> *and find the list of 2023 Fellows* <a href="https://foundation.rust-lang.org/news/announcing-the-rust-foundation-s-2023-fellows/" target="_blank" rel="noopener"><em>here</em></a>*.*

Congratulations again to our 2024 Fellows!