---
published: true
category: git
layout: post
title: Git Cheatsheet
---
This cheat sheet contains common git commands in use with some additional useful commands.

> *[] - indicates a parameter which should be replaced at runtime by user*

### Common commands
Getting a repo for the first time:
```bash
git clone [url]
```

Check status of local branch:
```bash
git status
```

Pulling content to the local branch from remote branch:
```bash
git pull
```

Stage files
```bash
git add . //Stage all changed files
git add [path/to/your/file] //Stage a single file
```

Committing changes
```bash
git commit -m "[your commit message]"
```

Pushing your changes to the remote branch:
```bash
git push
```

Resolving merge conflicts: [kdiff3](http://kdiff3.sourceforge.net/)
```bash
git mergetool //Launch the default
git mergetool --tool=kdiff3 //Launch preferred tool
```

### Working with branches

Create a new branch:
```bash
git checkout -b [your_branch_name]
```

Listing branches:
```bash
git branch -l //List local branches
git branch -a //List all branches
```

Delete a local branch:
```bash
git branch -d [your_branch_name]
```
```bash
git push --set-upstream origin [your_branch_name]
```
