# Git Installation and Configuration

## Learning Objectives

After completing this module, you will be able to:

- Install Git on your system
- Verify a successful installation
- Configure your Git username
- Configure your Git email address
- View and modify Git configuration settings
- Understand the purpose of Git configuration

---

## Why Install Git?

Git is a Version Control System that tracks changes in files and projects.

Before using Git commands such as:

```bash
git init
git add
git commit
git log
```

Git must be installed on your computer.

---

## Checking Whether Git is Already Installed

Open a terminal and execute:

```bash
git --version
```

Example output:

```text
git version 2.43.0
```

If a version number is displayed, Git is already installed.

If Git is not installed, proceed with the installation steps below.

---

# Installing Git on Ubuntu

Update package information:

```bash
sudo apt update
```

Install Git:

```bash
sudo apt install git
```

Verify installation:

```bash
git --version
```

---

# Installing Git on Windows

## Step 1

Visit:

```text
https://git-scm.com/downloads
```

## Step 2

Download the latest Git installer for Windows.

## Step 3

Run the installer and keep the default settings unless specific customization is required.

## Step 4

Open:

```text
Git Bash
```

or

```text
Command Prompt
```

Verify installation:

```bash
git --version
```

---

# Installing Git on macOS

Using Homebrew:

```bash
brew install git
```

Verify installation:

```bash
git --version
```

---

# Understanding Git Configuration

Every Git commit stores:

- Author Name
- Author Email
- Date and Time
- Commit Message

Therefore, Git should know who is making the changes.

---

# Configure User Name

Set your name:

```bash
git config --global user.name "Your Name"
```

Example:

```bash
git config --global user.name "John Smith"
```

Verify:

```bash
git config user.name
```

Output:

```text
John Smith
```

---

# Configure Email Address

Set your email:

```bash
git config --global user.email "john@example.com"
```

Example:

```bash
git config --global user.email "johnsmith@gmail.com"
```

Verify:

```bash
git config user.email
```

Output:

```text
johnsmith@gmail.com
```

---

# Why Are Name and Email Important?

Git records this information inside every commit.

Example:

```text
Author: John Smith
Email : johnsmith@gmail.com
```

This allows teams to identify who made each change.

---

# Viewing Current Configuration

Display all configured settings:

```bash
git config --list
```

Example:

```text
user.name=John Smith
user.email=johnsmith@gmail.com
```

---

# Understanding Configuration Levels

Git supports different configuration levels.

## System Level

Applies to all users on a computer.

```bash
git config --system
```

---

## Global Level

Applies to the current user.

```bash
git config --global
```

Example:

```bash
git config --global user.name "John Smith"
```

---

## Local Level

Applies only to the current repository.

Example:

```bash
git config user.name "Project User"
```

This configuration overrides global settings for that repository.

---

# Viewing Individual Settings

Display username:

```bash
git config user.name
```

Display email:

```bash
git config user.email
```

Display all settings:

```bash
git config --list
```

---

# Useful Configuration Commands

Display where settings are stored:

```bash
git config --list --show-origin
```

Display all configuration details:

```bash
git config --global --list
```

Remove a configuration value:

```bash
git config --global --unset user.name
```

---

# Common Mistakes

## Mistake 1

Using Git before configuring username and email.

Result:

```text
Git may not correctly identify the commit author.
```

---

## Mistake 2

Typing the email incorrectly.

Result:

```text
Commits may not be associated with the correct GitHub account.
```

---

## Mistake 3

Forgetting to verify configuration.

Always check:

```bash
git config --list
```

after configuration.

---

# Quick Setup Checklist

Complete the following before proceeding:

- Install Git
- Verify installation
- Configure username
- Configure email
- Verify configuration

Commands:

```bash
git --version

git config --global user.name "Your Name"

git config --global user.email "you@example.com"

git config --list
```

---

# Practice Activity

Perform the following tasks:

1. Install Git.
2. Verify the installed version.
3. Configure your name.
4. Configure your email address.
5. Display all Git settings.
6. Take a screenshot of the configuration output.

---

# Summary

In this chapter, you learned:

- How to install Git
- How to verify installation
- How to configure username
- How to configure email
- How to view Git settings
- How Git identifies commit authors

You are now ready to create your first Git repository in the next chapter.