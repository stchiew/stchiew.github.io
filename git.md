---
layout: page
title: PowerApps
permalink: /powerapps/
---

# Git common scenarios

### n commits behind main message

You need to rebase your dev branch with master. You got the above message because after checking out dev branch from master, the master branch got new commit and has moved ahead. You need to get those new commits to your dev branch.

Steps:

```
git checkout master
git pull        #this will update your local main
git checkout yourDevBranch
git rebase main
```

And then push back to remote

```
git push origin yourDevBranch
```
