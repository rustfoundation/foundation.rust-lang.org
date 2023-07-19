---
date: 2023-07-19T20:03:00Z
title: My first three months at the Rust Foundation
description: A recap of my work at the Rust Foundation and accomplishments so far
byline: Tobias Bieniek, crates.io team co-lead and Rust Foundation software engineer
tags:
  - foundation
layout: layouts/news.njk
---

In May 2022, I received an exciting email from the Rust Foundation:

> […] you have been provisionally selected to be one of our first Rust Foundation Fellows

As a contributor to the Rust project for many years, receiving this grant money allowed me to focus more of my time on the open source volunteer work I enjoy.

Fast-forward one year, and that fellowship grant has transformed into a full-time role at the Rust Foundation. My primary focus now revolves around the maintenance and feature development for [crates.io](https://crates.io), the official Rust package registry.

As I reflect on my first three months in this position, I want to take this opportunity to highlight some of the significant milestones I have achieved:

## Improved API tokens

One of the most noticeable achievements during this period has been the substantial improvements made to API tokens on crates.io.

With the introduction of token scopes, our users can now restrict their API tokens to specific crates and operations. For instance, only allowing a token to publish new versions of a specific crate.

In addition, I implemented optional token expiration, providing users with the ability to configure API tokens to automatically expire at a designated time.

To delve into more details, please refer to the [Rust Blog](https://blog.rust-lang.org/2023/06/23/improved-api-tokens-for-crates-io.html).

## The rust-version field

Crate authors have long been able to specify the minimum supported Rust version for their crate using the `rust-version` field in the `Cargo.toml` file. Previously, `cargo` had to read the `Cargo.toml` file of the downloaded crates to determine potential compatibility issues with the Rust version being used.

Working in collaboration with [Cassaundra Smith](https://github.com/cassaundra) from [Futurewei](https://www.futurewei.com), we implemented a solution that reads the `rust-version` field from the `Cargo.toml` file upon crate upload. The content is then stored in our database and the crate index, enabling `cargo` to eventually utilize it for dependency resolution purposes. To ensure comprehensive support, I also backfilled our database with this field's information for previously uploaded crate versions.

## Resolving data inconsistencies

As expected, crates.io has encountered its fair share of bugs and inconsistencies since its inception in 2014. Over the past few months, we have been diligently addressing these issues, focusing on resolving inconsistencies between the database, crate index, and crate storage on S3.

These issues ranged from crates that were yanked in the database (but not in the index), over releases with invalid SemVer versions, to crates that were deleted from S3 for privacy-related concerns but were still in the database.

While our work here is not finished yet, we have cleaned up a lot of these inconsistencies over the past couple of months. We also started treating our database as the primary source of truth, instead of saving some metadata subset in the database and another subset in the index.

## The "sparse" index

Initially, utilizing a Git repository for the crate index seemed promising, showcasing several advantageous properties. However, as time went on, the index update process became increasingly time-consuming for everyone using `cargo`. This slowdown was primarily attributed to the need to download all the commits associated with each released version.

To tackle this challenge, the `cargo` team initiated experiments with a solution called the "sparse" index. This approach involves using HTTP requests for only the relevant dependencies in individual projects, instead of downloading the entire index with every crate and version ever released.

[Arlo Siemsen](https://github.com/arlosi) from Microsoft did a lot of the work on `cargo` and crates.io to support this on both sides. I have done my best to support his efforts by providing code reviews and helping steer the development efforts in the right direction.

Starting with Rust 1.70, the "sparse" index has become the default method for managing dependencies. Although we encountered some obstacles during the development phase, the feature is now functioning very well.

## Preventing accidental leakage of secrets

While working with the crates.io codebase, I noticed that several structs were using derived `Debug` implementations while containing secret values such as database credentials and AWS keys. Recognizing the potential security implications, I introduced the [secrecy](https://crates.io/crates/secrecy) crate to our codebase. This allowed us to utilize its `SecretString` struct for handling system credentials and other sensitive information, effectively preventing accidental exposure in logs.

## Fixing versions with build metadata

The handling of "build metadata" in SemVer versions, denoted by the `xxx` part of a version number like `1.0.0-beta.1+xxx`, required attention due to certain flaws in our implementation.

Firstly, we discovered that we had permitted crate authors to publish `1.0.0+x` versions even if `1.0.0+y` already existed. However, `cargo` treats these versions as equivalent since they only differ in the build metadata part of the version number. Consequently, this inconsistency resulted in errors related to invalid download checksums and other cryptic errors. While the SemVer specification interpretation sparked a lengthy debate in the crates.io issue tracker, the only pragmatic solution for this was restricting this on the crates.io side, since older versions of `cargo` can't easily be fixed to support this.

Secondly, we noticed that some internet servers interpret a `+` character in the URL as a space character, namely Amazon S3, our crate file storage provider. While `crates.io` interprets `+` as `+`, S3 thinks of it differently, and we discovered that we had been saving the files to S3 with space character in their file names. After a lengthy investigation I came up with a solution to fix this issue, and the multistep process of this fix has started last week. We are now escaping `+` characters as `%2B` before we return any S3 or CDN URLs and started to move the S3 files to their correct paths.

## Support for the crates.io support

Until recently, [Carol (Nichols || Goulding)](https://github.com/carols10cents) had primarily managed the [help@crates.io](mailto:help@crates.io) support email address on her own. Since I was now getting paid to work on crates.io, I offered to support her with this too.

My first task was updating the (private) "crates.io operations guide", which also contains information on how to handle common support requests, like people requesting crate transfers or crate deletions due to privacy-related concerns.

While the support volume is fortunately still limited to only a couple of requests per day, this number quickly adds up when you can only handle these requests once in a while. I've committed myself to checking for new support emails each morning now, and with Carol covering the US timezones, we should be able to respond to your requests in a somewhat timely manner now.

## Dependencies

We have been using [Renovate](https://github.com/renovatebot/renovate) on the crates.io repository for quite a while already, and it is a great way to keep all of our dependencies up-to-date. Still, sometimes a dependency update can't just be merged because it is breaking our continuous integration checks in some way. When I started my job in April we had quite a few blocked dependency upgrades due to such issues. One week later, I managed to upgrade us to the latest version of everything again.

During this time, I also discovered [cargo-deny](https://github.com/EmbarkStudios/cargo-deny), and later incorporated it into our CI checks. This tool assists in identifying problematic dependencies in our dependency tree, including those with incompatible licenses or active security advisories. Upon its implementation, we promptly addressed five issues it had identified.

## Closing thoughts

While it often feels like each week yields only modest progress, my [work log](https://blog.pragmaticengineer.com/work-log-template-for-software-engineers/) has already grown to four pages and includes a lot more bullet points than I could fit in this blog post. I'm also pretty sure that this new job significantly increased my [imposter syndrome](https://blog.rust-lang.org/inside-rust/2022/04/19/imposter-syndrome.html), but since people keep telling me that they are happy with the work that I'm doing, I guess I'm doing alright…

Finally, I would like to thank the [OpenSSF's Alpha-Omega Initiative](https://openssf.org/community/alpha-omega/) and the [JFrog](https://jfrog.com/blog/jfrog-joins-rust-foundation-as-platinum-member/) for supporting the Rust Foundation security initiative, which enabled me to get this job and work on a lot of the things above.
