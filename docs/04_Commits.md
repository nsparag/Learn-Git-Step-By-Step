# Understanding Git Commits

## Learning Objectives

After completing this module, you will be able to:

- Understand what a commit is
- Create meaningful commits
- View commit history
- Understand commit identifiers
- Inspect changes in commits
- Follow commit best practices
- Develop a professional commit workflow

---

# What is a Commit?

A commit is a snapshot of your repository at a specific point in time.

Every commit records:

- The changes made
- The author who made the changes
- The date and time of the changes
- A message describing the changes

Think of a commit as a save point for your project.

---

# Why are Commits Important?

Commits help developers:

- Track project history
- Restore previous versions
- Understand what changed
- Understand why changes were made
- Collaborate efficiently

Without commits, it becomes difficult to manage a growing software project.

---

# Real World Analogy

Imagine writing a report.

You save versions such as:

```text
Report_v1.docx
Report_v2.docx
Report_v3.docx
Report_Final.docx
```

Git commits eliminate the need for multiple file copies.

Instead, Git maintains a complete change history automatically.

---

# Understanding the Git Workflow

A typical workflow looks like:

```text
Create File
      ↓
Modify File
      ↓
git add
      ↓
git commit
      ↓
Repository History
```

Every commit becomes part of the repository history.

---

# Creating a Commit

Suppose a file exists:

```text
README.md
```

Add some content:

```markdown
# My First Repository
```

Check repository status:

```bash
git status
```

Add the file to the staging area:

```bash
git add README.md
```

Create a commit:

```bash
git commit -m "Add project title to README"
```

Example output:

```text
[main a1b2c3d]
Add project title to README
```

---

# Anatomy of a Commit

A commit contains:

```text
Commit Hash
Author
Date
Commit Message
Changes
```

Example:

```text
commit a1b2c3d8f9e

Author: John Smith

Date: Tue Jul 8 10:00:00 2026

Add project title to README
```

---

# What is a Commit Hash?

Every commit receives a unique identifier.

Example:

```text
a1b2c3d8f9e
```

This identifier is called the Commit Hash.

Git uses hashes to:

- Track commits
- Compare commits
- Restore versions
- Merge changes

No two commits have the same hash.

---

# Viewing Commit History

Display complete history:

```bash
git log
```

Example:

```text
commit e5f6g7h

commit d4e5f6g

commit a1b2c3d
```

The newest commit appears first.

---

# Compact History View

For a shorter view:

```bash
git log --oneline
```

Example:

```text
e5f6g7h Fix typo

d4e5f6g Add installation guide

a1b2c3d Initial commit
```

This format is commonly used in day-to-day development.

---

# Viewing Commit Details

Display changes made in the latest commit:

```bash
git show
```

Example:

```bash
git show HEAD
```

You can also view a specific commit:

```bash
git show a1b2c3d
```

---

# Understanding the HEAD Pointer

Git maintains a special reference called:

```text
HEAD
```

HEAD points to the currently checked-out commit.

In most cases:

```text
HEAD → Latest Commit
```

View current commit:

```bash
git show HEAD
```

---

# Making Multiple Commits

A repository may contain many commits.

Example workflow:

Commit 1:

```text
Initial project setup
```

Commit 2:

```text
Add README documentation
```

Commit 3:

```text
Add installation instructions
```

Commit 4:

```text
Fix spelling errors
```

History:

```bash
git log --oneline
```

Output:

```text
4f5g6h7 Fix spelling errors

3e4f5g6 Add installation instructions

2d3e4f5 Add README documentation

1a2b3c4 Initial project setup
```

---

# Good Commit Messages

A commit message should clearly describe the change.

Good examples:

```text
Add installation guide

Create project README

Fix spelling mistakes

Update configuration instructions

Add Git introduction chapter
```

These messages clearly communicate the purpose of the commit.

---

# Poor Commit Messages

Avoid messages such as:

```text
update

changes

test

abc

done

work
```

These messages provide no useful information.

Future developers will struggle to understand the project history.

---

# Commit Message Guidelines

A good commit message should be:

- Short
- Clear
- Specific
- Action oriented

Examples:

```text
Add login functionality

Fix build issue

Update documentation

Create setup script
```

---

# One Commit, One Purpose

A good practice is:

```text
One Logical Change = One Commit
```

Bad example:

```text
Update README
Fix bug
Create feature
Modify configuration

(All in one commit)
```

Good example:

```text
Commit 1: Update README

Commit 2: Fix bug

Commit 3: Create feature

Commit 4: Modify configuration
```

This produces a cleaner project history.

---

# Checking Changes Before Commit

Before creating a commit:

Check status:

```bash
git status
```

Review staged changes:

```bash
git diff --staged
```

Verify that only the intended changes are included.

---

# Typical Daily Workflow

Modify files:

```bash
git status
```

Stage changes:

```bash
git add .
```

Create commit:

```bash
git commit -m "Describe the change"
```

View history:

```bash
git log --oneline
```

This cycle is repeated continuously during development.

---

# Practice Activity

Create a repository and perform the following actions:

1. Create README.md
2. Commit the README file
3. Create notes.txt
4. Commit notes.txt
5. Modify README.md
6. Commit the changes
7. View commit history

Expected result:

```text
At least three commits in the repository.
```

---

# Commands Learned

```bash
git add

git commit

git log

git log --oneline

git show

git diff --staged
```

---

# Summary

In this chapter, you learned:

- What a commit is
- Why commits are important
- How to create commits
- How Git stores project history
- What a commit hash is
- How to view commit history
- How to inspect commit details
- How to write meaningful commit messages
- Commit best practices used in industry

Commits are the foundation of Git. A well-maintained commit history makes a project easier to understand, maintain, debug, and collaborate on.

In the next chapter, you will learn how to use branches to develop features independently without affecting the main codebase.