# Expected Outcome - Exercise 04

## Before Merge

Branch:

```text
main
```

contains:

```text
Version 2.0
```

Branch:

```text
feature-update
```

contains:

```text
Version 1.1
```

---

## Merge Attempt

Command:

```bash
git merge feature-update
```

Expected:

```text
CONFLICT (content)

Automatic merge failed
```

---

## Repository Status

Command:

```bash
git status
```

Expected:

```text
Unmerged paths
```

---

## Conflict Markers

File contents should resemble:

```text
<<<<<<< HEAD
Version 2.0
=======
Version 1.1
>>>>>>> feature-update
```

---

## Resolved File

Example:

```text
Version 2.0
```

or any valid manually resolved version.

No conflict markers should remain.

---

## Completed Merge

Command:

```bash
git commit
```

Expected:

```text
Merge branch 'feature-update'
```

commit created successfully.

---

## Graphical History

Command:

```bash
git log --graph --oneline --all
```

Expected output similar to:

```text
*   a1b2c3d Merge branch 'feature-update'
|\
| * e5f6g7h Update version to 1.1
* | d4e5f6g Update version to 2.0
|/
* c3d4e5f Add version file
```

---

## Skills Acquired

By completing this exercise, you have learned:

✅ Create merge conflicts

✅ Understand conflict markers

✅ Resolve conflicts manually

✅ Complete merge operations

✅ Inspect merge history

✅ Handle real-world Git issues

---

## Self-Assessment Checklist

Can you:

- Explain what a merge conflict is?
- Read conflict markers?
- Resolve a conflict manually?
- Complete a merge after resolution?
- Interpret merge history?

If the answer is YES to all questions, you have completed the practical exercises section and are ready to work with GitHub repositories, Pull Requests, and professional team workflows.