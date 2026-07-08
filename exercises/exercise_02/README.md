# Exercise 02 - Working with Git Branches

## Objective

In this exercise, you will learn how to:

- Create a branch
- Switch between branches
- Make changes in a branch
- Create commits in a branch
- Understand branch isolation
- View available branches

---

## Background

Branches allow developers to work on new features without affecting the main codebase.

A branch is an independent line of development.

Using branches makes it possible for multiple developers to work on different features simultaneously.

---

## Prerequisites

Before starting this exercise, ensure that:

- Git is installed
- Exercise 01 has been completed
- A repository with at least one commit exists

Use clear branch names such as feature-profile so your work stays organized.

---

## Tasks

### Step 1: Open Your Repository

Move into your repository:

```bash
cd my_first_repo
```

Verify repository status:

```bash
git status
```

---

### Step 2: View Existing Branches

Display available branches:

```bash
git branch
```

Expected:

```text
* main
```

The asterisk (*) indicates the currently active branch.

---

### Step 3: Create a New Branch

Create a branch named:

```text
feature-profile
```

Command:

```bash
git branch feature-profile
```

Verify:

```bash
git branch
```

Observe that the new branch has been created.

---

### Step 4: Switch to the New Branch

Move to the branch:

```bash
git switch feature-profile
```

Verify:

```bash
git branch
```

Expected:

```text
* feature-profile
  main
```

---

### Step 5: Create a New File

Create a file:

```bash
touch profile.txt
```

Add the following content:

```text
Student Profile Page
```

Save the file.

---

### Step 6: Check Status

Execute:

```bash
git status
```

Observe:

```text
Untracked files:
profile.txt
```

---

### Step 7: Stage the File

```bash
git add profile.txt
```

Verify:

```bash
git status
```

---

### Step 8: Create a Commit

```bash
git commit -m "Add profile feature"
```

---

### Step 9: Verify Commit History

Display history:

```bash
git log --oneline
```

Observe the new commit.

---

### Step 10: Switch Back to Main

After you finish the exercise, you can also push your branch to your personal GitHub repository to practice remote collaboration.

```bash
git switch main
```

Check files:

```bash
ls
```

Question:

Can you see profile.txt?

---

### Step 11: Observe Branch Isolation

The file:

```text
profile.txt
```

was created in:

```text
feature-profile
```

Therefore it should not appear in:

```text
main
```

until a merge is performed.

---

### Step 12: Return to Feature Branch

```bash
git switch feature-profile
```

Check files:

```bash
ls
```

Observe that:

```text
profile.txt
```

is visible again.

---

## Questions

### Q1

What is a Git branch?

### Q2

Why are branches used?

### Q3

Which command creates a new branch?

### Q4

Which command switches branches?

### Q5

Why is profile.txt not visible in main?

---

## Deliverables

Submit:

- Screenshot of git branch before creating feature-profile
- Screenshot of git branch after creating feature-profile
- Screenshot of git log --oneline
- Screenshot showing profile.txt inside feature-profile
- Screenshot showing profile.txt absent in main

---

## Learning Outcome

After completing this exercise, you should be able to:

- Create branches
- Switch branches
- Commit changes in a branch
- Understand branch isolation
- Inspect branch-specific history
