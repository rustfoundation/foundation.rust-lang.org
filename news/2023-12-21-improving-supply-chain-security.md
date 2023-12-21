---
title: 'Improving Supply Chain Security for Rust Through Artifact Signing'
byline: 'Adam Harvey, Software Developer, Rust Foundation'
description: 'A high-level explanation of a Rust Foundation initiative to implement signing infrastructure in service of Rust ecosystem supply chain security'
date: 2023-12-21T17:00:00Z
tags:
  - foundation
  - security
  - security initiative
index: true
layout: layouts/news.njk
---


The Rust Foundation is co-ordinating an effort with the Rust Project and other stakeholders to improve supply chain security in the Rust ecosystem. We will start by ensuring that Rust releases and crates can be verified in a secure, low overhead manner and will work directly with affected Rust teams via a series of RFCs.

## Background

There are multiple reasons why we feel that it's the right time to work on this.

The first reason is that there are places where Rust is difficult to use right now. The standard ways of using Rust with `rustup`, `cargo`, and crates.io work well for Rustaceans with unfirewalled access to high speed Internet, but not all are so lucky. Some are behind restrictive firewalls which they are required to use. Some don't have reliable access to the Internet. In cases like these, being able to set up mirrors of Rust releases and crates in a secure way that provides cryptographic guarantees that they are getting the same packages as are provided by the Rust Project — without any risk of tampering — is vital.

Another reason for wanting to be able to better support mirrors is to address cost pressures on Rust. Approximately half of Rust release and crate traffic is from CI providers. Being able to securely distribute Rust releases and popular crates from within CI infrastructure would be mutually beneficial, since it would both allow the Rust Foundation to reallocate budget to other uses and would make Rust CI actions faster and more reliable on those platforms.

Finally, supply chain security is a growing concern, particularly among corporate and government users of Rust. The [Log4j vulnerability][log4j] brought much greater attention to the problems that can occur when a single dependency nested arbitrarily deep in a dependency graph has a critical vulnerability. Many of these users are putting significant resources into better understanding their dependencies, which includes being able to attest that their dependencies came from specific sources like crates.io and rust-lang.org.

## The plan

So, what do we want to do about this?

he Rust Foundation's Technology Team will follow the normal Rust Project RFC process by opening a series of RFCs to implement this project. This plan can — and almost certainly will — change as those RFCs are reviewed, feedback is gathered, experiments are conducted, and new features are implemented in collaboration with the relevant Rust teams.

On a high level, however, this is how we hope things may go from where we are in December 2023.

### PKI

Before anything can be signed, you need something to sign it with. As a result, the first step is to establish public key infrastructure (PKI) for the Rust Project that can be used to sign releases and crate metadata today, and which is extensible enough to allow for other [future possibilities](#future-possibilities).

This PKI would be managed by the Rust Project and (more specifically) its infrastructure team, with support from the Rust Foundation.

Part of defining the PKI includes defining how certificates will be managed, delegated, rotated, and revoked if necessary; getting to consensus on these details will be achieved through the initial PKI RFC.

### Releases

The canonical way Rust users get releases today is via `rustup`. At present, this uses simple HTTPS downloads from Rust Project infrastructure, which uses the system certificate store to validate that `rustup` is connecting to the right servers. While certificate pinning could be employed to mitigate issues with compromised system certificate stores, that doesn't help address problems for those who need to use mirrors.

We intend to create a delegated certificate within the new Rust PKI that can sign release artifacts, and then to work with the `rustup` team to extend `rustup` to be able to verify that artifacts are signed by the release team using the delegated certificate.

### Crates

Similar concerns apply to crates — Rustaceans need to be able to download crates and know that they're getting the crate files that were published to crates.io without modification.

We have a head start here: the crate index (both sparse and Git) includes SHA-256 checksums. This means that we can sign the index while getting the security guarantees that we need, without having to immediately sign crate files themselves. We also have the benefit of [prior work on index signing](https://github.com/rust-lang/rfcs/pull/2474), which we are grateful to be able to learn from.

Our plan is to use another delegated certificate to sign each index entry along with the index as a whole. Doing so allows `cargo` to validate that crates haven't been tampered with after publishing, and also allows the state of the entire index to be checked, making it harder for a malicious mirror to not update a vulnerable crate. This will be done in a layered way that allows for expansion, allowing the chain of trust to be extended as [future work](#future-possibilities) is implemented.

You may have noticed that this doesn't address crate signing by authors; for more detail on that, see the [future possibilities section](#future-possibilities).

## When

We're starting on this work immediately: we'll be opening an RFC for the foundational PKI portion of this plan Real Soon Now™, and following it with RFCs for the release and crates components thereafter.

## Who

The Rust Foundation’s Technology Team are leading this effort in conjunction with the Rust Project, consulting with other domain experts and stakeholders as needed. We're using the [`#tbd-signing` Zulip stream](https://rust-lang.zulipchat.com/#narrow/stream/417663-tbd-signing) to co-ordinate, and welcome feedback and suggestions there.

## Future possibilities

### Crate author signing

A related problem is that of crate signing and attestation: being able to verify that a crate version was published by a specific keyholder, and that it matches a specific (ideally signed) tag in a repository.

We have thoughts on this, and have had preliminary discussions with others who have explored this space, but we don't believe it makes sense to address this until we've addressed the infrastructure level concerns laid out above.

### Integration with other standards

Many other groups are working on cross-language and cross-ecosystem standards to address supply chain security, such as the OpenSSF. We have been — and intend to continue — working with such groups to ensure that our solution is as interoperable as possible with the broader ecosystem of security standards.

## In summary

In the next few months, we intend to start addressing gaps in the Rust supply chain security story by publishing RFCs that will, if accepted, develop and deploy public key infrastructure for the Rust Project, then using that PKI to sign Rust releases and crates in ways that allow them to be mirrored, verified, and used to build secure software in Rust.

We will do so in an open way, both through the normal RFC process and by working directly with the relevant Rust teams to ensure that we develop a secure, maintainable, flexible infrastructure that will serve us for many years to come.

[log4j]: https://www.cisa.gov/news-events/news/apache-log4j-vulnerability-guidance
