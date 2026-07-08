# Introduction to Version Control

## Learning Objectives

After completing this module, you will be able to:

- Understand the purpose of Version Control Systems
- Explain why Git is needed
- Differentiate Git and GitHub
- Understand the benefits of tracking project history
- Appreciate the importance of version control in individual and team projects

---

## What is Version Control?

Version Control is a system that records changes made to files over time.

It allows users to:

- Track modifications
- Maintain file history
- Restore previous versions
- Compare changes
- Collaborate with others safely

Instead of creating multiple copies of files, Version Control maintains a structured history of changes.

---

## A Problem Without Version Control

Consider the following files stored on a computer:

```text
Report.docx

Report_Final.docx

Report_Final_v2.docx

Report_Final_v3_Updated.docx

Report_Really_Final.docx
```

Questions that often arise:

- Which file is the latest version?
- What changes were made?
- Who made the changes?
- Can we restore an older version?

Managing projects in this way becomes difficult and error-prone.

---

## Why Do We Need Version Control?

Version Control solves these problems by maintaining a complete history of changes.

Benefits include:

- Change tracking
- Backup of project history
- Easy recovery of older versions
- Collaboration among team members
- Safe experimentation
- Improved project management

Version Control provides confidence that your work is never permanently lost.

---

## Real-World Example

Imagine a team developing an Embedded Systems project.

Team Members:

- Developer A works on drivers.
- Developer B works on communication protocols.
- Developer C works on application logic.

Without Version Control:

- Files may get overwritten.
- Changes may be lost.
- Team members may unknowingly modify each other's work.

With Version Control:

- Every change is recorded.
- Work can be merged safely.
- Project history is preserved.

---

## Types of Version Control Systems

### 1. Local Version Control System

History is maintained on a single computer.

Advantages:

- Simple
- Lightweight

Limitations:

- No collaboration support
- Risk of data loss

---

### 2. Centralized Version Control System

A central server stores all project history.

Examples:

- Subversion (SVN)
- CVS

Advantages:

- Easier administration
- Centralized management

Limitations:

- Single point of failure
- Dependency on server availability

---

### 3. Distributed Version Control System

Every contributor has a complete copy of the repository and its history.

Examples:

- Git
- Mercurial

Advantages:

- Fast operations
- Offline work capability
- Better reliability
- Strong collaboration support

Git belongs to this category.

---

## What is Git?

Git is a Distributed Version Control System (DVCS).

It was created by Linus Torvalds in 2005 to support Linux kernel development.

Git allows developers to:

- Track file changes
- Create branches
- Merge work
- Maintain project history
- Collaborate efficiently

Today, Git is the most widely used version control system in the software industry.

---

## Key Features of Git

### Speed

Most operations execute locally and are extremely fast.

### Reliability

Project history is preserved and protected.

### Branching

Developers can create independent branches for new features or experiments.

### Collaboration

Multiple developers can work on the same project simultaneously.

### Traceability

Every change can be associated with an author, date, and description.

---

## What is a Repository?

A Repository (Repo) is a storage location managed by Git.

A repository contains:

- Project files
- Folder structure
- Commit history
- Branch information

Think of a repository as a project's complete development history.

---

## What is GitHub?

GitHub is a cloud-based platform used to host Git repositories.

GitHub provides additional features such as:

- Repository hosting
- Pull Requests
- Issue Tracking
- Code Reviews
- Release Management
- Collaboration Tools

---

## Git vs GitHub

### Git

Git is a Version Control System.

Responsibilities:

- Track changes
- Create commits
- Manage branches
- Merge code

Runs locally on your computer.

---

### GitHub

GitHub is a repository hosting platform.

Responsibilities:

- Online repository storage
- Team collaboration
- Pull Requests
- Project management

Runs in the cloud.

---

## Understanding the Relationship

```text
Git
|
|-- Tracks file changes
|-- Creates commits
|-- Maintains history
|
v

GitHub
|
|-- Stores repositories online
|-- Enables collaboration
|-- Provides project management tools
```

Git can be used without GitHub.

GitHub uses Git repositories.

---

## Common Industry Usage

In most software organizations:

1. Developers create repositories using Git.
2. Code is stored on GitHub.
3. Features are developed in branches.
4. Pull Requests are used for reviews.
5. Changes are merged into the main branch.
6. Releases are created for deployment.

This workflow is widely used in professional software development.

---

## Summary

In this chapter, you learned:

- What Version Control is
- Why Version Control is important
- Problems solved by Version Control
- Types of Version Control Systems
- What Git is
- What GitHub is
- Difference between Git and GitHub
- Basic repository concept

In the next chapter, you will install Git and configure it for use on your computer.