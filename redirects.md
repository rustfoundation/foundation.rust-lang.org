---
# Courtesy of and Ref: https://github.com/11ty/eleventy/issues/510#issuecomment-824104799
# 
# This file does hijinx with the "pagingation" system to generate many small pages from one set of data...
# and uses that do to redirects from some URLs to others.
# We use this to try to keep old links working.
#
# There's limited power to this approach (it only works for specific pages listed; it can't glob),
# but those are limitations inherent to an approach that works via static site gen, rather than via server configuration.
# The related upside of an approach that works via static site gen is the portability.
pagination:
  data: redirects
  size: 1
  alias: redirect
# Add your redirection tuples to this list!
redirects:
  - {"from": "/board/", "to": "/about/"}
  - {"from": "/posts/", "to": "/news/"}
  - {"from": "/posts/2021-02-08-hello-world/", "to": "/news/2021-02-08-hello-world/"}
  - {"from": "/posts/2021-03-18-introducing-bobby-holley/", "to": "/news/2021-03-18-introducing-bobby-holley/"}
  - {"from": "/posts/2021-03-18-introducing-tyler-mandry/", "to": "/news/2021-03-18-introducing-tyler-mandry/"}
  - {"from": "/posts/2021-03-25-introducing-mark-rousskov/", "to": "/news/2021-03-25-introducing-mark-rousskov/"}
  - {"from": "/posts/2021-03-25-introducing-nell-shamrell-harrington/", "to": "/news/2021-03-25-introducing-nell-shamrell-harrington/"}
  - {"from": "/posts/2021-04-08-introducing-florian-gilcher/", "to": "/news/2021-04-08-introducing-florian-gilcher/"}
  - {"from": "/posts/2021-04-08-introducing-peixin-hou/", "to": "/news/2021-04-08-introducing-peixin-hou/"}
  - {"from": "/posts/2021-04-15-introducing-jane-lusby/", "to": "/news/2021-04-15-introducing-jane-lusby/"}
  - {"from": "/posts/2021-04-15-introducing-shane-miller/", "to": "/news/2021-04-15-introducing-shane-miller/"}
  - {"from": "/posts/2021-04-22-introducing-josh-stone/", "to": "/news/2021-04-22-introducing-josh-stone/"}
  - {"from": "/posts/2021-04-22-introducing-lars-bergstrom/", "to": "/news/2021-04-22-introducing-lars-bergstrom/"}
  - {"from": "/posts/2021-04-29-introducing-joel-marcey/", "to": "/news/2021-04-29-introducing-joel-marcey/"}
  - {"from": "/posts/2021-09-21-member-spotlight-open-source-security-software/", "to": "/news/2021-09-21-member-spotlight-open-source-security-software/"}
  - {"from": "/posts/2021-10-01-member-spotlight-parastate/", "to": "/news/2021-10-01-member-spotlight-parastate/"}
  - {"from": "/posts/2021-10-07-member-spotlight-knoldus/", "to": "/news/2021-10-07-member-spotlight-knoldus/"}
  - {"from": "/posts/2021-10-18-crates-io-oncall-ferrous-systems/", "to": "/news/2021-10-18-crates-io-oncall-ferrous-systems/"}
  - {"from": "/posts/2021-10-26-member-spotlight-tag1/", "to": "/news/2021-10-26-member-spotlight-tag1/"}
  - {"from": "/posts/2021-11-04-rust-foundation-ama-launch/", "to": "/news/2021-11-04-rust-foundation-ama-launch/"}
  - {"from": "/posts/2021-11-17-introducing-rebecca-rumbul/", "to": "/news/2021-11-17-introducing-rebecca-rumbul/"}
  - {"from": "/posts/2021-12-06-love-for-rust-at-reinvent/", "to": "/news/2021-12-06-love-for-rust-at-reinvent/"}
  - {"from": "/posts/2021-12-13-member-spotlight-automata/", "to": "/news/2021-12-13-member-spotlight-automata/"}
  - {"from": "/posts/2021-12-15-take-the-state-of-rust-survey/", "to": "/news/2021-12-15-take-the-state-of-rust-survey/"}
  - {"from": "/posts/2021-12-20-member-spotlight-spectral/", "to": "/news/2021-12-20-member-spotlight-spectral/"}
  - {"from": "/posts/2022-01-06-happy-new-year-rustaceans-from-bec/", "to": "/news/2022-01-06-happy-new-year-rustaceans-from-bec/"}
  - {"from": "/posts/2022-01-31-survey-rust-foundation-community-grants-program/", "to": "/news/2022-01-31-survey-rust-foundation-community-grants-program/"}
  - {"from": "/posts/2022-02-02-farewell-florian/", "to": "/news/2022-02-02-farewell-florian/"}
  - {"from": "/posts/2022-02-08-member-spotlight-zama/", "to": "/news/2022-02-08-member-spotlight-zama/"}
  - {"from": "/posts/2022-02-16-member-spotlight-simplabs/", "to": "/news/2022-02-16-member-spotlight-simplabs/"}
  - {"from": "/posts/2022-03-08-member-spotlight-1password/", "to": "/news/2022-03-08-member-spotlight-1password/"}
  - {"from": "/news/2022-04-11-member-spotlight-tangram/", "to": "/news/2022-04-11-member-spotlight-tangram-vision/"}
  - {"from": "/news/cloud-compute-program-update/", "to": "/news/2022-06-09-cloud-compute-program-update/"}
# The "permalink" attribute determines where the output page will be located.
permalink: "{{ redirect.from }}"
# The "redirect" layout just has a small html header with the meta tags that do redirection.
layout: layouts/redirect.njk
---
(the content can be left blank; it's entirely the frontmatter doing the work here.)