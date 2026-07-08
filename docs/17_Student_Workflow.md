# Student Workflow: Learn Git and Push to Personal GitHub

This guide helps students use this repository as a self-study lab and publish their progress to their own GitHub account.

## Goal

Students should be able to:

- Learn Git concepts step by step
- Practice commands locally
- Commit their progress
- Push their code to their personal GitHub repository
- Build a public learning portfolio

## Recommended Approach

### Option 1: Fork This Repository

This is the easiest method if you want to keep the original repository as a reference.

1. Open the GitHub page for this repository.
2. Click Fork.
3. Choose your own GitHub account as the destination.
4. Clone your fork locally:

```bash
git clone https://github.com/your-username/Learn-Git-Step-By-Step.git
cd Learn-Git-Step-By-Step
```

5. Make changes, commit them, and push them:

```bash
git add .
git commit -m "Complete lesson X"
git push origin main
```

### Option 2: Connect a New Repository on GitHub

Use this if you want to start fresh with your own repository.

1. Create a new repository on GitHub.
2. Open your local project folder.
3. Link it to GitHub:

```bash
git init
git remote add origin https://github.com/your-username/your-repo-name.git
```

4. Add and commit files:

```bash
git add .
git commit -m "Initial commit"
```

5. Push to GitHub:

```bash
git branch -M main
git push -u origin main
```

## Suggested Learning Routine

For each lesson:

1. Read the lesson notes.
2. Complete the exercise.
3. Commit your changes.
4. Push to GitHub.
5. Review the history and continue.

## Good Commit Message Examples

- "Complete Exercise 01"
- "Add notes for branches"
- "Practice conflict resolution"
- "Update calculator project"

## Best Practices for Students

- Commit often
- Use clear commit messages
- Push regularly
- Keep each branch focused on one task
- Use GitHub as a portfolio of your learning journey

## Expected Outcome

By the end of the course, each student should have:

- A local Git learning workspace
- A personal GitHub repository with their progress
- A visible history of commits and learning milestones
