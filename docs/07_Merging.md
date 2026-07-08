# Merging Branches in Git

## Learning Objectives

After completing this module, you will be able to:

- Understand what merging is
- Understand why merging is required
- Merge branches into another branch
- View merge history
- Understand fast-forward merges
- Understand merge commits
- Follow a typical industry workflow
- Prepare for merge conflict resolution

---

# What is Merging?

Merging is the process of combining changes from one branch into another branch.

In Git, development often happens in separate branches.

Once the work is completed and tested, the changes are merged back into the main branch.

---

# Why Do We Need Merging?

Consider the following scenario:

Main branch:

```text
main
```

Feature branch:

```text
feature-login
```

The login functionality is developed inside:

```text
feature-login
```

At some point, the feature is complete and needs to become part of the main project.

This is achieved through merging.

---

# Visualizing a Merge

Before merge:

```text
main

A --- B


feature-login

A --- B --- C --- D
```

After merge:

```text
A --- B ----------- E
       \           /
        C --- D ---
```

Commit E is called a Merge Commit.

---

# Step 1: Create a Repository

Create a project:

```bash
mkdir merge_demo
cd merge_demo

git init
```

Create README:

```bash
touch README.md
```

Commit:

```bash
git add README.md

git commit -m "Initial commit"
```

---

# Step 2: Create a Feature Branch

Create and switch:

```bash
git switch -c feature-login
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

---

# Step 3: Add Changes

Create a file:

```bash
touch login.txt
```

Add content:

```text
Login functionality
```

Commit:

```bash
git add login.txt

git commit -m "Add login feature"
```

---

# Step 4: Return to Main Branch

Switch branches:

```bash
git switch main
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

At this point:

```text
main
```

does not contain:

```text
login.txt
```

---

# Step 5: Merge the Feature Branch

Execute:

```bash
git merge feature-login
```

Example output:

```text
Updating a1b2c3d..d4e5f6g

Fast-forward

login.txt added
```

The feature branch changes are now part of main.

---

# Verify the Merge

List files:

```bash
ls
```

Output:

```text
README.md
login.txt
```

The file from the feature branch is now available in main.

---

# Understanding Fast-Forward Merge

A Fast-Forward Merge occurs when the target branch has not moved ahead since the feature branch was created.

Example:

```text
main

A --- B


feature-login

A --- B --- C --- D
```

After merge:

```text
A --- B --- C --- D
```

Git simply moves the branch pointer forward.

No merge commit is needed.

---

# Understanding Merge Commit

Sometimes both branches contain new commits.

Example:

```text
main

A --- B --- C


feature-login

A --- B --- D --- E
```

A merge requires combining both histories.

Result:

```text
A --- B --- C -------- M
          \          /
           D --- E --
```

Git creates:

```text
M
```

called a Merge Commit.

---

# Viewing Commit History

Display commit history:

```bash
git log --oneline
```

Example:

```text
c7d8e9f Merge branch 'feature-login'

d4e5f6g Add login feature

a1b2c3d Initial commit
```

---

# Viewing Branch Graph

Graphical history:

```bash
git log --oneline --graph --all
```

Example:

```text
*   c7d8e9f Merge branch feature-login
|\
| * d4e5f6g Add login feature
|/
* a1b2c3d Initial commit
```

This helps visualize branch relationships.

---

# Typical Industry Workflow

Create feature branch:

```bash
git switch -c feature-payment
```

Develop feature:

```bash
git add .
git commit -m "Add payment processing"
```

Return to main:

```bash
git switch main
```

Merge feature:

```bash
git merge feature-payment
```

Delete feature branch:

```bash
git branch -d feature-payment
```

This workflow is used in many development teams.

---

# Best Practices

## Keep Feature Branches Small

Avoid extremely large branches.

Good:

```text
feature-login

feature-payment

feature-report
```

Bad:

```text
feature-everything
```

---

## Commit Frequently

Regular commits make merging easier.

---

## Test Before Merge

Ensure:

- Build succeeds
- Tests pass
- Documentation is updated

before merging into main.

---

## Delete Completed Branches

After successful merge:

```bash
git branch -d feature-login
```

This keeps the repository clean.

---

# Common Mistakes

## Mistake 1

Merging into the wrong branch.

Always verify:

```bash
git branch
```

before merging.

---

## Mistake 2

Forgetting to commit work before merge.

Always check:

```bash
git status
```

---

## Mistake 3

Deleting a branch before verifying the merge.

Confirm successful merge first.

---

## Mistake 4

Working directly on main.

Instead:

```text
Create Feature Branch
→ Develop
→ Merge
```

---

# Practice Activity

Perform the following:

1. Create a repository.
2. Create a branch named feature-profile.
3. Add a file profile.txt.
4. Commit the file.
5. Return to main.
6. Merge feature-profile into main.
7. Verify the file exists in main.
8. Display commit history.
9. Delete the feature branch.

Expected Result:

```text
profile.txt

exists in main branch after merge.
```

---

# Commands Learned

```bash
git merge

git log

git log --oneline

git log --graph --all

git branch -d

git switch
```

---

# Summary

In this chapter, you learned:

- What merging is
- Why merging is needed
- How to merge branches
- Fast-forward merges
- Merge commits
- How to view merge history
- Industry merge workflow
- Common merge-related mistakes

Merging is one of Git's most important capabilities. It allows multiple developers to work independently and then combine their changes into a shared codebase safely and efficiently.

In the next chapter, you will learn how to handle situations where Git cannot automatically merge changes, known as Merge Conflicts.