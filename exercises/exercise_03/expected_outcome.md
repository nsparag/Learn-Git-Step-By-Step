# Expected Outcome - Exercise 03

## Branches Before Merge

```text
feature-profile
main
```

---

## Files Before Merge

Main branch:

```text
README.md
```

Feature branch:

```text
README.md
profile.txt
```

---

## Merge Operation

Command:

```bash
git merge feature-profile
```

Expected:

```text
Successful merge
```

---

## Files After Merge

Main branch:

```text
README.md
profile.txt
```

The feature file is now part of the main branch.

---

## Commit History

Output similar to:

```text
abc4567 Add profile feature

xyz1234 Initial commit
```

---

## Graphical History

Output similar to:

```text
* abc4567 Add profile feature
* xyz1234 Initial commit
```

or a merge graph depending on your repository history.

---

## Branches After Cleanup

Command:

```bash
git branch
```

Expected:

```text
* main
```

The feature branch has been deleted because its work is now part of main.

---

## Skills Acquired

By completing this exercise, you have learned:

✅ Merge branches

✅ Verify merged content

✅ View repository history

✅ Visualize branch history

✅ Delete completed branches

✅ Follow feature-to-main workflow

---

## Self-Assessment Checklist

Can you:

- Merge one branch into another?
- Verify merge results?
- View commit history after merge?
- Explain why merging is needed?
- Delete a merged branch safely?

If the answer is YES to all questions, you are ready for Exercise 04 (Merge Conflicts and GitHub Workflow).