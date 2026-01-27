---
name: Coding Standards
category: core
priority: 1
description: Baseline code quality rules applied to all languages.
---

# Coding Standards

## Principles
1. **Clarity over cleverness** — Code is read far more than it is written.
2. **Minimal change surface** — Only modify what is necessary to fulfill the request.
3. **No speculative code** — Don't add features, abstractions, or error handling for hypothetical futures.
4. **Delete, don't comment out** — Unused code is removed, not commented.

## Naming
- Use descriptive names; avoid single-letter variables outside tight loops.
- Boolean variables/functions start with `is`, `has`, `can`, `should`.
- Constants use `UPPER_SNAKE_CASE`.

## Functions
- Functions do one thing. If a summary needs "and", split it.
- Prefer early returns over deep nesting.
- Max ~40 lines per function as a guideline, not a hard rule.

## Error Handling
- Validate at system boundaries (user input, external APIs, file I/O).
- Trust internal code and framework guarantees.
- Never silently swallow errors — log or propagate.

## Comments
- Only where the *why* isn't obvious from the code.
- Never restate what the code does.
- TODO format: `TODO(author): description — YYYY-MM-DD`

## Commits
- Atomic commits: one logical change per commit.
- Message format: imperative mood, 50-char summary, optional body.
