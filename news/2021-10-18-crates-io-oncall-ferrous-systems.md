---
layout: post
title: "Adios Pagers: New Developments on Crates.io"
description: Ferrous Systems takes over crates.io oncall rotation
tags:
   - update
   - crates.io
---

<h2>by <a href="https://github.com/tmandry">Tyler Mandry</a>, Quality Director, Rust Foundation and <a href="https://github.com/yaahc/">Jane Lusby</a>, Project Director, Collaboration</h2>

![Crates.io](/img/posts/2021-10-18-crates-io-oncall-ferrous-systems/crates-io.png)

If you’re reading this post, you’re probably familiar with [Crates.io](https://crates.io/) and its significance in the Rust ecosystem. If you write Rust code using Cargo, you’ve certainly downloaded a crate from crates.io to use in your project, and hopefully your experience has been positive. A LOT of stuff runs on top of Crates.io, and Rust developers around the world depend on it to support their projects. In fact, as of this publication, Crates.io has seen over **ten billion downloads** and now hosts **69,000+ crates**! Pretty impressive numbers.

Crates.io is maintained by a [talented and dedicated group of volunteers](https://www.rust-lang.org/governance/teams/crates-io) who are responsible for improving the service. Until recently, this team was also responsible for troubleshooting issues and ensuring it always ran as needed. This was a 24/7 responsibility, which meant rotating pager duty among the volunteers to be sure issues were addressed quickly and Rust developers didn’t experience downtime. On behalf of the roughly [1.3MM members](https://www.zdnet.com/article/programming-languages-javascript-has-most-developers-but-rust-is-the-fastest-growing/) of the Rust community, we want to take a moment to say thank you to the Crates.io team for your amazing support. ❤️

When we talked to the team, however, it became clear that they could use some assistance, particularly with the on-call element. So, we reached out to a number of individuals and contractors who had the skills to provide it and asked if they could help.

And now, we’re delighted to share that [Ferrous Systems](https://ferrous-systems.com/), a team of Rust programming consultants, has taken over responsibility for the on-call rotation necessary to ensure that Crates.io is always accessible. The Rust Foundation is financing a team of four programmers from Ferrous Systems that will act as a “first line of defense” for keeping the server up and running. They’ll be on rotation at all times to ensure continual coverage and quick, seamless issue resolution, so that programmers around the globe will be unaware of – and uninterrupted by – any service hiccups. The improvements have already been well received. Justin Geibel, a lead of the Crates.io team, recently shared the following:

> This weekend I attended a wedding (and then took a recovery day) without having to worry that my laptop was nearby in case there was a page. Thank you for getting this secured. It has been a huge reduction in stress knowing that a capable team is available and ready to respond to any incidents.

It’s important to note that the Crates.io team will continue to own the Crates.io project and will remain focused on improving the service and responding to the community. Ferrous Systems isn’t replacing the team by any stretch, nor is it joining the team. The addition of Ferrous Systems is to support the Crates.io volunteers, free them up to focus on other projects that will advance the service, and ensure they’re not tethered to their laptops by the on-call pager. While these volunteers once had to be on call 24/7, they can now have more autonomy.

Removing this added stress from the volunteers in this group is so important, both for their well-being and for their longevity as active users and contributors in the Rust community. The broader Rust community benefits here as well, from improved Crates.io reliability and faster resolution of any issues that do arise. The Ferrous Systems team has also been tasked with some development work to enhance the reliability of the Crates.io service, which will benefit all users.

Obviously, the importance of Crates.io to Rust and the Rust community cannot be overstated. It’s the foundation for so much great Rust development and is depended on by developers across the globe. As the Rust community continues to grow, we’re happy to see Crates.io evolve and mature to better deliver on Rust’s promise of empowering everyone to build reliable and efficient software.

To learn more about the Rust Foundation, check out our [introductory video](https://www.youtube.com/watch?v=AI4lPN0BqGc) and [recent blog posts](https://foundation.rust-lang.org/posts/), and follow us on [Twitter](https://twitter.com/rust_foundation) and [LinkedIn](https://www.linkedin.com/company/rust-foundation/) to stay up to date.
