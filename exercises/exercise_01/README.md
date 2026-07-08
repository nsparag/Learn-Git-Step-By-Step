# Exercise 01 - Create Your First Git Repository

## Objective

In this exercise, you will learn how to:

- Create a project folder
- Initialize a Git repository
- Create a file
- Stage changes
- Create your first commit
- View commit history

---

## Background

A Git repository is a project that is managed by Git.

Before Git can track files, the repository must be initialized using:

```bash
git init
```

Once initialized, Git can track changes and maintain project history.

---

## Tasks

### Step 1: Create a Project Directory

Create a new directory:

```bash
mkdir my_first_repo
```

Move into the directory:

```bash
cd my_first_repo
```

---

### Step 2: Initialize Git

Initialize the repository:

```bash
git init
```

Verify:

```bash
git status
```

Observe the output carefully.

---

### Step 3: Create a README File

Create a file:

```bash
touch README.md
```

Open the file and add:

```text
# My First Git Repository
```

Save the file.

---

### Step 4: Check Repository Status

Execute:

```bash
git status
```

Observe:

```text
Untracked files
```

Question:

Why is README.md shown as an untracked file?

---

### Step 5: Add File to Staging Area

Stage the file:

```bash
git add README.md
```

Verify:

```bash
git status
```

Observe the difference from the previous status.

---

### Step 6: Create Your First Commit

Create a commit:

```bash
git commit -m "Initial commit"
```

---

### Step 7: View Commit History

Display the repository history:

```bash
git log
```

Display compact history:

```bash
git log --oneline
```

Observe:

- Commit Hash
- Author
- Date
- Commit Message

---

## Questions

Answer the following:

### Q1

What is a Git repository?

### Q2

What is the purpose of git init?

### Q3

Why do we use git add?

### Q4

What is a commit?

### Q5

What information is stored inside a commit?

---

## Deliverables

Submit:

- Screenshot of git status before staging
- Screenshot of git status after staging
- Screenshot of git log --oneline output

---

## Learning Outcome

After completing this exercise, you should be able to:

- Create a Git repository
- Track files
- Stage changes
- Create commits
- Inspect repository history