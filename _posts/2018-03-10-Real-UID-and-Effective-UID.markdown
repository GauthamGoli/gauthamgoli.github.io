---
layout: post
title:  "Real UID and Effective UID"
date:   2018-03-10 21:40:00 +0530
author: GauthamGoli
categories: blog
---

Recently I was speedrunning [Narnia](http://overthewire.org/wargames/narnia/) as a practice. In Level 1, I was using a shell code
to spawn a shell (/bin/sh) , but upon obtaining the shell `id` wasn't returning `uid` of next level's user which was weird, as
I was expecting to see `uid` of `narnia2` instead of `narnia1`.
<br/>
<br/>
![Weird ]({{ site.url }}/assets/wrong-uid.png)
<br/>
<br/>
The clue was hidden in the source code of previous level's challenge.
<br/>
<br/>
![Clue ]({{ site.url }}/assets/clue-uid.png)
<br/>
<br/>
`setreuid` is used to set `real uid` (first argument) and `effective uid` (second argument) and in the above code, its
setting them both as `effective uid` hence, I was able to get a shell as shell checks if Real UID is same as Effective UID
and only then executes with privileges of Effective UID, else drops `euid` privileges. This is a new security measure by the shell itself.

Easy enough now I'd just have to update shell code to call `setreuid(geteuid(), geteuid())` first and then obtain shell.