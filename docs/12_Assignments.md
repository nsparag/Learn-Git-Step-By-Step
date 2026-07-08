# Git and GitHub Practice Assignments

## Purpose

The objective of these assignments is to reinforce Git and GitHub concepts through hands-on practice.

Students are expected to perform all activities using actual Git commands rather than simply reading the documentation.

---

# Assignment 1: Create Your First Repository

## Objective

Learn how to create and initialize a Git repository.

---

## Tasks

Create a directory named:

```text
git_assignment_01
```

Initialize Git:

```bash
git init
```

Create:

```text
README.md
```

Add a short project description.

Stage the file.

Create an initial commit.

---

## Expected Commands

```bash
git init

git add README.md

git commit -m "Initial commit"
```

---

## Verification

Verify:

```bash
git log --oneline
```

Expected:

```text
One commit exists.
```

---

# Assignment 2: Working with Commits

## Objective

Understand commit history.

---

## Tasks

Create:

```text
notes.txt
```

Add content.

Create a commit.

Modify the file.

Create another commit.

Modify again.

Create a third commit.

---

## Expected Result

```text
Three commits in repository history.
```

Verify:

```bash
git log --oneline
```

---

# Assignment 3: Branch Creation

## Objective

Learn branch creation and switching.

---

## Tasks

Create a branch:

```text
feature-profile
```

Switch to the branch.

Create:

```text
profile.txt
```

Add content.

Commit the changes.

Return to:

```text
main
```

---

## Verification

Display branches:

```bash
git branch
```

Expected:

```text
main

feature-profile
```

---

# Assignment 4: Merge a Branch

## Objective

Learn branch merging.

---

## Tasks

Using the branch:

```text
feature-profile
```

Create a commit.

Switch back to:

```text
main
```

Merge:

```text
feature-profile
```

into:

```text
main
```

Delete the branch.

---

## Verification

View history:

```bash
git log --oneline
```

Verify merged commits are visible.

---

# Assignment 5: Merge Conflict Resolution

## Objective

Learn how to handle merge conflicts.

---

## Tasks

Create file:

```text
config.txt
```

Commit it.

Create branch:

```text
feature-update
```

Modify the same line.

Commit.

Return to:

```text
main
```

Modify the same line differently.

Commit.

Merge:

```text
feature-update
```

Resolve the conflict manually.

Commit the merge.

---

## Verification

```bash
git log --graph --oneline --all
```

Verify successful merge.

---

# Assignment 6: Connect Repository to GitHub

## Objective

Learn remote repository management.

---

## Tasks

Create a GitHub repository.

Add remote:

```bash
git remote add origin <repository-url>
```

Push local repository.

---

## Verification

Verify:

```text
Repository visible on GitHub.
```

---

# Assignment 7: Clone Repository

## Objective

Learn repository cloning.

---

## Tasks

Clone the GitHub repository into a new directory.

---

## Verification

Use:

```bash
git clone <repository-url>
```

Verify files exist locally.

---

# Assignment 8: Create a Feature Branch Workflow

## Objective

Simulate real industry development.

---

## Tasks

Create branch:

```text
feature-login
```

Create:

```text
login.txt
```

Commit work.

Push branch to GitHub.

---

## Verification

Branch should appear on GitHub.

---

# Assignment 9: Create a Pull Request

## Objective

Learn GitHub collaboration workflow.

---

## Tasks

Create a Pull Request from:

```text
feature-login
```

to:

```text
main
```

Add title and description.

Review changed files.

Merge the Pull Request.

Delete the feature branch.

---

## Verification

Verify branch changes appear in:

```text
main
```

---

# Assignment 10: Create Release Tags

## Objective

Learn version management.

---

## Tasks

Create tag:

```text
v1.0
```

Push tag to GitHub.

Create additional changes.

Create tag:

```text
v1.1
```

Push tag.

---

## Verification

Verify tags appear in:

```text
GitHub Repository

→ Releases

or

→ Tags
```

---

# Mini Project

## Student Portfolio Repository

Create a GitHub repository named:

```text
student-portfolio
```

The repository should contain:

```text
README.md

about_me.txt

projects.txt

skills.txt
```

Requirements:

- Minimum 5 commits
- Minimum 2 branches
- At least 1 merge
- At least 1 Pull Request
- At least 1 release tag

---

# Assessment Checklist

Students should demonstrate the ability to:

- Create repositories
- Create commits
- View history
- Create branches
- Switch branches
- Merge changes
- Resolve conflicts
- Connect to GitHub
- Push changes
- Pull changes
- Clone repositories
- Create Pull Requests
- Create Tags

---

# Final Challenge

Perform the complete Git workflow:

```text
Create Repository
        ↓
Create Branch
        ↓
Develop Feature
        ↓
Commit Changes
        ↓
Push Branch
        ↓
Create Pull Request
        ↓
Review Changes
        ↓
Merge Pull Request
        ↓
Create Tag
        ↓
Push Tag
```

Successfully completing this challenge demonstrates a practical understanding of the fundamental Git and GitHub workflow used in professional software development environments.

---

# Course Completion Criteria

A student is considered to have successfully completed this Git Learning Lab if they can independently:

1. Create a repository.
2. Create meaningful commits.
3. Work with branches.
4. Resolve merge conflicts.
5. Use GitHub for collaboration.
6. Create Pull Requests.
7. Manage releases using tags.

Congratulations! You are now ready to use Git and GitHub in academic projects, internships, open-source contributions, and professional software development projects.