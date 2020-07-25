---
title: "Git Steps"
---

# GIT STEPS

Get latest from remote branch and replace everything  
  
    git fetch origin some-branch
    git reset --hard FETCH_HEAD
    
To wipeout untracked files  
`git clean -fd`

To clone a specific branch  
`git clone -b branchname --single-branch https://github.com/stchiew/repo.git`


