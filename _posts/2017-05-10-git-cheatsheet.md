---
published: true
category: 'git, cheatsheet'
layout: post
title: Git Cheatsheet
description: >-
  A cheatsheet containing common git commands in use with some additional useful
  commands
---
This cheatsheet contains common git commands in use with some additional useful commands.

> *[] - indicates a parameter which should be replaced at runtime by user*

## Common commands

Init a local repo as a git repo:
```bash
git init
```

Get a repo for the first time:
```bash
git clone [url]
```

Check status of local branch:
```bash
git status
```

Pull content to the local branch from remote branch:
```bash
git pull
```

Stage all changed files:
```bash
git add .
```

Stage a single file:
```bash
git add [path/to/your/file]
```

Commit changes:
```bash
git commit -m "[your commit message]"
```

One line commit history:
```bash
git log --pretty=oneline
```

Push your changes to the remote branch:
```bash
git push
```

Resolve merge conflicts by launching default merge tool:
```bash
git mergetool
```

Resolve merge conflicts by launching preferred tool:
```bash
git mergetool --tool=kdiff3
```

> *One of the best tools I found for merging conflicts is [kdiff3](http://kdiff3.sourceforge.net/).*

## Work with branches

Create a new branch:
```bash
git checkout -b [your_branch_name]
```

Push the new branch to the remote repo:
```bash
git push origin [your_branch_name]
```

Set tracking information for the new branch:
```bash
git branch --set-upstream-to=origin/[your_branch_name] [your_branch_name]
```

Push the new branch to the remote repo with tracking:
```bash
git push -u origin [your_branch_name]
```

Switch to another branch:
```bash
git checkout [your_branch_name]
```

List local branches:
```bash
git branch -l
```

List all branches:
```bash
git branch -a
```

Merge two branches:

> *You must commit everything in your branch and switch to the base branch you want to merge your changes in to, before you perform the merge*

```bash
git merge [your_branch_name]
```

Override a branch with remote content:
```bash
git reset --hard origin/[your_branch_name]
```

Delete a local branch:
```bash
git branch -d [your_branch_name]
```

Diff two branches:
```bash
git diff --name-status [branch_1]..[branch_2]
```

## Work with tags

Create a lightweight(temporary) tag:
```bash
git tag [tag_name]
```

Create an annotated tag:
```bash
git tag -a [tag_name] -m "[your tag annotation]"
```

List all tags:
```bash
git tag -l
```

List filtered tag list:
```bash
git tag -l "v1.0.*"
git tag -l "v1.*"
```

Delete a tag:
```bash
git tag -d [tag_name]
```

Show tag details:
```bash
git show [tag_name]
```

Tag a commit later:
```bash
git tag -a [tag_name] [commit_checksum]
```

Push single tag to the remote:
```bash
git push origin [tag_name]
```

Push multiple tags to the remote:
```bash
git push origin --tags
```

Delete a tag from local repo:
```bash
git tag -d [tag_name]
```

Delete tag from remote:
```bash
git push origin :refs/tags/[tag_name]
```