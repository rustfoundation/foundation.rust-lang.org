---
title: A Note on Data Retention & Data Privacy Standards From the crates.io Team
byline:
description: >-
  This blog post is a guest contribution from the crates.io team, intended to
  update the community on our shared, general approach if either the Rust
  Foundation or crates.io teams ever receive a legally-binding request for data.
date: 2023-06-15T14:00:00Z
tags:
  - guest blog series
index: false
layout: layouts/news.njk
---
On May 24th, [<u>PyPI announced that they had received multiple subpoenas</u>](https://blog.pypi.org/posts/2023-05-24-pypi-was-subpoenaed/) from the United States Department of Justice requesting PyPI user data. Since then, members of the Rust community have reached out to ask if any similar requests have been received by the crates.io team, and have inquired about the policies of crates.io, the Rust Project, and the Rust Foundation should such a request be received.

### **The crates.io team members and the Rust Foundation can confirm that neither group has received requests for private crates.io user data as of this post (June 15, 2023).**

The crates.io team intends to work with the Rust Foundation and legal counsel to add an amendment to the [<u>existing Rust privacy policy governing crates.io and other official Rust sites and applications</u>](https://foundation.rust-lang.org/policies/privacy-policy/). This amendment will specify the process that will be followed in the event such a request is received from law enforcement or a government agency.&nbsp;

### While we are unable to provide specifics on this amendment until we have had more time to confer with legal counsel, our guiding principles in the interim will be as follows:

1. We will only respond to legal requests made to the Rust Foundation concerning crates.io that are complete, correct, and legally-binding.
2. The crates.io team will provide only the minimum data required by the request.
3. The crates.io team will communicate the nature of the request and what was provided to the maximum extent allowed by the request and law, while respecting the anonymity of those involved.
4. If the request allows us to notify the subject(s) of the request and we have contact details for the subject(s), we will notify them directly of what data was provided. We will also consult with our legal counsel about the potential ways we could publicly, and anonymously, report any legally-binding requests for data we might receive in the future.

The crates.io team would also like to commend PyPI and the Python Software Foundation for the way they handled this request. We will seek to emulate their approach as closely as we can should we ever find ourselves in this position.&nbsp;

## Our Existing Data-Retention and Privacy Policy

Below, you’ll find a summary of the existing privacy policy followed by the Rust Foundation, crates.io, and associated Rust Project services. While this information is discoverable via the Rust Foundation privacy policy, we are sharing it here to reinforce the limited data we collect and the strict parameters around its retention:

### **crates.io Receives the Following Data From its Users Upon Log In:&nbsp;**

* As a GitHub account is required for log-in, crates.io receives users’ GitHub usernames, avatars, and any email addresses publicly listed in their GitHub public profile.&nbsp;
* As a verified email address is required to publish a crate, we receive any public email address associated with your GitHub account and any email a user enters directly into crates.io. We only use your email address to contact you about your account.
* In order to associate user accounts with the appropriate organizations and teams, we also collect users’ organization memberships and the teams within them from GitHub&nbsp;
* When you visit crates.io or interact with crates.io using Cargo, we receive your IP address, user-agent header, and request path as part of our standard server logs. Log entries for some authenticated requests, such as publishing a crate, also contain your crates.io account. These logs are stored for 1 year.
* Upon visiting static.crates.io (where the crate files that Cargo downloads are hosted), we receive your IP address, user-agent header, referer header, and request path as part of our standard server logs. These logs are stored for 1 year.&nbsp; Cargo downloads are not associated with your crates.io username, as we do not store that information.
* All crates on crates.io are public, including the list of crate owners’ usernames and the crate upload date. Anyone may view or download a crate’s contents. Because of the public nature of crates.io, any personal data you might include in a Cargo.toml file uploaded to a crate is publicly available.&nbsp;
* Due to its public nature, be aware if you include any private information in a crate that information may be indexed by search engines or used by third parties. Sensitive information should not be included in a crate file.

### **Rust Foundation Data-Retention Policies:&nbsp;**

* The Rust Foundation retains personal data only for as long as is necessary, or as needed to provide users with the Foundation’s services.
* If a user wishes for their personal information to be removed from a Foundation service, they may request deletion of that information.
* The Rust Foundation will retain and use user information only to the extent necessary to comply with our legal obligations.

[<u>Click here</u>](https://foundation.rust-lang.org/policies/privacy-policy/#data-retention) to read the full language of the policies listed above.&nbsp;

---

## Summary

The crates.io team will be meeting with the Rust Foundation and legal counsel to update and expand our shared data-retention policy. Our goal will be to add an amendment on how we would operate if a legally-binding request for data is issued and determine opportunities to minimize the level of data we retain without compromising the management of the Rust infrastructure. If you have feedback or specific concerns about the types of private user data we retain that might be available to a legally binding request, please email that feedback to [<u>help@crates.io</u>](mailto:help@crates.io) and/or [contact@rustfoundation.org](mailto:contact@rustfoundation.org).

We will post updates on our progress in the [<u>"Data-Retention Policy Amendment Updates" topic in the public foundation Zulip stream</u>](https://rust-lang.zulipchat.com/#narrow/stream/335408-foundation/topic/Data-Retention.20Policy.20Amendment.20Updates). This work will likely take multiple months of coordination between all groups.

The existing Rust Foundation and crates.io privacy and data-retention policy can be found [<u>here</u>](https://foundation.rust-lang.org/policies/privacy-policy/).&nbsp;

Signed,

The crates.io team (in collaboration with the Rust Foundation)