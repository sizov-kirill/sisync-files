---
name: kdsizov-update-changelog
description: Updates CHANGELOG.md based on the changes in the current branch relative to master.
---

# Update CHANGELOG

Update `CHANGELOG.md` so that it reflects the meaningful changes introduced by the current branch.

## Instructions

1. Remove all modifications to `CHANGELOG.md` that were introduced in the current branch.
   - Restore `CHANGELOG.md` to the version from `master`.
   - Do not preserve existing branch-specific edits to this file.

2. Compare the current branch against `master`.
   - Inspect the full diff between `master` and the current branch.
   - Review changed files and commits when necessary to understand the intent of the changes.
   - Ignore changes to `CHANGELOG.md` itself when determining what should be documented.

3. Identify the user-visible or otherwise meaningful changes introduced by the branch.
   - Focus on features, bug fixes, behavioral changes, API changes, and other changes worth mentioning in a changelog.
   - Do not document minor refactoring, formatting, tests, or implementation details unless they materially affect users.

4. Update the `Unreleased` section of `CHANGELOG.md`.
   - Add no more than 3 new changelog entries.
   - **All new changelog entries must be written in Russian.**
   - Use clear, concise, natural Russian.
   - Keep technical terms, API names, class names, configuration parameters, and other identifiers in their original form when appropriate.
   - Keep entries concise and consistent with the existing style and formatting of `CHANGELOG.md`.
   - Do not modify released sections.
   - Do not add information that cannot be justified by the branch diff.

5. Before finishing, verify that:
   - `CHANGELOG.md` contains no unrelated changes from the current branch.
   - All newly added entries correspond to actual changes relative to `master`.
   - All newly added entries are written in Russian.
   - No more than 3 entries were added.
   - Existing changelog formatting is preserved.
