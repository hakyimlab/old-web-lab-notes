---
title: Github Cheatsheet
author: Haky Im
date: '2021-06-16'
slug: github-cheatsheet
categories: []
tags: []
---


## clean github repository history

```
-- Remove the history from
rm -rf .git

-- recreate the repos from the current content only
git init
git add .
git commit -m "Initial commit"

-- push to the github remote repos ensuring you overwrite history
git remote add origin git@github.com:<YOUR ACCOUNT>/<YOUR REPOS>.git
git push -u --force origin master
```

## get rid of DS_Store files
```
find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch
echo .DS_Store >> .gitignore
git add .gitignore
git commit -m '.DS_Store banished!'
```