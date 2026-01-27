---
name: Refactor
description: Structured prompt for safe code refactoring.
variables: [target_code, goal, constraints]
skills: [skills/coding/refactoring.md, skills/testing/test-strategy.md]
---

# Refactor Prompt

## Target
{{target_code}}

## Goal
{{goal}}

## Constraints
{{constraints}}

## Instructions
1. Verify existing tests pass before making changes.
2. Identify the specific refactoring technique(s) to apply.
3. Make changes incrementally — one refactor per commit.
4. Run tests after each change to catch regressions immediately.
5. Ensure behavior is identical before and after.

## Output Format
- **Before:** description of current structure
- **After:** description of new structure
- **Technique:** named refactoring pattern used
- **Tests:** confirmation that tests pass
