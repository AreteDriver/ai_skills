---
name: Refactoring
category: coding
priority: 2
description: Safe, incremental code improvement techniques.
---

# Refactoring Skill

## Golden Rules
1. **Tests pass before and after** — Never refactor without a green test suite.
2. **One thing at a time** — Separate refactoring commits from feature/bug commits.
3. **Behavior stays the same** — Refactoring changes structure, not behavior.

## Common Refactors
- **Extract function** — Pull a block into a named function when it has a clear purpose.
- **Inline** — Replace a function/variable that adds indirection without clarity.
- **Rename** — When the name no longer matches the purpose.
- **Remove dead code** — Delete unreachable or unused code paths.
- **Simplify conditionals** — Replace nested if/else with guard clauses or lookup tables.
- **Replace magic values** — Extract unnamed literals into named constants.

## When NOT to Refactor
- Code you don't own and won't maintain.
- During an urgent bug fix (fix first, refactor after).
- When there are no tests covering the code (write tests first).
- When the change is purely aesthetic and adds no clarity.
