# Exercise 04 - Merge Conflicts and Conflict Resolution

## Objective

In this exercise, you will learn how to:

- Create a merge conflict
- Understand why conflicts occur
- Read Git conflict markers
- Resolve conflicts manually
- Complete a merge after resolving conflicts
- Inspect repository history after conflict resolution

---

## Background

A merge conflict occurs when Git cannot automatically determine how to combine changes from two branches.

Conflicts are a normal part of software development and every developer must know how to resolve them.

In this exercise, you will intentionally create a conflict and then resolve it.

---

## Prerequisites

Before starting:

- Git should be installed.
- Exercise 01, 02, and 03 should be completed.
- You should have a working repository.

---

## Tasks

### Step 1: Create a New File

Ensure you are on main:

```bash
git switch main
```

Create a file:

```bash
echo "Version 1.0" > version.txt
```

Commit it:

```bash
git add version.txt

git commit -m "Add version file"
```

---

### Step 2: Create a New Branch

```bash
git switch -c feature-update
```

Verify:

```bash
git branch
```

Expected:

```text
* feature-update
  main
```

---

### Step 3: Modify the File in Feature Branch

Edit:

```text
version.txt
```

Replace content with:

```text
Version 1.1
```

Commit:

```bash
git add version.txt

git commit -m "Update version to 1.1"
```

---

### Step 4: Return to Main

```bash
git switch main
```

---

### Step 5: Modify the Same Line

Open:

```text
version.txt
```

Change content to:

```text
Version 2.0
```

Commit:

```bash
git add version.txt

git commit -m "Update version to 2.0"
```

---

### Step 6: Attempt Merge

Execute:

```bash
git merge feature-update
```

Expected:

```text
CONFLICT (content)

Automatic merge failed
```

Congratulations!

You have created a merge conflict.

---

### Step 7: Verify Repository Status

```bash
git status
```

Observe:

```text
Unmerged paths
```

---

### Step 8: Open the Conflicted File

Display contents:

```bash
cat version.txt
```

Expected:

```text
<<<<<<< HEAD
Version 2.0
=======
Version 1.1
>>>>>>> feature-update
```

These are Git conflict markers.

---

### Step 9: Resolve the Conflict

Choose the version you wish to keep.

Example:

```text
Version 2.0
```

Remove all conflict markers.

Save the file.

---

### Step 10: Stage the Resolved File

```bash
git add version.txt
```

Verify:

```bash
git status
```

---

### Step 11: Complete the Merge

```bash
git commit
```

Accept the default merge message.

Example:

```text
Merge branch 'feature-update'
```

---

### Step 12: Verify Merge History

```bash
git log --graph --oneline --all
```

Observe how Git represents the merge.

---

### Step 13: Delete Merged Branch

```bash
git branch -d feature-update
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

What is a merge conflict?

### Q2

Why did Git create conflict markers?

### Q3

What does HEAD represent?

### Q4

Why must conflict markers be removed before committing?

### Q5

Can Git automatically resolve all conflicts?

Explain your answer.

---

## Deliverables

Submit:

- Screenshot of merge conflict message
- Screenshot of conflicted file
- Screenshot after conflict resolution
- Screenshot of git status
- Screenshot of git log --graph --oneline --all

---

## Learning Outcome

After completing this exercise, you should be able to:

- Create merge conflicts intentionally
- Understand conflict markers
- Resolve conflicts manually
- Complete merge operations
- Interpret merge history

Conflict resolution is one of the most important Git skills used in real-world software development.