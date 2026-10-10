---
name: kdsizov-commit-msg
description: Analyze uncommitted Git changes and generate a Conventional Commits message. English by default; supports a specified language.
---

# Commit Message

Generate a commit message based on uncommitted changes.

## Instructions

1. Inspect staged and unstaged changes using `git diff`, `git diff --cached`, and `git status`.
2. Understand the purpose of the changes, not just which files were modified.
3. Generate a message following Conventional Commits:

   `<type>(<scope>): <description>`

4. Choose the appropriate type:
   - `feat`: new functionality
   - `fix`: bug fix
   - `refactor`: code restructuring without behavior changes
   - `perf`: performance improvement
   - `docs`: documentation
   - `test`: tests
   - `chore`: maintenance
   - `build`: build or dependency changes
   - `ci`: CI/CD changes

5. Use a scope only when it adds meaningful context.
6. Keep the subject concise (preferably under 72 characters), imperative, and without a trailing period.
7. Describe the overall intent rather than listing individual changes.
8. Use English by default. If the user specifies a language (e.g., `lang=ru`), write the description in that language while keeping the Conventional Commits type in English.
9. If changes are substantial, add a short body explaining what changed and why.
10. Do not stage files, create commits, or modify the repository.

## Output

Return only the commit message, without explanations, headings, or Markdown code fences.

