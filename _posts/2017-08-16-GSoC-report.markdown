---
layout: post
title:  "Contributions to Homebrew in GSoC '17"
image: https://gauthamgoli.github.io/assets/gsoc-cover.jpg
date:   2017-08-16 11:15:00 +0530
author: GauthamGoli
categories: blog
---
![GSoC 2017]({{ site.url }}/assets/GSoC-logo.png)
![GSoC]({{ site.url }}/assets/GSoC-text.png)



Past couple of months, I have been contributing to [Homebrew](https://github.com/Homebrew/brew) as a [GSoC project](). This post summarizes the work that has been done, and the road ahead.

### Summary

Pull requests that got merged during GSoC work period:

 - [#2610: Add autocorrect method for ComponentsOrder rubocop and tests](https://github.com/Homebrew/brew/pull/2610)
 - [#2628: audit: Detect multiline and interpolated strings in formula desc cop](https://github.com/Homebrew/brew/pull/2628)
 - [#2631: audit: Port audit_homepage method to rubocop and add tests](https://github.com/Homebrew/brew/pull/2631)
 - [#2662: audit: Port audit_text method to rubocop and add tests](https://github.com/Homebrew/brew/pull/2662)
 - [#2664: audit: Port audit_caveats method to rubocop and add tests](https://github.com/Homebrew/brew/pull/2664)
 - [#2755: audit: Port audit_checksum method to rubocop and add tests](https://github.com/Homebrew/brew/pull/2755)
 - [#2776: audit: Fix audit_checksum method's rubocop and add more tests](https://github.com/Homebrew/brew/pull/2776)
 - [#2790: audit: Port audit_legacy_patches method to rubocop and add tests](https://github.com/Homebrew/brew/pull/2790)
 - [#2842: audit: Don't run audit methods when `--only-cops` option is passed](https://github.com/Homebrew/brew/pull/2842)
 - [#2843: audit: Port audit_conflicts method to rubocop and add tests](https://github.com/Homebrew/brew/pull/2843)
 - [#2853: style: Don't run FormulaAuditStrict cops when `brew style foo` cmd is executed ](https://github.com/Homebrew/brew/pull/2853)
 - [#2879: audit: Port audit_options non-strict rules to rubocop and add tests](https://github.com/Homebrew/brew/pull/2879)
 - [#2901: audit: Port audit_options strict rules to rubocop and add tests](https://github.com/Homebrew/brew/pull/2901)
 - [#2905: audit: Port audit_options rules for new formulae to rubocop and add test](https://github.com/Homebrew/brew/pull/2905)
 - [#2906: style: disable NewFormulaAudit cops' execution by default unless specified](https://github.com/Homebrew/brew/pull/2906)
 - [#2911: audit: Port audit_urls partially to rubocop and add corresponding tests ](https://github.com/Homebrew/brew/pull/2911)
 - [#2932: audit: Port audit_urls to rubocop and add corresponding tests Part 2](https://github.com/Homebrew/brew/pull/2932)
 - [#2957: audit: Run style violations check when `--new-formula` is passed](https://github.com/Homebrew/brew/pull/2957)
 - [#2964: audit: Port dependency rules from line_problems to rubocop and add tests](https://github.com/Homebrew/brew/pull/2964)
 - [#2975: audit: Port audit_urls strict rules to rubocop, add tests, autocorrect](https://github.com/Homebrew/brew/pull/2975)
 - [#2976: audit: Port patches audit code to a rubocop and add tests](https://github.com/Homebrew/brew/pull/2976)
 - [#2980: audit: fix bug where `brew audit foo` runs every style check.](https://github.com/Homebrew/brew/pull/2980)
 - [#3012: Add node pattern methods to handle dependency audits in a better way](https://github.com/Homebrew/brew/pull/3012)

Pull requests related to GSoC and still under review:
 - [#2982: audit: Port audit_class to rubocop, add tests and autocorrect (OPEN)](https://github.com/Homebrew/brew/pull/2982)
 - [#2995: audit: Port line_problems to rubocop and add tests part 2 (OPEN)](https://github.com/Homebrew/brew/pull/2995)

### Credits

Until next time and May the source be with you!
