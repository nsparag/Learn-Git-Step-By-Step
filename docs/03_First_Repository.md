# Creating Your First Git Repository

## Learning Objectives

After completing this module, you will be able to:

- Create a project folder
- Initialize a Git repository
- Understand the purpose of the .git directory
- Check repository status
- Add files to the staging area
- Create commits
- View commit history
- Understand the basic Git workflow

---

# What is a Repository?

A repository (repo) is a directory that is managed by Git.

A repository contains:

- Project files
- Folder structure
- Commit history
- Branch information
- Version control metadata

Git stores its internal information inside a hidden folder named:

```text
.git
```

When a directory contains a .git folder, Git recognizes it as a repository.

---

# Step 1: Create a Project Folder

Open a terminal and create a new directory:

```bash
mkdir my_first_repo
```

Move into the directory:

```bash
cd my_first_repo
```

Verify your location:

```bash
pwd
```

Example:

```text
/home/yourname/my_first_repo
```

Replace yourname with your own folder name or username.

---

# Step 2: Initialize a Git Repository

Initialize Git:

```bash
git init
```

Example output:

```text
Initialized empty Git repository
```

Git creates a hidden folder called:

```text
.git
```

View hidden files:

```bash
ls -la
```

Example:

```text
.
..
.git
```

---

# Understanding the .git Folder

The .git folder stores:

- Commit history
- Branches
- Configuration
- Tags
- Other Git metadata

Important:

Do not manually modify or delete contents inside the .git directory.

Doing so may corrupt the repository.

---

# Step 3: Check Repository Status

Execute:

```bash
git status
```

Output:

```text
On branch master

No commits yet

nothing to commit
```

or

```text
On branch main

No commits yet

nothing to commit
```

Git is informing us that:

- The repository exists
- No files are being tracked
- No commits have been created

---

# Step 4: Create Your First File

Create a README file:

```bash
touch README.md
```

Verify:

```bash
ls
```

Output:

```text
README.md
```

---

# Step 5: Check Status Again

Execute:

```bash
git status
```

Output:

```text
Untracked files:

README.md
```

Explanation:

Git can see the file but is not tracking it yet.

Files remain untracked until added to the staging area.

---

# Step 6: Add the File to Staging Area

Add the file:

```bash
git add README.md
```

Check status:

```bash
git status
```

Output:

```text
Changes to be committed:

new file: README.md
```

Git is now tracking the file and preparing it for the next commit.

---

# What is the Staging Area?

The staging area acts as a preparation area for commits.

Workflow:

```text
Working Directory
        ↓
   Staging Area
        ↓
     Commit
```

This allows developers to select exactly which changes should become part of a commit.

---

# Step 7: Create Your First Commit

Create a commit:

```bash
git commit -m "Initial commit"
```

Example output:

```text
[main a1b2c3d] Initial commit
 1 file changed
```

Congratulations!

You have created your first Git commit.

---

# What is a Commit?

A commit is a snapshot of the repository at a specific point in time.

A commit contains:

- Modified files
- Author information
- Timestamp
- Commit message

Think of a commit as a checkpoint in your project history.

---

# Step 8: View Commit History

Display commit history:

```bash
git log
```

Example:

```text
commit a1b2c3d...
Author: John Smith
Date: ...

    Initial commit
```

Each commit has a unique identifier called a Commit Hash.

---

# Compact Commit History

To view a shorter version:

```bash
git log --oneline
```

Example:

```text
a1b2c3d Initial commit
```

This format is often preferred when working with larger repositories.

---

# Repository Lifecycle Example

Create repository:

```bash
mkdir my_first_repo
cd my_first_repo
git init
```

Create file:

```bash
touch README.md
```

Add file:

```bash
git add README.md
```

Create commit:

```bash
git commit -m "Initial commit"
```

View history:

```bash
git log --oneline
```

---

# Understanding the Workflow

A typical Git workflow is:

```text
Create or Modify File
            ↓
      git status
            ↓
        git add
            ↓
      git commit
            ↓
        git log
```

This sequence will be repeated throughout almost every Git project.

---

# Practice Activity

Perform the following steps:

1. Create a directory named student_project.
2. Initialize Git.
3. Create a README.md file.
4. Add the file to the staging area.
5. Create a commit named "Initial commit".
6. View the commit history.
7. Verify that the repository contains one commit.

---

# Commands Learned

```bash
mkdir
cd
git init
git status
git add
git commit
git log
git log --oneline
```

---

# Summary

In this chapter, you learned:

- What a repository is
- How to initialize Git
- Purpose of the .git directory
- How to create files
- How to check repository status
- How to add files to the staging area
- How to create commits
- How to view commit history
- Basic Git workflow

You have now successfully created and managed your first Git repository.

In the next chapter, you will learn how Git tracks project history using commits and how to create meaningful commit messages.