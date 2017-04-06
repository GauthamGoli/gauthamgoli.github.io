---
layout: post
title:  "Google Summer of Code starts!"
date:   2017-05-04 21:30:00 +0530
categories: blog
---

I'm psyched. After a long wait, the GSoC 2017 projects have been announced and I'm in. I will be working with Homebrew.
Homebrew is a package management software for macOS, analogous to `apt` on debian machines.

### Project

The title of my GSoC project is 'Porting `brew audit` rules to RuboCop'. Although 'porting' may sound like a trivial task,
 as the work has already been done and there is no creative process involved, I would say its the contrary in this project. `brew audit`
 command checks the Homebrew 'Formulae' for their conformation with Homebrew's coding style. Until now regular expressions have been used
 to match the relevant methods , statements, etc. One can easily imagine, it gets pretty complicated soon enough to handle edge cases evident
  by looking at source of `audit` and its complexity, which can
 otherwise be handled elegantly using a static code analyser. Without travail the gist of my work is to:
  - Integrate RuboCop with brew to run custom cops avoiding extra end user configuration
  - Develop a DSL for developers/contributors to easily write brew-specific custom cops
  - Port existing rules to custom cops

This is going to help the developers and contributors of Homebrew to ship code more productively (RuboCop has editor integration: Real time highlighting of
audit rule violations! ) and I would have hopefully become efficient at reading complex code written by others.

### Credits

It is customary to take part in Google Summer of Code being a member of SDSLabs. I am thankful to colleagues and seniors at SDSLabs and mentors at Homebrew.

Until next time. May the source be with you!