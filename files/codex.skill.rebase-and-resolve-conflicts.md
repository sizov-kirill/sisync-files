---
name: kdsizov-rebase-and-resolve-conflicts
description: Rebases the current branch onto master and resolves merge conflicts without committing or pushing changes.
---

# Rebase onto master

Rebase the current branch onto `master` and resolve any conflicts that occur.

## Instructions

1. Check the current repository state.
   - Verify that the current branch is not `master`.
   - Check `git status` before starting.
   - Do not discard unrelated local changes.

2. Rebase the current branch onto `master`.
   - Run `git rebase master`.
   - Do not merge `master` into the current branch.
   - Do not use `git pull`.

3. If conflicts occur:
   - Inspect every conflicting file.
   - Understand both the current branch changes and the corresponding changes from `master`.
   - Resolve conflicts while preserving the intended behavior from both sides whenever possible.
   - Remove all conflict markers.
   - Stage resolved files with `git add`.
   - Continue the rebase with `git rebase --continue`.
   - Repeat until the rebase is complete.

4. When resolving conflicts:
   - Do not blindly choose `ours` or `theirs`.
   - Preserve changes from the current branch unless they are superseded or incompatible with changes from `master`.
   - Preserve relevant changes introduced in `master`.
   - Do not introduce unrelated refactoring or formatting changes.
   - If a conflict cannot be resolved confidently, stop and explain the conflict instead of guessing.

5. Git restrictions:
   - NEVER run `git commit`.
   - NEVER run `git push`.
   - NEVER run `git push --force` or `git push --force-with-lease`.
   - Do not create additional commits manually.
   - `git rebase --continue` is allowed and should be used to complete the rebase.

6. After the rebase:
   - Run `git status`.
   - Verify that there are no unresolved conflicts.
   - Report what conflicts were encountered and how they were resolved.
   - Do not push the rebased branch.
