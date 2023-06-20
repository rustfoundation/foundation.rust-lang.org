---
layout: news
title: Better API tokens for crates.io
description: crates.io API tokens can now have an optional expiry date and be scoped to certain actions and crates
byline: Tobias Bieniek, crates.io team co-lead and Rust Foundation software engineer
date: 2023-06-21
tags:
   - crates.io
   - security
   - guest blog series
---

A few weeks ago the [crates.io team](https://www.rust-lang.org/governance/teams/crates-io) announced on the [Inside Rust](https://blog.rust-lang.org/inside-rust/2023/05/09/api-token-scopes.html) blog that the "API token scopes" feature was now in a public beta testing period.

Let me quote from that blog post to give you a quick idea of what "API token scopes" are:

> Roughly three years ago [Pietro Albini](https://github.com/pietroalbini) opened an RFC called ["crates.io token scopes"](https://github.com/rust-lang/rfcs/pull/2947). This RFC described an improvement to the existing API tokens, that everyone is using to publish crates to the [crates.io](https://crates.io/) package registry. The proposal was to make it possible to restrict API tokens to 1) certain operations and 2) certain crates.
>
> Unfortunately, the crates.io team members were quite busy at the time, so it took a while for this proposal to get accepted. To be precise, during the [EuroRust](https://eurorust.eu) conference in October 2022 we talked about the RFC again and after a few modifications the RFC was moved into FCP status and then finally merged.
>
> The implementation was started soon after, but was paused again due to other priorities at the time. Fortunately, I was lucky enough to get one of the software engineering jobs at the [Rust Foundation](https://rustfoundation.org/), so in early April the development continued [...].

Since this blog post we have enabled the new API token creation page for all users, and we have now also implemented optional token expiration  as well:

![Screenshot of the "New API Token" page](/img/news/2023-06-21-better-api-tokens-for-crates-io/new-api-token-page.png)

Similar to when you create an API token for GitHub, you can choose to not have an expiry date at all, use one of the presets or even choose a custom expiration date.

As described in the Inside Rust blog post, the Scopes and Crates sections allow you to restrict the token to e.g. only be able to publish *new* versions of existing crates. In the example screenshot above this would be the `serde` crate and any other crate starting with `serde-`. Note that you still need to be an owner of the crate to publish new versions for it... 😉

We recommend using these new restriction when you use CI systems to release new versions of your crates. If a token is accidentally leaked you don't risk a full account takeover anymore, and instead the damage is contained to the crate that the token is restricted to.

You can go to <https://crates.io/settings/tokens/new> now and create a new API token scoped to the operations and crates you want!

If you notice any issues, or if you have any questions don't hesitate to find us on [Zulip](https://rust-lang.zulipchat.com/#narrow/stream/318791-t-crates-io/topic/token.20scopes) or open an issue on [GitHub](https://github.com/rust-lang/crates.io/issues/new/choose).

Finally, the crates.io team would like to thank the [OpenSSF's Alpha-Omega Initiative](https://openssf.org/community/alpha-omega/) and the [Rust Foundation member JFrog](https://jfrog.com/blog/jfrog-joins-rust-foundation-as-platinum-member/) for funding the Rust Foundation security initiative, which enabled us to implement these features and perform a lot of other security-related work on the crates.io codebase.
