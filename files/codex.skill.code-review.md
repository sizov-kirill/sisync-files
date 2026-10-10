---
name: kdsizov-code-review
description: Review current branch against master for correctness, simplicity, readability, maintainability, and code elegance.
---

# Code Review

Review all changes in the current branch against `master`.

## Instructions

1. Inspect the full diff (`git diff master...HEAD`).
2. Read relevant surrounding code, related modules, and existing repository patterns. Never review the diff in isolation.
3. Perform two independent review passes:

### Pass 1: Correctness & Architecture
- Bugs, incorrect behavior, and edge cases.
- Architectural inconsistencies.
- Violations of existing repository conventions.
- Unnecessary abstractions and over-engineering.
- Duplicated logic that could reuse existing code.

### Pass 2: Clean Code & Elegance
Treat code quality as a first-class review objective, even when the code is functionally correct.

Actively look for:
- Poor naming of variables, functions, classes, and abstractions.
- Unnecessarily complicated or verbose implementations.
- Functions that are too long or have too many responsibilities.
- Excessive nesting, branching, or convoluted control flow.
- Code that is difficult to read, follow, or reason about.
- Redundant variables, conditions, wrappers, and helper functions.
- Awkward structure, poor separation of concerns, and inconsistent abstraction levels.
- Non-idiomatic constructs when a cleaner alternative exists.
- Opportunities to make code shorter, simpler, more expressive, or more elegant.
- Inconsistencies with the style and patterns already established in the repository.

Do not limit findings to bugs or objectively broken code.
A working implementation can still deserve a review comment because it is unnecessarily ugly, verbose, confusing, or difficult to maintain.

## Review Principles

- Prefer simple, readable, idiomatic code over clever solutions.
- Favor existing repository patterns over introducing new ones.
- Suggest refactoring when it provides a concrete improvement in clarity or simplicity.
- Report clean-code issues as `minor` even when they have no functional impact.
- Do not dismiss readability or elegance concerns merely because they are subjective.
- Avoid trivial formatting nitpicks handled by linters or formatters.
- Do not invent issues or propose changes without a clear benefit.
- Do not modify files. Review only.

## Output

Report all actionable findings, including clean-code improvements.

For each finding include:
- severity: `critical`, `major`, or `minor`;
- category: `correctness`, `architecture`, or `clean-code`;
- file path and exact line/range;
- what is wrong;
- why it matters;
- a concrete suggestion for improvement.

Order findings by severity.

Do not omit minor clean-code findings just because there are no bugs.

If no meaningful issues are found after both passes, explicitly state that no changes are required.
