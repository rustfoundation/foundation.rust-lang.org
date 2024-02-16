---
title: Zama and the Future of Privacy Applications Using Rust
byline: Rand Hindi, CEO and Co-Founder of Zama
description: "A Rust Foundation Guest Blog contributed by Silver Member, Zama.\_"
date: 2024-02-19T12:00:00Z
tags:
  - guest blog series
index: false
layout: layouts/news.njk
---
Welcome to another installment in the Rust Foundation [<u>guest blog series</u>](https://foundation.rust-lang.org/tags/guest%20blog%20series/), written by members of the Rust Foundation and our community. This guest blog was contributed by Rand Hindi, CEO and Co-Founder of [Zama](https://www.zama.ai/) – a Rust Foundation Silver Member organization. Zama is a cryptography company building an open source framework for homomorphic encryption: a new data encryption approach that enables users to compute on encrypted data.&nbsp;

Read on to learn more about how Zama is involved with the Rust community and specifically about TFHE-rs: Zama’s cryptographic library.&nbsp;

---

Keeping our sensitive data confidential is paramount at a time when data leaks seem to happen at an alarming rate. At the same time, many users provide their email addresses, usernames, and other even more sensitive data online without a second thought. It’s as though we accept that data breaches happen and, on some level, many seem okay with taking that risk. At Zama, however, we don’t believe that the idea of private data sharing is out of reach.

With Fully Homomorphic Encryption (FHE), guaranteeing privacy is no longer a pipedream. This powerful technology enables Zama to deliver on a long-held promise to guarantee the encrypted state of that data– even during third party processing.

# Zama and Rust

Zama specializes in building open-source cryptographic tools to help developers use homomorphic encryption without having to know anything about cryptography. We extend a specific encryption scheme called TFHE, or [<u>Fully Homomorphic Encryption over the Torus</u>](https://www.zama.ai/post/tfhe-deep-dive-part-1). The first implementation of the TFHE scheme was only for boolean circuits, but Zama’s state-of-the-art [<u>TFHE-rs</u>](https://www.zama.ai/post/announcing-tfhe-rs) extends the original capabilities of TFHE to support programmable bootstrapping over integers, making it the fastest implementation of a Fully Homomorphic Encryption (FHE) scheme to date.

Now, Zama is working on speeding up FHE to make it practical for most use cases, both for web2 and web3 applications.&nbsp;

Implementing TFHE in Rust was a no-brainer. We began writing in Rust in 2019 – this was a serendipitous choice as we selected it based on security, performances and obviously, because it was one of the preferred languages of our team members. Since then, Rust has been recognized for its focus on security and high-level performance. Retrospectively, Rust is the natural choice for implementing cryptographic schemes.

# TFHE-rs

Today, we continue to develop products with Rust as a backbone. The [<u>TFHE-rs library</u>](https://github.com/zama-ai/tfhe-rs) is Zama’s low-level library, and everything we’re building is done on top of it. Building it in Rust gives us extra confidence to keep moving the FHE space forward.&nbsp;

TFHE-rs provides various functions for performing homomorphic operations on encrypted data, ensuring that it remains confidential throughout the computation process. With TFHE-rs, researchers, developers, and others can use the library to suit their purposes without an advanced understanding of cryptography.

Largely thanks to Rust, TFHE-rs is the fastest public implementation of the TFHE scheme. As shown below, execution time is vastly improved compared to other schemes. Visit our website for a complete list of [<u>benchmarks</u>](https://docs.zama.ai/tfhe-rs/getting-started/benchmarks) for our Rust implementation of TFHE.

# Doubling Down on the Rust Community&nbsp;

Earlier in 2023, we renewed our Rust Foundation Membership. We also supported the [<u>Rust Community Grants Program</u>](https://foundation.rust-lang.org/grants/). We decided to do this because, at Zama, we are invested in what the Rust community will build on top of what we have created: an accessible framework of products to help all developers build applications that are private by default.

In an effort to expand our community and attract more talented Rust developers, we launched our [<u>Bounty and Grant Program</u>](http://github.com/zama-ai/bounty-and-grant-program), which allows our open-source community to play an active role in improving our technologies. Because our developers and contributors largely work in Rust, we’re finding answers to new and complex problems together that we may have not discovered working alone. Since then, the program has grown through 5 seasons with our commitment not only to doing work in the open, but actively involving the community in what we do. The program has been a great way to connect with our community and find people who want to work with us. We are thrilled to see where this Bounty Program leads Zama next. As an example, in this season of the Zama Bounty Program, we are challenging contributors to create an implementation of an SQL encrypted query on a clear database using TFHE-rs.

We are happy to see people from the Rust community involved in what we do at Zama, as they help us push the limits of what is possible with FHE. We envision a future where Rust and Zama communities collaborate, with privacy in mind, to build the products we actually want to use.

As a forward-thinking, privacy-centric company, we’re very happy with the security and flexibility of Rust. The amount of support available through the community and the Rust Foundation allows us to focus on the privacy built into our products instead of worrying about the underlying functionality. The secure nature of the language, the speed it affords, and the fact that it makes development fun are all reasons we love implementing Rust.

> ### **Dr. Rand Hindi, CEO at** [**<u>Zama</u>**](https://www.zama.ai/)
>
> Dr. Rand Hindi is an entrepreneur and investor in over 50 companies across AI, blockchain, hardware, and biotech. He started coding at the age of 10, founded a social network at 14, and did a Ph.D. at 21. He then created Snips, a privacy-centric AI startup that was acquired by Sonos.
>
> Dr. Hindi frequently speaks and writes about blockchain, AI, privacy, and homomorphic encryption.

---

Our sincere thanks to Zama for their Rust Foundation Silver membership and for their generous support of our Community Grants Program.&nbsp;

If your organization would like more information on Rust Foundation Membership, please visit our [<u>membership page</u>](https://foundation.rust-lang.org/members/) and email us at [<u>membership@rustfoundation.org</u>](mailto:membership@rustfoundation.org) to inquire.&nbsp;

Click here to learn more about the Community Grants Program and email us at [<u>grants@rustfoundation.org</u>](mailto:grants@rustfoundation.org) to get involved.&nbsp;