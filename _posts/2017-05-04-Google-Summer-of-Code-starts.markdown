---
layout: post
title:  "GSoC '17 starts!"
image: https://gauthamgoli.github.io/assets/GauthamGoli.jpg
date:   2017-05-04 21:30:00 +0530
categories: blog
---
![GSoC 2017]({{ site.url }}/assets/GSoC-logo.png)
![GSoC]({{ site.url }}/assets/GSoC-text.png)



I'm psyched. After a long wait, the GSoC 2017 projects have been announced and I'm in. I will be working with Homebrew.
Homebrew is a package management software for macOS, analogous to `apt` on debian machines and `yum` on rpm-based systems.
Homebrew is one of the most widely used developer tools on macOS. Nothing is more satisfying and exciting to me than knowing that the code I write is going to be used by hundreds of thousands of developers and will make the lives of millions of users easier.

### Project

The title of my GSoC project is 'Porting `brew audit` rules to RuboCop'. Although 'porting' may sound like a trivial task,
 as the work has already been done and there is no creative process involved, I would say its the contrary in this project. `brew audit`
 command checks Homebrew 'Formulae' for their conformation with Homebrew's coding style using regular expressions
 to match the relevant methods , statements, etc. One can easily imagine, it gets pretty complicated soon enough to handle edge cases evident
  by looking at source of `audit` and its complexity, which can
 otherwise be handled elegantly using a static code analyser by creating Abstract Syntax Tree (AST) representation of the parsed code.

 Without travail the gist of my work is to:
  - Integrate a static code analyser with brew to run custom cops avoiding extra end user configuration
  - Develop a DSL for developers/contributors to easily write brew-specific custom cops
  - Port existing rules to custom cops

This is going to help the developers and contributors of Homebrew to ship code more productively (RuboCop has editor integration: Real time highlighting of
audit rule violations! ) and I would have hopefully become efficient at reading complex code written by others.

### Credits

It is customary to take part in Google Summer of Code being a member of SDSLabs. I am thankful to colleagues and seniors at SDSLabs and mentors at Homebrew.

Until next time and May the source be with you!
