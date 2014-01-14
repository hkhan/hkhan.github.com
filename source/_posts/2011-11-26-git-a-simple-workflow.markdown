---
layout: post
title: "Git: A simple workflow"
date: 2011-11-26 23:41
comments: true
categories: git
keywords: git, workflow, code quality
description: A simple git workflow for peer reviews and knowledge sharing
---

This is a very simple yet effective workflow in small teams to encourage knowledge sharing and improve code quality. I have been using this lately and seems to be working very well. The following illustrates the workflow assuming the upstream remote named 'origin' on github.

``` bash
# create and switch to a new feature branch
git checkout -b new-feature
```
``` bash
# do some work on the feature branch and commit locally
git commit -m 'Initial commit'

# push the 'feature' branch to remote 'origin'
git push -u origin new-feature and set up tracking
```
``` bash
git commit -m 'Some more feature work'

# push some more commited work to remote
git push new-feature
```

Once the feature has been completed, raise a **pull request** which will result in a notification to the team members to review and merge the feature code into the master branch.

After successful code review and merging, get **Hubot** to deploy the master branch, test the feature and have a cup of tea!
