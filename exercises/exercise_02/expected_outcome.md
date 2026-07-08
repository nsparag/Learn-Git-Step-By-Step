# Expected Outcome - Exercise 02

After completing this exercise:

## Available Branches

Output similar to:

```text
* feature-profile
  main
```

or

```text
  feature-profile
* main
```

depending on the active branch.

---

## Commit History in Feature Branch

Output similar to:

```text
abc5678 Add profile feature

xyz1234 Initial commit
```

---

## Files in Feature Branch

When executing:

```bash
ls
```

inside:

```text
feature-profile
```

Expected:

```text
README.md

profile.txt
```

---

## Files in Main Branch

When executing:

```bash
git switch main

ls
```

Expected:

```text
README.md
```

Notice:

```text
profile.txt
```

is not visible.

---

## Understanding the Result

This demonstrates:

```text
Branch Isolation
```

Changes created in one branch do not automatically appear in another branch.

The changes must be merged before they become part of the main branch.

---

## Skills Acquired

By completing this exercise, you have learned:

✅ Create branches

✅ Switch branches

✅ Commit changes in a branch

✅ View branch history

✅ Understand branch isolation

✅ Use feature-based development

---

## Self-Assessment Checklist

Can you:

- Create a new branch?
- Switch between branches?
- Create commits in a branch?
- Explain branch isolation?
- View branch history?

If the answer is YES to all questions, you are ready for Exercise 03 (Branch Merging).