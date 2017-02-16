---
layout: post
title:  "Contributing to Homebrew"
date:   2017-02-12 20:53:30 +0530
categories: blog
---

TL;DR

I got my first non-trivial [Pull Request](https://github.com/Homebrew/brew/pull/1873) merged in Homebrew, adding a new feature by which Custom Cops can be written for ```brew audit``` command. It was fun!

### The Start

Now that I am in the final semester of my undergraduate studies, I could finally get some time to contribute to open source. I use a MacBookPro 15" , and naturally I have used Homebrew for installing packages. Surely, it saved many hours of pesky dependency management. I looked at Homebrew's repository and was pleasantly surprised. Homebrew has got very encouraging maintainers and its very easy to start contributing to Homebrew. Just run `brew audit <some-formula>` , then fix the errors and submit a patch! The README of Homebrew is very beginner friendly. 

My initial PRs were about adding `plist_options` for formulas which don't have them defined. A `plist` is a configuration file for managing daemons/scripts using `launchd` in MacOS. `launchd` is analogous to `cron` but is much flexible. I also had to write tests for those formula's in which I added the `plist_options` , thus learnt few things along the way. 

In all, I had [8 PRs merged in homebrew-core](https://github.com/Homebrew/homebrew-core/pulls?q=is%3Apr+author%3AGauthamGoli+is%3Aclosed) .These are very simple one's.

### Adding a new feature 

I started looking through the [open issues](https://github.com/Homebrew/brew/issues) in Homebrew labelled as `bug`, `help wanted` and `features`. I picked [Use Rubocop for some `brew audit`'s](https://github.com/Homebrew/brew/issues/569) and tried to understand the objective. The idea is to use [Rubocop](https://github.com/bbatsov/rubocop/) for writing checks to audit formulas when `brew audit` command is run. Currently regular expressions are used to run the checks on the formuals. Rubocop is a Static Code Analyser, clearly using it gives more flexibilty and versatility. I started going through the [documentation](http://rubocop.readthedocs.io/en/latest/) of Rubocop, but the section which explains how to write custom cops was not so complete. I got stumped. So what would one do? Use the source, Luke! In the source code, where the class of Cop is defined, an example was written in [the comments](https://github.com/bbatsov/rubocop/blob/1f59c203564363eef78364652990162605adea94/lib/rubocop/cop/cop.rb) on how to write a custom cop. I also had to read up on Abstract Syntax Trees(AST) and understand how RuboCop parses Ruby Code. (SideNote: Rubocop uses [Parser](https://github.com/whitequark/parser) which in turn uses AST to represent/parse ruby code). This [blog post](http://iempire.ru/2016/12/18/rewrite-code-with-rubocop/) by Kir Shatrov helped too in understanding how custom cops are written.

### Getting the PR merged

Finally, I wrote a [basic cop](https://github.com/GauthamGoli/rubocop-brew) and was able to test it and submitted a [Pull Request](https://github.com/Homebrew/brew/pull/1873) .The maintainers reviewed every single line of code/file change in the PR, which helped in making the code neat and readable. The PR got merged and code is shipped. Now Cop violations can be automatically fixed by adding `--fix` flag to `brew audit`. Not only that, If you have Rubocop editor integration, then cop violations will now get highlighted and reported as you type. I will now look into how audit rules can be converted to Custom Cops. 


Homebrew's codebase is huge and now I will also try to go a bit deeper and gain general understanding of how everything fits together so that I can work on adding new features/fix bugs.