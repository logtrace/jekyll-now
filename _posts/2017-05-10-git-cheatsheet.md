---
published: true
category: 'git, cheatsheet'
layout: post
title: Git Cheatsheet
description: >-
  This cheatsheet contains common git commands in use with some additional
  useful commands
---
This cheatsheet contains common git commands in use with some additional useful commands.

> *[] - indicates a parameter which should be replaced at runtime by user*

### Common commands
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

Stage files:
```bash
git add . //Stage all changed files
git add [path/to/your/file] //Stage a single file
```

Commit changes:
```bash
git commit -m "[your commit message]"
```

Push your changes to the remote branch:
```bash
git push
```

Resolve merge conflicts: [kdiff3](http://kdiff3.sourceforge.net/)
```bash
git mergetool //Launch the default
git mergetool --tool=kdiff3 //Launch preferred tool
```

### Work with branches

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

List branches:
```bash
git branch -l //List local branches
git branch -a //List all branches
```

Delete a local branch:
```bash
git branch -d [your_branch_name]
```

Diff two branches:
```bash
git diff --name-status [branch_1]..[branch_2]
```
