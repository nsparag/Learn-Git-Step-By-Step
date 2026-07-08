# Working with Git Branches

## Learning Objectives

After completing this module, you will be able to:

- Understand what a branch is
- Understand why branches are used
- Create branches
- Switch between branches
- View available branches
- Make changes in a branch
- Understand branch isolation
- Follow basic branching workflows

---

# What is a Branch?

A branch is an independent line of development within a repository.

Branches allow developers to work on new features, bug fixes, or experiments without affecting the main project.

Think of a branch as a parallel version of your project.

---

# Why Do We Need Branches?

Imagine you are developing a software project.

The current version is working correctly.

You now want to:

- Add a new feature
- Fix a bug
- Experiment with a different approach

Making changes directly in the main branch is risky because unfinished work may break the project.

Branches provide a safe environment for development.

---

# Real-World Example

Suppose a team is developing an e-commerce website.

Developer A:

```text
Working on Login Feature
```

Developer B:

```text
Working on Payment Module
```

Developer C:

```text
Fixing a Bug
```

Each developer can create a separate branch and work independently.

Later, their changes can be merged into the main branch.

---

# Understanding the Main Branch

When a repository is created, Git usually creates a default branch called:

```text
main
```

Example:

```bash
git branch
```

Output:

```text
* main
```

The asterisk (*) indicates the currently active branch.

---

# Viewing Existing Branches

Display available branches:

```bash
git branch
```

Example:

```text
* main
```

Currently, only one branch exists.

---

# Creating a New Branch

Create a branch named:

```text
feature-login
```

Command:

```bash
git branch feature-login
```

Check branches:

```bash
git branch
```

Output:

```text
feature-login
* main
```

The branch has been created, but you are still working on the main branch.

---

# Switching to a Branch

Move to the new branch:

```bash
git checkout feature-login
```

Output:

```text
Switched to branch 'feature-login'
```

Verify:

```bash
git branch
```

Output:

```text
* feature-login
main
```

The asterisk now shows the active branch.

---

# Modern Way to Switch Branches

Git also provides:

```bash
git switch feature-login
```

This command performs the same operation.

Many developers prefer git switch because it is easier to understand.

---

# Create and Switch in One Command

Instead of performing two commands:

```bash
git branch feature-login

git switch feature-login
```

You can use:

```bash
git switch -c feature-login
```

or

```bash
git checkout -b feature-login
```

Both commands:

1. Create the branch
2. Switch to the branch

---

# Working Inside a Branch

Suppose you are on:

```text
feature-login
```

Create a file:

```bash
touch login.txt
```

Add content:

```text
Login feature under development
```

Stage and commit:

```bash
git add login.txt

git commit -m "Add login feature draft"
```

This commit exists only in the feature branch.

---

# Understanding Branch Isolation

Changes in one branch do not automatically appear in another branch.

Example:

Branch:

```text
main
```

Contains:

```text
README.md
```

Branch:

```text
feature-login
```

Contains:

```text
README.md
login.txt
```

The new file remains isolated until the branches are merged.

---

# Switching Back to Main

Move back to the main branch:

```bash
git switch main
```

or

```bash
git checkout main
```

Verify:

```bash
git branch
```

Output:

```text
feature-login
* main
```

You are now working on the main branch again.

---

# Checking Branch-Specific Files

List files:

```bash
ls
```

You may notice that:

```text
login.txt
```

is no longer visible.

Why?

Because the file was committed in:

```text
feature-login
```

and not in:

```text
main
```

This demonstrates branch isolation.

---

# Viewing All Branches

To see all local branches:

```bash
git branch
```

Example:

```text
feature-login
feature-payment
feature-search
* main
```

---

# Renaming a Branch

Suppose you created:

```text
testbranch
```

Rename it:

```bash
git branch -m testbranch feature-test
```

Verify:

```bash
git branch
```

---

# Deleting a Branch

Delete a branch:

```bash
git branch -d feature-test
```

Example:

```bash
git branch -d feature-login
```

Git will prevent deletion if the branch contains unmerged work.

---

# Force Delete a Branch

Use carefully:

```bash
git branch -D feature-login
```

This permanently removes the branch even if changes are not merged.

---

# Typical Industry Workflow

Main branch:

```text
main
```

Create feature branch:

```bash
git switch -c feature-login
```

Develop feature:

```bash
git add .
git commit -m "Implement login functionality"
```

Return to main:

```bash
git switch main
```

Merge feature branch:

```bash
git merge feature-login
```

Delete feature branch:

```bash
git branch -d feature-login
```

This workflow is commonly used in professional software teams.

---

# Best Practices

## Keep Main Stable

Avoid experimental changes directly on:

```text
main
```

---

## Create a Branch for Every Feature

Examples:

```text
feature-login

feature-payment

feature-search

feature-reports
```

---

## Use Meaningful Names

Good names:

```text
feature-login

bugfix-payment-error

feature-user-profile
```

Poor names:

```text
test

abc

newbranch

temp
```

---

## Commit Frequently

Small commits make development easier to track and review.

---

# Practice Activity

Perform the following:

1. Create a repository.
2. Create a branch named feature-profile.
3. Switch to the new branch.
4. Create a file profile.txt.
5. Commit the file.
6. Switch back to main.
7. Verify the file is not visible.
8. List all branches.

Expected Result:

```text
Two branches:

main

feature-profile
```

with independent histories.

---

# Commands Learned

```bash
git branch

git branch <branch-name>

git switch <branch-name>

git switch -c <branch-name>

git checkout <branch-name>

git checkout -b <branch-name>

git branch -m

git branch -d

git branch -D
```

---

# Summary

In this chapter, you learned:

- What a branch is
- Why branches are important
- How to create branches
- How to switch between branches
- How branch isolation works
- How to rename branches
- How to delete branches
- Common industry branching practices

Branches are one of Git's most powerful features. They allow developers to work safely, independently, and collaboratively without affecting the stability of the main project.

In the next chapter, you will learn how changes from different branches can be combined using Git Merge.