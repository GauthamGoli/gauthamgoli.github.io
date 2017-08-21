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

All Pull Requests in **[Homebrew/brew](https://github.com/Homebrew/brew)** by me can be accessed here:
 - [https://github.com/Homebrew/brew/pulls?q=is:pr&author:GauthamGoli](https://github.com/Homebrew/brew/pulls?utf8=%E2%9C%93&q=is%3Apr%20author%3AGauthamGoli)

<details>
  <summary>&nbsp;&nbsp;&nbsp;List of all the above PRs (both merged/open) <strong>(Click to expand)</strong></summary>
  <p>
<!-- the above p cannot start right at the beginning of the line and is mandatory for everything else to work -->
<h4>Pull requests that got merged during GSoC work period:</h4>
<ul>
<li> <a href="https://github.com/Homebrew/brew/pull/2610">#2610: Add autocorrect method for ComponentsOrder rubocop and tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2628">#2628: audit: Detect multiline and interpolated strings in formula desc cop</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2631">#2631: audit: Port audit_homepage method to rubocop and add tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2662">#2662: audit: Port audit_text method to rubocop and add tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2664">#2664: audit: Port audit_caveats method to rubocop and add tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2755">#2755: audit: Port audit_checksum method to rubocop and add tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2776">#2776: audit: Fix audit_checksum method's rubocop and add more tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2790">#2790: audit: Port audit_legacy_patches method to rubocop and add tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2842">#2842: audit: Don't run audit methods when `--only-cops` option is passed</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2843">#2843: audit: Port audit_conflicts method to rubocop and add tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2853">#2853: style: Don't run FormulaAuditStrict cops when `brew style foo` cmd is executed </a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2879">#2879: audit: Port audit_options non-strict rules to rubocop and add tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2901">#2901: audit: Port audit_options strict rules to rubocop and add tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2905">#2905: audit: Port audit_options rules for new formulae to rubocop and add test</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2906">#2906: style: disable NewFormulaAudit cops' execution by default unless specified</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2911">#2911: audit: Port audit_urls partially to rubocop and add corresponding tests </a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2932">#2932: audit: Port audit_urls to rubocop and add corresponding tests Part 2</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2957">#2957: audit: Run style violations check when `--new-formula` is passed</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2964">#2964: audit: Port dependency rules from line_problems to rubocop and add tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2975">#2975: audit: Port audit_urls strict rules to rubocop, add tests, autocorrect</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2976">#2976: audit: Port patches audit code to a rubocop and add tests</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/2980">#2980: audit: fix bug where `brew audit foo` runs every style check.</a> </li>
     <li> <a href="https://github.com/Homebrew/brew/pull/3012">#3012: Add node pattern methods to handle dependency audits in a better way</a> </li>
</ul>
<h4> Pull requests still under review:</h4>
<ul>
    <li> <a href="https://github.com/Homebrew/brew/pull/2982">#2982: audit: Port audit_class to rubocop, add tests and autocorrect</a> </li>
    <li> <a href="https://github.com/Homebrew/brew/pull/2995">#2995: audit: Port line_problems to rubocop and add tests part 2</a> </li>
    <li> <a href="https://github.com/Homebrew/brew/pull/3063">#3063: audit: In Cops and their tests convert all multiline strings to heredocs</a> </li>
</ul>
</p></details>
<br/>

### Stats

<div class="infogram-embed" data-id="9ba7f11c-5ddb-40ce-aed9-8a5e9ca3fa82" data-type="interactive" data-title="Welcome: Your first project"></div><script>!function(e,t,s,i){var n="InfogramEmbeds",o=e.getElementsByTagName("script"),d=o[0],r=/^http:/.test(e.location)?"http:":"https:";if(/^\/{2}/.test(i)&&(i=r+i),window[n]&&window[n].initialized)window[n].process&&window[n].process();else if(!e.getElementById(s)){var a=e.createElement("script");a.async=1,a.id=s,a.src=i,d.parentNode.insertBefore(a,d)}}(document,0,"infogram-async","//e.infogram.com/js/dist/embed-loader-min.js");</script><div style="padding:8px 0;font-family:Arial!important;font-size:13px!important;line-height:15px!important;text-align:center;border-top:1px solid #dadada;margin:0 30px"><a href="https://infogram.com/9ba7f11c-5ddb-40ce-aed9-8a5e9ca3fa82" style="color:#989898!important;text-decoration:none!important;" target="_blank">Welcome: Your first project</a><br><a href="https://infogram.com" style="color:#989898!important;text-decoration:none!important;" target="_blank" rel="nofollow">Infogram</a></div>

### Project Description

This project implements [RuboCop](https://github.com/bbatsov/rubocop/) custom cops to check Homebrew's coding style violations programmatically. More details can be
found [here](https://gauthamgoli.github.io/blog/2017/05/04/Google-Summer-of-Code-starts.html) and [here](https://summerofcode.withgoogle.com/projects/#5375471609970688).

### Project Learnings

[Searching through the whole git history](http://travisjeffery.com/b/2012/02/search-a-git-repo-like-a-ninja/) has been very helpful, as it would mostly lead me to the first PR where the concerned contributor
or maintainer would have written about the code. PR checklist template FTW!

I learnt to test my code extensively before opening a PR. The importance of this cannot be stressed enough. Do not ever be negligent and assume that
your code will always work. Then things **will** break when that nasty edge case is encountered.

I also learnt to not be afraid and jump into source code instead of reading the docs. RuboCop has a more user driven documentation, while
documentation of its internals is rather scarce. By going through the source of RuboCop, I came across an undocumented
and a powerful [feature](https://github.com/bbatsov/rubocop/blob/master/lib/rubocop/node_pattern.rb) of RuboCop. It greatly simplified some parts of my GSoC Project. Also, I reported a [bug](https://github.com/bbatsov/rubocop/issues/4437),
and contributed in writing a new cop in RuboCop project.
I also got to understand how certain aspects of RuboCop offense checks work, thus preventing unexpected bugs in Homebrew.

The reason why 3 out of the 15 methods could not be ported is because RuboCop
 runs in a separate process and these methods use Homebrew's internals, hence are not available in that process. Unix sockets for interprocess communication(IPC) could be used
 but making it complicated is just not worth it.

### Road ahead

Whilst the `audit` rules have been ported to RuboCop cops, few of them have `autocorrect`. Now I would be looking at adding `autocorrect` methods, so correcting the style offenses across
huge number of `Formulae` can be automated. I also look forward to continue contributing to Homebrew. Its the project which makes macOS usable to developers and I myself
use `brew` heavily on a day to day basis.

Over all, it has been an amazing experience for me, working on a popular project, with awesome supportive friendly [talented](https://soundcloud.com/mikemcquaid/sets/anticipated-hindsight) mentors ([MikeMcQuaid](https://github.com/MikeMcQuaid) & [Jcount](https://github.com/JCount)) and [co](https://github.com/raza15) [interns](https://github.com/mansimarkaur).


### Credits

This project would never have gotten to this stage without the code reviews and discussions with my mentors.
A huge shout out & sincere Thanks to all the mentors at Homebrew ([MikeMcQuaid](https://github.com/MikeMcQuaid), [Jcount](https://github.com/JCount),
 [ilovezfs](https://github.com/ilovezfs), [alyssais](https://github.com/alyssais), [apjanke](https://github.com/apjanke) , [woodruffw](https://github.com/woodruffw),
 [bfontaine](https://github.com/bfontaine) & others) and amazing people at Google for this opportunity and giving a headstart in OSS. You simply rock!


Until next time and May the source be with you!
