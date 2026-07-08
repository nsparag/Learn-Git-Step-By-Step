# GitHub Flow - Industry Development Workflow

## Learning Objectives

After completing this module, you will be able to:

- Understand how software teams use Git and GitHub
- Follow a professional development workflow
- Create feature branches
- Work with Pull Requests
- Participate in code reviews
- Merge approved changes
- Maintain a clean project history

---

# What is GitHub Flow?

GitHub Flow is a lightweight development workflow used by many software teams.

It provides a structured process for developing, reviewing, and deploying software.

The workflow is simple and suitable for:

- Individual projects
- Student projects
- Open-source projects
- Professional software development

---

# GitHub Flow Overview

```text
Main Branch
      |
      |
Create Branch
      |
Develop Feature
      |
Create Commit(s)
      |
Push Branch
      |
Create Pull Request
      |
Code Review
      |
Merge
      |
Delete Branch
```

---

# Why Use GitHub Flow?

Benefits:

- Keeps main stable
- Encourages code reviews
- Supports collaboration
- Simplifies feature development
- Makes project history easier to understand

---

# Step 1: Start from Main

Before creating a branch:

```bash
git switch main
```

Update local repository:

```bash
git pull
```

Always start from the latest version of the project.

---

# Step 2: Create a Feature Branch

Create a branch for a specific task.

Example:

```bash
git switch -c feature-login
```

Other examples:

```text
feature-payment

feature-report

feature-dashboard

bugfix-login-error
```

---

# Branch Naming Convention

Use descriptive names.

Good:

```text
feature-user-profile

feature-search

bugfix-memory-leak

bugfix-build-error
```

Avoid:

```text
test

temp

new

work
```

---

# Step 3: Develop the Feature

Create or modify files.

Example:

```text
login.cpp

login.h
```

Check status:

```bash
git status
```

---

# Step 4: Commit Changes

Stage files:

```bash
git add .
```

Create commit:

```bash
git commit -m "Add user login functionality"
```

Make commits whenever a logical unit of work is completed.

---

# Step 5: Push Branch to GitHub

Push branch:

```bash
git push -u origin feature-login
```

The branch is now available on GitHub.

---

# Step 6: Create Pull Request

Open GitHub.

You will see:

```text
Compare & Pull Request
```

Click the button.

Create a Pull Request.

---

# Good Pull Request Title

Example:

```text
Add user login functionality
```

Bad examples:

```text
Update

Changes

Work Done
```

The title should clearly describe the work.

---

# Good Pull Request Description

Example:

```text
Summary

Implemented user login feature.

Changes

- Added login form
- Added validation
- Added authentication logic

Testing

- Tested valid users
- Tested invalid users
```

---

# Step 7: Code Review

Team members review:

- Logic
- Readability
- Coding Standards
- Performance
- Documentation

Reviewers may request modifications before approval.

---

# Step 8: Update Pull Request

If review comments are received:

Modify code.

Commit changes:

```bash
git add .
git commit -m "Address review comments"
```

Push updates:

```bash
git push
```

The Pull Request updates automatically.

---

# Step 9: Merge Pull Request

After approval:

```text
Merge Pull Request
```

Select:

```text
Confirm Merge
```

Changes become part of:

```text
main
```

---

# Step 10: Delete Branch

After successful merge:

```bash
git branch -d feature-login
```

Delete remote branch:

```bash
git push origin --delete feature-login
```

This keeps the repository clean.

---

# Complete Example

Create branch:

```bash
git switch -c feature-profile
```

Develop feature.

Commit:

```bash
git add .
git commit -m "Add profile page"
```

Push:

```bash
git push -u origin feature-profile
```

Create Pull Request.

Review.

Merge.

Delete branch.

---

# GitHub Flow in Industry

Most professional development teams follow a process similar to:

```text
Task Assignment
        ↓
Feature Branch
        ↓
Development
        ↓
Commit History
        ↓
Pull Request
        ↓
Code Review
        ↓
Approval
        ↓
Merge
        ↓
Release
```

This workflow improves quality, collaboration, and traceability.

---

# Best Practices

## One Feature Per Branch

Good:

```text
feature-login
```

Bad:

```text
feature-login-payment-report
```

---

## Commit Frequently

Small commits are easier to review.

---

## Use Meaningful Commit Messages

Good:

```text
Add login validation

Fix password bug
```

---

## Keep Pull Requests Small

Reviewing 100 lines is easier than reviewing 5000 lines.

---

## Delete Completed Branches

Avoid accumulating unused branches.

---

# Practice Activity

Create a repository and perform:

1. Create branch feature-profile.
2. Add profile.txt.
3. Commit changes.
4. Push branch.
5. Create Pull Request.
6. Merge Pull Request.
7. Delete branch.

Expected Result:

```text
Successful completion of GitHub Flow.
```

---

# Summary

In this chapter, you learned:

- What GitHub Flow is
- Why teams use it
- How to create feature branches
- How Pull Requests fit into development
- How code reviews improve quality
- How to merge changes professionally
- Industry best practices for Git and GitHub usage

GitHub Flow is one of the most widely adopted workflows in modern software development and is an essential skill for every software engineer.