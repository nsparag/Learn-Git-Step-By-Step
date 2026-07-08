# Working with Git Tags

## Learning Objectives

After completing this module, you will be able to:

- Understand what Git tags are
- Create tags
- View tags
- Tag important project versions
- Push tags to GitHub
- Delete tags
- Understand release versioning
- Follow industry best practices for software releases

---

# What is a Tag?

A tag is a permanent label attached to a specific commit.

Tags are commonly used to mark:

- Releases
- Milestones
- Important versions

Examples:

```text
v1.0

v1.1

v2.0

release-2026
```

Unlike branches, tags generally do not change after they are created.

---

# Why Use Tags?

Imagine a project with hundreds of commits.

History:

```text
Commit A

Commit B

Commit C

Commit D

Commit E

Commit F
```

Suppose:

```text
Commit D
```

represents the first stable release.

Without tags:

```text
Need to remember commit hash.
```

With tags:

```text
v1.0
```

You can quickly locate the release.

---

# Real-World Example

Software products often have versions such as:

```text
Version 1.0

Version 1.1

Version 2.0
```

A Git tag can be used to mark these versions.

Example:

```text
v1.0
```

points to the commit used for Version 1.0.

---

# Viewing Existing Tags

List available tags:

```bash
git tag
```

Output:

```text
(no tags)
```

if no tags exist.

---

# Creating a Lightweight Tag

Create a tag:

```bash
git tag v1.0
```

Verify:

```bash
git tag
```

Output:

```text
v1.0
```

---

# Viewing Tag Information

Display tag details:

```bash
git show v1.0
```

Output:

```text
Commit Information

Author

Date

Commit Message
```

Git shows the commit associated with the tag.

---

# Annotated Tags

Industry projects typically use annotated tags.

Create:

```bash
git tag -a v1.0 -m "First stable release"
```

Example:

```bash
git tag -a v1.0 -m "Release version 1.0"
```

Annotated tags store:

- Tag Name
- Tag Message
- Author
- Date

---

# Viewing Annotated Tags

Display information:

```bash
git show v1.0
```

Example:

```text
Tag: v1.0

Message:
First stable release
```

---

# Listing Tags with Details

Display tags:

```bash
git tag
```

Display annotated information:

```bash
git show <tag-name>
```

Example:

```bash
git show v1.0
```

---

# Tagging a Specific Commit

View history:

```bash
git log --oneline
```

Example:

```text
c3d4e5f Add login feature

b2c3d4e Add README

a1b2c3d Initial commit
```

Tag a specific commit:

```bash
git tag v1.0 c3d4e5f
```

Git now associates:

```text
v1.0
```

with that commit.

---

# Understanding Software Versioning

A common version format is:

```text
MAJOR.MINOR.PATCH
```

Example:

```text
1.0.0

1.1.0

1.1.1

2.0.0
```

---

# Meaning of Version Numbers

## MAJOR

Breaking changes.

Example:

```text
1.0.0 → 2.0.0
```

---

## MINOR

New functionality added.

Example:

```text
1.0.0 → 1.1.0
```

---

## PATCH

Bug fixes.

Example:

```text
1.1.0 → 1.1.1
```

---

# Common Tag Naming Conventions

Examples:

```text
v1.0

v1.1

v2.0

v2.1.3
```

These are widely used in open-source and commercial projects.

---

# Push Tags to GitHub

Tags are not automatically pushed.

Push a specific tag:

```bash
git push origin v1.0
```

---

# Push All Tags

Push every tag:

```bash
git push origin --tags
```

GitHub will now display the tags.

---

# Viewing Tags on GitHub

Navigate to:

```text
Repository

→ Releases

or

→ Tags
```

You will see available project versions.

---

# Deleting a Local Tag

Remove a local tag:

```bash
git tag -d v1.0
```

Verify:

```bash
git tag
```

---

# Delete a Remote Tag

Remove a tag from GitHub:

```bash
git push origin --delete v1.0
```

Example output:

```text
Deleted tag 'v1.0'
```

---

# Checking Out a Tag

Suppose you want to inspect an older release.

Execute:

```bash
git checkout v1.0
```

Git moves to the tagged version.

You can now review files exactly as they existed in that release.

---

# Typical Industry Workflow

Develop feature:

```bash
git add .
git commit -m "Complete release features"
```

Create release tag:

```bash
git tag -a v1.0 -m "Release version 1.0"
```

Push code:

```bash
git push
```

Push tag:

```bash
git push origin v1.0
```

Create GitHub Release.

---

# Git Tags vs Branches

## Branch

Used for active development.

Example:

```text
main

feature-login

feature-payment
```

Branches move as development continues.

---

## Tag

Used for marking a specific point in history.

Example:

```text
v1.0

v2.0
```

Tags remain fixed.

---

# Best Practices

## Tag Every Important Release

Examples:

```text
v1.0

v1.1

v2.0
```

---

## Use Meaningful Names

Good:

```text
v1.0

v2.0.1
```

Bad:

```text
test

release

new
```

---

## Prefer Annotated Tags

Use:

```bash
git tag -a
```

for production releases.

---

## Push Tags Immediately

After creating a release:

```bash
git push origin --tags
```

---

# Practice Activity

Perform the following:

1. Create a repository.
2. Create three commits.
3. Tag the latest commit as v1.0.
4. View tag information.
5. Push the tag to GitHub.
6. Create another commit.
7. Tag it as v1.1.
8. Push all tags.

Expected Result:

```text
Repository contains:

v1.0

v1.1
```

representing two releases.

---

# Commands Learned

```bash
git tag

git tag v1.0

git tag -a v1.0 -m "message"

git show v1.0

git push origin v1.0

git push origin --tags

git tag -d v1.0

git push origin --delete v1.0

git checkout v1.0
```

---

# Summary

In this chapter, you learned:

- What Git tags are
- Why tags are important
- How to create tags
- Difference between lightweight and annotated tags
- How to push tags to GitHub
- How to delete tags
- How tags support software releases
- Industry best practices for versioning

Tags play a critical role in professional software development by marking stable releases and important milestones. They allow developers, testers, and users to identify and retrieve specific versions of a project quickly and reliably.