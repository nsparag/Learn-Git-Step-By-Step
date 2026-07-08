# Common Git Commands Reference

## Purpose

This document serves as a quick reference guide for the most frequently used Git commands.

Students can use this file as a cheat sheet while performing practical exercises and projects.

---

# Repository Initialization

Initialize a new Git repository:

```bash
git init
```

Check repository status:

```bash
git status
```

Display Git version:

```bash
git --version
```

---

# Configuration Commands

Configure username:

```bash
git config --global user.name "Your Name"
```

Configure email:

```bash
git config --global user.email "you@example.com"
```

Display configuration:

```bash
git config --list
```

Display username:

```bash
git config user.name
```

Display email:

```bash
git config user.email
```

---

# File Tracking Commands

Add a specific file:

```bash
git add README.md
```

Add all modified files:

```bash
git add .
```

Check current status:

```bash
git status
```

---

# Commit Commands

Create commit:

```bash
git commit -m "Commit message"
```

View history:

```bash
git log
```

Compact history:

```bash
git log --oneline
```

View graphical history:

```bash
git log --graph --oneline --all
```

Show latest commit:

```bash
git show
```

---

# Branch Commands

View branches:

```bash
git branch
```

Create branch:

```bash
git branch feature-login
```

Create and switch:

```bash
git switch -c feature-login
```

Switch branch:

```bash
git switch main
```

Rename branch:

```bash
git branch -m old-name new-name
```

Delete merged branch:

```bash
git branch -d feature-login
```

Force delete branch:

```bash
git branch -D feature-login
```

---

# Merge Commands

Merge branch:

```bash
git merge feature-login
```

Abort merge:

```bash
git merge --abort
```

---

# Difference Commands

Show unstaged changes:

```bash
git diff
```

Show staged changes:

```bash
git diff --staged
```

Compare two commits:

```bash
git diff commit1 commit2
```

---

# Remote Repository Commands

View remotes:

```bash
git remote
```

View remote URLs:

```bash
git remote -v
```

Add remote:

```bash
git remote add origin URL
```

Remove remote:

```bash
git remote remove origin
```

Display remote information:

```bash
git remote show origin
```

---

# Push Commands

Push current branch:

```bash
git push
```

First push:

```bash
git push -u origin main
```

Push specific branch:

```bash
git push origin feature-login
```

---

# Pull Commands

Pull latest changes:

```bash
git pull
```

Pull specific branch:

```bash
git pull origin main
```

Fetch updates:

```bash
git fetch
```

---

# Clone Commands

Clone repository:

```bash
git clone REPOSITORY_URL
```

Example:

```bash
git clone https://github.com/user/project.git
```

---

# Tag Commands

List tags:

```bash
git tag
```

Create tag:

```bash
git tag v1.0
```

Create annotated tag:

```bash
git tag -a v1.0 -m "First release"
```

View tag:

```bash
git show v1.0
```

Push tag:

```bash
git push origin v1.0
```

Push all tags:

```bash
git push origin --tags
```

Delete local tag:

```bash
git tag -d v1.0
```

Delete remote tag:

```bash
git push origin --delete v1.0
```

---

# Stash Commands

Temporarily save changes:

```bash
git stash
```

View stashes:

```bash
git stash list
```

Restore stash:

```bash
git stash pop
```

Delete stash:

```bash
git stash drop
```

---

# Undo Commands

Discard unstaged changes:

```bash
git restore filename
```

Unstage file:

```bash
git restore --staged filename
```

Undo latest commit (keep changes):

```bash
git reset --soft HEAD~1
```

Undo latest commit:

```bash
git reset HEAD~1
```

---

# Helpful Daily Commands

Check status:

```bash
git status
```

View branch:

```bash
git branch
```

View recent commits:

```bash
git log --oneline -5
```

Pull latest updates:

```bash
git pull
```

Push changes:

```bash
git push
```

---

# Daily Developer Workflow

```bash
git pull

git switch -c feature-new-task

git add .

git commit -m "Implement new task"

git push -u origin feature-new-task
```

Create Pull Request on GitHub.

Review.

Merge.

Delete branch.

---

# Command Categories Summary

## Repository

```bash
git init
git status
```

## Commits

```bash
git add
git commit
git log
```

## Branches

```bash
git branch
git switch
git merge
```

## Remotes

```bash
git remote
git push
git pull
git clone
```

## Releases

```bash
git tag
```

## Recovery

```bash
git stash
git restore
git reset
```

---

# Summary

This document provides a quick reference for the most commonly used Git commands.

Students should use this guide during practical sessions until the commands become familiar through repeated usage.

Remember:

```text
Learn Git by using Git.
```

Regular practice is the fastest way to become comfortable with Git and GitHub.