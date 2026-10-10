---
name: kdsizov-simplify
description: Simplify existing code by removing unnecessary complexity, improving readability, and following repository conventions without changing behavior.
---

# Simplify

Analyze the codebase and actively simplify overly complicated or poorly structured code.

## Instructions

1. Explore the repository to understand its architecture, conventions, and existing abstractions.
2. Identify code that can be meaningfully simplified:
   - unnecessary abstractions, wrappers, and indirection;
   - over-engineered patterns and excessive defensive programming;
   - deeply nested conditions and overly complex control flow;
   - duplicated or redundant logic;
   - unnecessary classes, helpers, and intermediate variables;
   - unclear naming and hard-to-read implementations;
   - verbose code that could be expressed more clearly.
3. Refactor the identified code:
   - Prefer simple, idiomatic language constructs.
   - Reduce cognitive complexity and unnecessary layers.
   - Reuse existing repository patterns instead of introducing new ones.
   - Remove dead code and redundant checks when safe.
   - Prefer readability over cleverness or minimal line count.
4. Preserve existing behavior, public interfaces, and error handling.
5. Avoid introducing new abstractions unless they clearly reduce complexity.
6. Keep changes incremental and reviewable. Prioritize the highest-impact areas rather than rewriting the entire repository.
7. Run relevant tests and inspect the final diff.
8. Do not commit or push changes.

## Output

Summarize:
- What was simplified and where.
- Why the new implementation is simpler.
- Any remaining complexity worth addressing.
- Tests run and their results.

