# Exercise 03 - Merging Branches

## Objective

In this exercise, you will learn how to:

- Merge a feature branch into the main branch
- Understand why merging is required
- Verify merge results
- View repository history after a merge
- Remove a completed feature branch

---

## Background

Branches allow developers to work independently.

Once a feature is completed and tested, it must be merged back into the main branch so that it becomes part of the project.

Merging combines changes from one branch into another.

---

## Prerequisites

Before starting:

- Exercise 01 must be completed
- Exercise 02 must be completed
- A branch named feature-profile should exist

---

## Current Situation

You should have:

```text
main
```

and

```text
feature-profile
```

The file:

```text
profile.txt
```

should exist only in:

```text
feature-profile
```

---

## Tasks

### Step 1: View Existing Branches

```bash
git branch
```

Expected:

```text
* feature-profile
  main
```

or

```text
  feature-profile
* main
```

---

### Step 2: Verify File Exists in Feature Branch

Switch to feature branch:

```bash
git switch feature-profile
```

Display files:

```bash
ls
```

Expected:

```text
README.md
profile.txt
```

---

### Step 3: Switch to Main Branch

```bash
git switch main
```

Verify:

```bash
git branch
```

Expected:

```text
  feature-profile
* main
```

---

### Step 4: Verify File Is Absent

```bash
ls
```

Expected:

```text
README.md
```

Question:

Why is profile.txt missing?

---

### Step 5: Merge Feature Branch

Execute:

```bash
git merge feature-profile
```

Observe the output carefully.

Example:

```text
Updating a1b2c3d..d4e5f6g

Fast-forward
```

or

```text
Merge made by the 'ort' strategy.
```

---

### Step 6: Verify the Merge

Display files:

```bash
ls
```

Expected:

```text
README.md

profile.txt
```

The file from the feature branch is now available in main.

---

### Step 7: View Commit History

Display history:

```bash
git log --oneline
```

Observe:

```text
Add profile feature
Initial commit
```

Both commits should now be visible from main.

---

### Step 8: View Graphical History

```bash
git log --graph --oneline --all
```

Observe how Git represents branch history.

---

### Step 9: Delete Completed Branch

Since the feature is now merged:

```bash
git branch -d feature-profile
```

Verify:

```bash
git branch
```

Expected:

```text
* main
```

---

## Questions

### Q1

Why are branches merged?

### Q2

Which command merges branches?

### Q3

What happened to profile.txt after merging?

### Q4

Why is it safe to delete a branch after it has been merged?

### Q5

What is the difference between creating a branch and merging a branch?

---

## Deliverables

Submit:

- Screenshot before merge
- Screenshot after merge
- Screenshot of git log --oneline
- Screenshot of git log --graph --oneline --all
- Screenshot after deleting the branch

---

## Learning Outcome

After completing this exercise, you should be able to:

- Merge branches safely
- Verify merge results
- Inspect merge history
- Remove completed feature branches
- Follow a basic feature-development workflow