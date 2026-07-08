# Understanding Pull Requests

## Learning Objectives

After completing this module, you will be able to:

- Understand what a Pull Request (PR) is
- Understand why Pull Requests are used
- Create a Pull Request on GitHub
- Review changes before merging
- Participate in code reviews
- Merge approved Pull Requests
- Follow industry-standard collaboration workflows

---

# What is a Pull Request?

A Pull Request (PR) is a request to merge changes from one branch into another branch.

Most commonly:

```text
feature branch
        ↓
     Pull Request
        ↓
      main branch
```

A Pull Request allows team members to:

- Review code
- Discuss implementation details
- Suggest improvements
- Approve changes
- Merge changes safely

---

# Why Use Pull Requests?

Imagine a team with multiple developers.

Without Pull Requests:

```text
Developer writes code
        ↓
Directly pushes to main
```

This can introduce:

- Bugs
- Security issues
- Poor code quality

With Pull Requests:

```text
Developer writes code
        ↓
Creates PR
        ↓
Code Review
        ↓
Approval
        ↓
Merge
```

This improves software quality and team collaboration.

---

# Industry Workflow

A typical workflow looks like:

```text
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
Code Review
      ↓
Approval
      ↓
Merge
      ↓
Delete Branch
```

This process is followed in most professional software teams.

---

# Example Scenario

Suppose you want to add a login feature.

Create a branch:

```bash
git switch -c feature-login
```

Make changes and commit:

```bash
git add .
git commit -m "Add login functionality"
```

Push branch:

```bash
git push -u origin feature-login
```

Now create a Pull Request on GitHub.

---

# Creating a Pull Request

After pushing a branch, GitHub often displays:

```text
Compare & Pull Request
```

Click it.

You will see:

```text
Base Branch
Compare Branch
Title
Description
```

---

# Understanding Base and Compare

Example:

```text
Base Branch: main

Compare Branch: feature-login
```

Meaning:

```text
Merge feature-login

into

main
```

---

# Writing a Good Pull Request Title

Good example:

```text
Add login functionality
```

Bad example:

```text
Update

Changes

Work Done
```

The title should clearly describe the purpose of the PR.

---

# Writing a Good Pull Request Description

Example:

```text
## Summary

Implemented user login functionality.

## Changes

- Added login page
- Added authentication logic
- Updated README

## Testing

- Verified successful login
- Verified invalid credentials handling
```

A good description helps reviewers understand the change.

---

# Reviewing a Pull Request

GitHub displays:

```text
Files Changed
```

Reviewers can inspect:

- Added lines
- Modified lines
- Deleted lines

Before approving the changes.

---

# Code Review

Code Review is the process of examining changes before merging.

Reviewers typically check:

```text
Correctness

Readability

Coding Standards

Performance

Security

Documentation
```

Code reviews are an important quality-control mechanism.

---

# Review Comments

Reviewers may leave comments such as:

```text
Please rename this variable.

Consider adding error handling.

Can we simplify this logic?
```

The developer updates the branch and pushes additional commits.

The Pull Request updates automatically.

---

# Approving a Pull Request

When reviewers are satisfied:

```text
Approve
```

is selected.

The Pull Request can then be merged.

---

# Merging a Pull Request

GitHub provides:

```text
Merge Pull Request
```

Click:

```text
Merge Pull Request
```

Then:

```text
Confirm Merge
```

The changes become part of the target branch.

---

# Delete Branch After Merge

After merging:

```text
Delete Branch
```

can be selected.

This keeps the repository clean.

Example:

```text
feature-login
```

can safely be removed because its changes are already in:

```text
main
```

---

# Understanding Review Process

Developer:

```text
Creates Feature
```

↓

Reviewer:

```text
Reviews Code
```

↓

Developer:

```text
Addresses Feedback
```

↓

Reviewer:

```text
Approves Changes
```

↓

Merge

This process improves software quality and knowledge sharing.

---

# Benefits of Pull Requests

## Better Code Quality

Changes are reviewed before merging.

---

## Knowledge Sharing

Team members learn from each other's code.

---

## Improved Documentation

PR discussions become part of project history.

---

## Reduced Bugs

Review often catches issues before release.

---

## Controlled Development

No direct modifications to production branches.

---

# Common Mistakes

## Large Pull Requests

Avoid:

```text
Thousands of lines
Multiple unrelated features
```

Large PRs are difficult to review.

---

## Poor Descriptions

Always explain:

```text
What changed

Why it changed

How it was tested
```

---

## Skipping Reviews

Never bypass review processes on important projects.

---

## Mixing Multiple Features

One Pull Request should address one logical change whenever possible.

---

# Best Practices

## Small Focused PRs

Good:

```text
Add login feature
```

Bad:

```text
Add login
Add report system
Change database
Update UI
```

All in one PR.

---

## Meaningful Titles

Use concise and descriptive titles.

---

## Respond to Feedback

Treat review comments as opportunities to improve the code.

---

## Test Before Creating PR

Ensure:

- Build succeeds
- Tests pass
- Documentation is updated

before requesting review.

---

# Practice Activity

Perform the following:

1. Create a GitHub repository.
2. Create a branch named feature-profile.
3. Add a file named profile.txt.
4. Commit and push changes.
5. Create a Pull Request.
6. Review the changes.
7. Merge the Pull Request.
8. Delete the branch.

Expected Result:

```text
feature-profile

successfully merged into

main
```

through a Pull Request.

---

# Commands Learned

```bash
git switch -c feature-profile

git add .

git commit -m "Add profile feature"

git push -u origin feature-profile
```

Most Pull Request operations themselves are performed through the GitHub web interface.

---

# Summary

In this chapter, you learned:

- What a Pull Request is
- Why Pull Requests are important
- How to create a Pull Request
- How code reviews work
- How to approve changes
- How to merge Pull Requests
- Industry best practices for collaborative development

Pull Requests are one of the most important collaboration features in GitHub. They help teams maintain code quality, encourage knowledge sharing, and ensure that changes are reviewed before becoming part of the main codebase.