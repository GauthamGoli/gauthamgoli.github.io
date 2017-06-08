---
layout: post
title:  "Dependant branch PR workflow "
date:   2017-06-08 17:30:00 +0530
author: GauthamGoli
categories: blog
---

As one would start making regular contributions to an opensource project, its possible that you might have come to a
point where your work is at a faster pace compared to the review pace. This might land you in a situation where you work
 on feature A and open a PR, while its still being reviewed, you work on feature B which is dependant on feature A's code
 which is not merged in the upstream yet. While this is plausible, some people might argue that this has an inherant flaw in the way you write your code. ¯\\\_(ツ)_/¯

### Cherry-pick

Cherry-pick is the new found love! With cherry-pick you can apply the change any commit(s) introduces in any other branch.
So, when you are on feature B's branch, just run `git cherry-pick <commit-hash>`  where `<commit-hash>` is the hash of the commit
containing the code that you need from feature A. Now you can continue working on feature B and once feature A gets merged,
run `git rebase master` when on Feature B's branch and you would have a clean history to open a PR for feature B.

![Git rebase]({{ site.url }}/assets/git-rebase.png)

How does this work? Look at the Image on top. `git rebase master` works by applying the changes of feature branch on the master
branch. When the master branch already contains the changes that you are about to apply (Those cherry-picked commmits),
then those commits are not applied as they would be empty commits anyway.


### Credits

Thanks to [alyssais](https://github.com/alyssais) ! 