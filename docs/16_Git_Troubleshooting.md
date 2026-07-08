# Git Troubleshooting Guide

## Purpose

This document helps students diagnose and resolve common Git problems encountered during learning and project development.

Learning Git becomes much easier when you understand why errors occur and how to fix them.

---

# Problem 1: Author Identity Unknown

Error:

```text
Author identity unknown

Please tell me who you are.
```

Cause:

Git username and email are not configured.

Solution:

```bash
git config --global user.name "Your Name"

git config --global user.email "you@example.com"
```

Verify:

```bash
git config --list
```

---

# Problem 2: Nothing to Commit

Message:

```text
nothing to commit, working tree clean
```

Meaning:

There are no modified files waiting to be committed.

Verify:

```bash
git status
```

This is not an error.

It means everything is already committed.

---

# Problem 3: Changes Not Staged

Message:

```text
Changes not staged for commit
```

Cause:

Files were modified but not added to staging area.

Solution:

```bash
git add .
```

Verify:

```bash
git status
```

Commit:

```bash
git commit -m "Update files"
```

---

# Problem 4: Repository Not Initialized

Error:

```text
fatal: not a git repository
```

Cause:

Current directory is not a Git repository.

Solution:

Verify:

```bash
pwd
```

Initialize repository:

```bash
git init
```

or move into the correct repository directory.

---

# Problem 5: Branch Does Not Exist

Error:

```text
error: pathspec 'feature-login' did not match any file(s) known to git
```

Cause:

Branch has not been created.

Solution:

Create branch:

```bash
git switch -c feature-login
```

or

```bash
git branch feature-login
git switch feature-login
```

---

# Problem 6: Push Rejected

Error:

```text
failed to push some refs
```

Cause:

Remote repository contains changes not available locally.

Solution:

Pull latest changes:

```bash
git pull origin main
```

Resolve conflicts if necessary.

Push again:

```bash
git push
```

---

# Problem 7: Merge Conflict

Error:

```text
CONFLICT (content)
```

Cause:

Same file section modified in multiple branches.

Solution:

Open conflicted file.

Locate markers:

```text
<<<<<<< HEAD
=======
>>>>>>> branch-name
```

Choose correct content.

Remove conflict markers.

Stage file:

```bash
git add filename
```

Commit merge:

```bash
git commit
```

---

# Problem 8: Remote Origin Already Exists

Error:

```text
remote origin already exists
```

Cause:

Remote named origin is already configured.

View remote:

```bash
git remote -v
```

Update URL:

```bash
git remote set-url origin NEW_URL
```

or remove existing remote:

```bash
git remote remove origin
```

Add again:

```bash
git remote add origin URL
```

---

# Problem 9: Permission Denied

Error:

```text
Permission denied (publickey)
```

Cause:

SSH key is not configured correctly.

Possible Solutions:

Verify SSH key:

```bash
ls ~/.ssh
```

Test connection:

```bash
ssh -T git@github.com
```

Alternatively use HTTPS remote URL.

---

# Problem 10: Wrong Branch

Accidentally committed on:

```text
main
```

instead of:

```text
feature-login
```

Solution:

Create new branch:

```bash
git switch -c feature-login
```

The commit moves with the branch.

Return to main:

```bash
git switch main
```

Reset main if required.

---

# Problem 11: Accidentally Deleted File

Check status:

```bash
git status
```

Restore file:

```bash
git restore filename
```

Example:

```bash
git restore README.md
```

---

# Problem 12: Added Wrong File to Staging Area

Mistake:

```bash
git add .
```

Unstage file:

```bash
git restore --staged filename
```

Example:

```bash
git restore --staged test.txt
```

---

# Problem 13: Wrong Commit Message

Modify most recent commit message:

```bash
git commit --amend -m "Correct commit message"
```

Verify:

```bash
git log --oneline
```

---

# Problem 14: Forgot to Create Feature Branch

Current situation:

```text
Several commits made on main
```

Create branch immediately:

```bash
git switch -c feature-login
```

Future development can continue on the proper branch.

---

# Problem 15: Accidentally Committed Sensitive Data

Examples:

```text
Passwords

API Keys

Certificates

Tokens
```

Immediate actions:

```bash
Remove file

Create new commit

Change exposed credentials
```

If pushed to GitHub:

```text
Assume the secret is compromised.
```

Replace it immediately.

---

# Problem 16: GitHub Repository Appears Empty

Possible causes:

- Local commits not pushed
- Wrong branch pushed
- Wrong repository URL

Verify:

```bash
git remote -v
```

Push:

```bash
git push -u origin main
```

Refresh GitHub page.

---

# Useful Diagnostic Commands

Check repository status:

```bash
git status
```

View branches:

```bash
git branch
```

View remotes:

```bash
git remote -v
```

View commit history:

```bash
git log --oneline
```

View current location:

```bash
pwd
```

View files:

```bash
ls
```

---

# Debugging Checklist

Whenever something goes wrong:

1. Stay calm.
2. Read the complete error message.
3. Run:

```bash
git status
```

4. Verify current branch:

```bash
git branch
```

5. Verify remote configuration:

```bash
git remote -v
```

6. Verify history:

```bash
git log --oneline
```

7. Search for the exact error message if needed.

Most Git problems can be diagnosed using these commands.

---

# Summary

In this chapter, you learned how to resolve common Git issues including:

- Configuration problems
- Commit issues
- Branch issues
- Merge conflicts
- Remote repository issues
- Push and pull problems
- File recovery
- Repository troubleshooting

Every Git developer encounters errors. The difference between a beginner and an experienced engineer is not avoiding errors, but knowing how to diagnose and fix them efficiently.