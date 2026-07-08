# Resolving Merge Conflicts in Git

## Learning Objectives

After completing this module, you will be able to:

- Understand what a merge conflict is
- Identify situations that create conflicts
- Read conflict markers
- Resolve merge conflicts manually
- Complete a merge after conflict resolution
- Follow industry best practices for conflict management

---

# What is a Merge Conflict?

A Merge Conflict occurs when Git cannot automatically determine how changes from two branches should be combined.

Git can merge changes automatically when modifications occur in different files or different parts of a file.

However, if two branches modify the same lines of a file, Git requires human intervention.

---

# Why Do Merge Conflicts Occur?

Consider the following situation.

Branch:

```text
main
```

File:

```text
Application Version 1.0
```

Another branch:

```text
feature-update
```

Both branches modify the same line.

Git now sees:

```text
main:
Application Version 2.0
```

and

```text
feature-update:
Application Version 1.1
```

Git cannot determine which change is correct.

A merge conflict occurs.

---

# Common Causes of Merge Conflicts

## Same Line Modified

Two developers edit the same line.

---

## File Deleted in One Branch

A file is deleted in one branch and modified in another.

---

## Simultaneous Refactoring

Large code restructuring performed in multiple branches.

---

## Long-Lived Branches

Branches that remain active for long periods often accumulate conflicting changes.

---

# Creating a Merge Conflict

## Step 1: Create Repository

```bash
mkdir conflict_demo
cd conflict_demo

git init
```

Create a file:

```bash
echo "Version 1.0" > version.txt
```

Commit:

```bash
git add version.txt

git commit -m "Initial version"
```

---

## Step 2: Create Branch

```bash
git switch -c feature-update
```

Modify file:

```text
Version 1.1
```

Commit:

```bash
git add version.txt

git commit -m "Update version to 1.1"
```

---

## Step 3: Return to Main

```bash
git switch main
```

Modify the same file:

```text
Version 2.0
```

Commit:

```bash
git add version.txt

git commit -m "Update version to 2.0"
```

---

## Step 4: Attempt Merge

Execute:

```bash
git merge feature-update
```

Git responds:

```text
Auto-merging version.txt

CONFLICT (content):
Merge conflict in version.txt

Automatic merge failed.
```

A merge conflict now exists.

---

# Checking Repository Status

View status:

```bash
git status
```

Example:

```text
Unmerged paths:

both modified:
version.txt
```

This indicates manual action is required.

---

# Understanding Conflict Markers

Open the conflicted file:

```text
<<<<<<< HEAD
Version 2.0
=======
Version 1.1
>>>>>>> feature-update
```

Git inserts markers showing conflicting content.

---

# Meaning of Conflict Markers

Current branch:

```text
<<<<<<< HEAD
Version 2.0
```

Incoming branch:

```text
=======
Version 1.1
>>>>>>> feature-update
```

Git is asking:

```text
Which content should be kept?
```

---

# Resolving the Conflict

Suppose the correct version is:

```text
Version 2.0
```

Edit the file:

```text
Version 2.0
```

Remove all conflict markers.

Save the file.

---

# Mark Conflict as Resolved

Stage the file:

```bash
git add version.txt
```

Verify status:

```bash
git status
```

---

# Complete the Merge

Create merge commit:

```bash
git commit
```

Git creates a merge commit.

Example:

```text
Merge branch 'feature-update'
```

---

# Verify the Merge

View history:

```bash
git log --oneline --graph --all
```

Example:

```text
*   e5f6g7h Merge branch 'feature-update'
|\
| * d4e5f6g Update version to 1.1
* | c3d4e5f Update version to 2.0
|/
* a1b2c3d Initial version
```

The merge is complete.

---

# Abort a Merge

Suppose you accidentally start a merge.

Cancel it:

```bash
git merge --abort
```

Repository returns to the state before the merge started.

---

# Best Practices to Avoid Conflicts

## Pull Frequently

Before starting work:

```bash
git pull
```

Stay updated with the latest changes.

---

## Use Small Feature Branches

Smaller branches create fewer conflicts.

Good:

```text
feature-login

feature-report
```

Bad:

```text
feature-big-project
```

---

## Merge Regularly

Do not allow feature branches to remain isolated for weeks.

---

## Communicate with Team Members

If multiple developers modify the same files, coordination helps prevent conflicts.

---

## Commit Frequently

Smaller, focused commits are easier to merge.

---

# Real Industry Example

Developer A:

```text
Updating Login Module
```

Developer B:

```text
Updating Login Module
```

Both modify:

```text
login.cpp
```

Conflict occurs during merge.

Developers review the changes, select the correct implementation, and complete the merge.

Merge conflicts are normal and occur regularly in software development.

---

# Common Mistakes

## Panic When Seeing Conflict Markers

Conflict markers are informational.

Read them carefully and decide the correct content.

---

## Deleting Entire File

Only remove conflict markers and invalid content.

Do not accidentally delete useful changes.

---

## Forgetting to Commit After Resolution

After resolving:

```bash
git add
git commit
```

must be executed.

---

## Ignoring git status

Always check:

```bash
git status
```

during conflict resolution.

---

# Practice Activity

Perform the following:

1. Create a repository.
2. Create a file named notes.txt.
3. Commit the file.
4. Create a feature branch.
5. Modify the file and commit.
6. Return to main.
7. Modify the same line and commit.
8. Merge the feature branch.
9. Observe the conflict.
10. Resolve it manually.
11. Complete the merge.

Expected Result:

```text
Successful merge after manual conflict resolution.
```

---

# Commands Learned

```bash
git merge

git status

git add

git commit

git merge --abort

git log --graph --all
```

---

# Summary

In this chapter, you learned:

- What merge conflicts are
- Why conflicts occur
- How to identify conflict markers
- How to resolve conflicts manually
- How to complete a merge after resolution
- How to abort a merge
- Best practices for minimizing conflicts

Merge conflicts are a normal part of collaborative software development. The ability to understand and resolve them confidently is an essential skill for every software engineer.