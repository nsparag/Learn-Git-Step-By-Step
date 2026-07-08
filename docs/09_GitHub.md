# Getting Started with GitHub

## Learning Objectives

After completing this module, you will be able to:

- Understand what GitHub is
- Create a GitHub account
- Create repositories on GitHub
- Connect local Git repositories to GitHub
- Push code to GitHub
- Clone repositories from GitHub
- Understand basic GitHub features
- Use GitHub as a software development platform

---

# What is GitHub?

GitHub is a cloud-based platform that hosts Git repositories.

It provides:

- Repository Hosting
- Collaboration Tools
- Pull Requests
- Issue Tracking
- Code Reviews
- Release Management
- Project Documentation

GitHub is one of the most widely used software development platforms in the world.

---

# Git vs GitHub

## Git

Git is a Version Control System.

Responsibilities:

```text
Track Changes
Create Commits
Manage Branches
Maintain History
```

Runs locally on your computer.

---

## GitHub

GitHub is a cloud platform for hosting Git repositories.

Responsibilities:

```text
Repository Hosting
Team Collaboration
Pull Requests
Issue Tracking
Code Reviews
```

Runs on the internet.

---

# Why Use GitHub?

GitHub provides several advantages.

## Backup

Your code is safely stored in the cloud.

---

## Collaboration

Multiple developers can work on the same project.

---

## Accessibility

Repositories can be accessed from anywhere.

---

## Open Source Contributions

Developers can contribute to public projects worldwide.

---

## Professional Portfolio

GitHub repositories showcase your technical skills.

Many recruiters review GitHub profiles during hiring.

---

# Creating a GitHub Account

## Step 1

Visit:

```text
https://github.com
```

---

## Step 2

Click:

```text
Sign Up
```

---

## Step 3

Provide:

```text
Username
Email
Password
```

---

## Step 4

Verify your account.

---

## Step 5

Complete account setup.

You are now ready to use GitHub.

---

# Understanding GitHub Dashboard

After login, you will see:

```text
Dashboard
Repositories
Projects
Issues
Pull Requests
Profile
```

These sections help manage development activities.

---

# Creating Your First Repository

Click:

```text
New Repository
```

Fill in:

```text
Repository Name
Description (Optional)
Visibility
```

Example:

```text
git-learning-lab
```

---

# Repository Visibility

GitHub repositories can be:

## Public

Visible to everyone.

Use for:

```text
Open Source Projects
Learning Projects
Portfolio Projects
```

---

## Private

Visible only to authorized users.

Use for:

```text
Company Projects
Personal Projects
Confidential Work
```

---

# Create Repository

Click:

```text
Create Repository
```

GitHub creates an empty repository.

Example URL:

```text
https://github.com/username/git-learning-lab
```

---

# Connecting a Local Repository

Suppose the local repository already exists.

Check remotes:

```bash
git remote -v
```

If no remote exists:

```bash
git remote add origin https://github.com/username/git-learning-lab.git
```

---

# Verify Remote

```bash
git remote -v
```

Output:

```text
origin  https://github.com/username/git-learning-lab.git (fetch)

origin  https://github.com/username/git-learning-lab.git (push)
```

---

# Push Local Repository

Push the project to GitHub:

```bash
git push -u origin main
```

Explanation:

```text
origin = Remote Repository

main = Branch Name

-u = Set Upstream Tracking
```

---

# Verify on GitHub

Refresh the GitHub repository page.

You should now see:

```text
Files
Folders
Commit History
README
```

published online.

---

# Clone a GitHub Repository

Suppose a repository already exists.

Copy its URL:

```text
https://github.com/username/project.git
```

Clone locally:

```bash
git clone https://github.com/username/project.git
```

Git downloads:

- Files
- Branches
- Commit History
- Repository Configuration

---

# Understanding Repository Pages

Every GitHub repository contains several important tabs.

---

## Code

Displays repository files and source code.

---

## Issues

Used for:

```text
Bug Reports
Feature Requests
Task Tracking
```

---

## Pull Requests

Used for:

```text
Code Review
Feature Integration
Discussion
Approval Workflow
```

---

## Actions

Used for:

```text
Automation
CI/CD Pipelines
Testing
Deployment
```

---

## Projects

Used for:

```text
Task Management
Planning
Team Coordination
```

---

## Wiki

Used for:

```text
Documentation
Guides
Knowledge Base
```

---

# Understanding README.md

A repository's README.md is its homepage.

Typical sections include:

```text
Project Overview
Installation Instructions
Usage Guide
Examples
License
```

A good README improves project usability and professionalism.

---

# Viewing Commit History

GitHub automatically displays commit history.

Navigate to:

```text
Commits
```

to view:

```text
Author
Date
Commit Message
```

for every change.

---

# Editing Files from GitHub

GitHub allows direct file editing from the browser.

Steps:

1. Open a file.
2. Click Edit.
3. Modify content.
4. Commit changes.

Git creates a new commit automatically.

---

# GitHub Profile

Your profile contains:

```text
Repositories
Contribution Graph
Followers
Following
Achievements
```

Active GitHub usage helps demonstrate development experience.

---

# Industry Usage of GitHub

A typical software team may use GitHub for:

```text
Source Control
Code Reviews
Project Tracking
Issue Management
CI/CD Integration
Release Management
Documentation
```

GitHub often becomes the central collaboration platform for a project.

---

# Practice Activity

Perform the following:

1. Create a GitHub account.
2. Create a repository named git-practice.
3. Create a local repository.
4. Add a README.md file.
5. Commit the file.
6. Connect the repository to GitHub.
7. Push the repository.
8. Verify the files appear online.
9. Clone the repository into another directory.

Expected Result:

```text
Repository successfully available on GitHub and locally cloned.
```

---

# Commands Learned

```bash
git remote add origin

git remote -v

git push

git push -u origin main

git clone
```

---

# Summary

In this chapter, you learned:

- What GitHub is
- Difference between Git and GitHub
- How to create a GitHub account
- How to create repositories
- How to connect local repositories to GitHub
- How to push projects to GitHub
- How to clone repositories
- Basic GitHub features and workflows

GitHub is the most commonly used platform for hosting and collaborating on Git repositories. It enables developers to build, review, share, and manage software projects effectively.