---
date: 2023-07-01T12:00:00Z
title: My first three months at the Rust Foundation
description: Time flies when you're having fun… at the Rust Foundation
byline: Tobias Bieniek, crates.io team co-lead and Rust Foundation software engineer
tags:
  - foundation
layout: layouts/news.njk
---

Back in May 2022 I got an email from the Rust Foundation saying:

> […] you have been provisionally selected to be one of our first Rust Foundation Fellows

Fast-forward roughly one year, and that fellowship grant has transformed into a full-time job at the Rust Foundation, where my primary focus now is maintenance and feature development for [crates.io](https://crates.io), the official Rust package registry.

I started this job in April, and now, three months later, I thought it would be a good opportunity to recap on what I've worked on since then:

## API token scopes and expiration

Let's start with the most visible achievement first: API tokens on crates.io are now a lot more powerful and secure than before.

With the introduction of token scopes our users can now restrict their API tokens to specific crates and operations, for instance only allowing a token to publish new versions of a specific crate.

Shortly after, I've also implemented optional token expiration, meaning that new API tokens can be configured to automatically expire at a certain point in time.

You can also read more details about this on the [Rust Blog](https://blog.rust-lang.org/2023/06/23/improved-api-tokens-for-crates-io.html).

## The rust-version field

Crate authors have for quite some time been able to specify the minimum supported Rust version for their crate using a `rust-version` field in the `Cargo.toml` file. Up until a couple of weeks ago `cargo` had to read the `Cargo.toml` file of the downloaded crates to figure out if you might be using a Rust version that is incompatible with the downloaded crate.

In collaboration with [Cassaundra Smith](https://github.com/cassaundra) from [Futurewei](https://www.futurewei.com) I've worked on reading this field from the `Cargo.toml` file when new crates are uploaded, and then saving its content to our database and the crate index, so that `cargo` can eventually use it for dependency resolution purposes. Since this only worked for newly uploaded versions, I have also written a bit of code to backfill our database from the existing versions that were already uploaded to crates.io before we implemented support for this field.

## Data inconsistencies

Unsurprisingly, crates.io has not been bug-free since the first line of code was written in 2014. This has resulted in a couple of interesting inconsistencies between the database, the crate index and the crate storage on S3. This ranged from versions that were yanked in the database, but not in the index, over versions with invalid SemVer versions, to crates that were deleted from S3 for privacy-related concerns, but were still in the database.

While our work here is not finished yet, we have cleaned up a lot of these inconsistencies over the past couple of months. We also started treating our database as the primary source of truth, instead of saving some metadata subset in the database and another subset in the index.

## The "sparse" index

Using a git repository for the crate index seemed like a good idea at first, and it certainly has some nice properties, but as you may have noticed, the index update started to take quite some time in the past year. The reason for this is that every released version creates a commit in that index repository and downloading all of these commits takes time.

The `cargo` team started to experiment with a solution to this issue by using HTTP requests for only the dependencies that it cares about in the individual project, instead of downloading the index of every crate and version that was ever released.

[Arlo Siemsen](https://github.com/arlosi) from Microsoft did a lot of the work on `cargo` and crates.io to support this on both sides. I've tried to support his efforts as best as I could by providing code reviews and steering the development efforts in the right direction.

Rust 1.70 has now enabled the "sparse" index as the default way of working with dependencies, and while we initially had some issues to overcome during the development of this feature, it now seems to work very well.

## Preventing accidental leakage of secrets

While working with the crates.io codebase, I noticed that quite a few structs were using derived `Debug` implementations, but were also containing secret values, like database credentials and AWS keys, that should not be printed in any logs. To prevent this from becoming an actual security issue in the future I introduced the [secrecy](https://crates.io/crates/secrecy) crate to our codebase and started using its `SecretString` struct for our various system credentials and other secrets.

## Fixing versions with build metadata

"Build metadata" in SemVer versions means the `xxx` part in a version number like `1.0.0-beta.1+xxx`. Since this is a relatively rarely used feature, it took a while for anyone to notice that our implementation for this was slightly broken in various ways.

One way it was broken was that we allowed crate authors to publish `1.0.0+x` if `1.0.0+y` already exists. `cargo` however treats these versions as equivalent since they only differ in the build metadata part of the version number. This was manifesting in errors about invalid download checksums and other cryptic errors. While there was a long debate in the crates.io issue tracker on how the SemVer specification should be interpreted, the only pragmatic solution for this was restricting this on the crates.io side, since older versions of `cargo` can't easily be fixed to support this.

The second interesting fact about such versions is that some internet servers interpret a `+` character in the URL as a space character, namely Amazon S3, our crate file storage provider. While `crates.io` interprets `+` as `+`, S3 thinks of it differently, and we discovered that we had been saving the files to S3 with space character in their file names. After a lengthy investigation I came up with a solution to fix this issue, and the multistep process of this fix has started last week. We are now escaping `+` characters as `%2B` before we return any S3 or CDN URLs and started to move the S3 files to their correct paths.

## Support for the crates.io support

[Carol (Nichols || Goulding)](https://github.com/carols10cents) had essentially been the only person behind the [help@crates.io](mailto:help@crates.io) support email address for some time. Since I was now getting paid to work on crates.io, I offered to support her with this too.

My first task was updating the (private) "crates.io operations guide", which also contains information on how to handle common support requests, like people requesting crate transfers or crate deletions due to privacy-related concerns.

While the support volume is fortunately still limited to only a couple of requests per day, this number quickly adds up when you can only handle these requests once in a while. I've committed myself to checking for new support emails each morning now, and with Carol covering the US timezones, we should be able to respond to your requests in a somewhat timely manner now.

## Dependencies

We have been using [Renovate](https://github.com/renovatebot/renovate) on the crates.io repository for quite a while already, and it is a great way to keep all of our dependencies up-to-date. Still, sometimes a dependency update can't just be merged because it is breaking our continuous integration checks in some way. When I started my job in April we had quite a few blocked dependency upgrades due to such issues. One week later, I managed to upgrade us to the latest version of everything again.

I also discovered [cargo-deny](https://github.com/EmbarkStudios/cargo-deny) during that time, and later added it to our CI checks. This tool helps us find bad dependencies in our dependency tree, either with incompatible licenses or with active security advisories. When I initially introduced it, it had immediately found five issues that we needed to fix.

## Closing thoughts

While each weeks feels like I've accomplished very little, my [work log](https://blog.pragmaticengineer.com/work-log-template-for-software-engineers/) is now four pages long and includes a lot more points than I could fit in this blog post. I'm also pretty sure that this new job significantly increased my [imposter syndrome](https://blog.rust-lang.org/inside-rust/2022/04/19/imposter-syndrome.html), but since people keep telling me that they are happy with the work that I'm doing, I guess I'm doing alright…

Finally, I would like to thank the [OpenSSF's Alpha-Omega Initiative](https://openssf.org/community/alpha-omega/) and the [JFrog](https://jfrog.com/blog/jfrog-joins-rust-foundation-as-platinum-member/) for funding the Rust Foundation security initiative, which enabled me to get this job and work on a lot of the things above.
