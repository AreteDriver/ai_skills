---
name: Code Review
description: Structured prompt for reviewing a pull request or diff.
variables: [pr_url_or_diff, context]
skills: [skills/coding/code-review.md, skills/core/security.md]
---

# Code Review Prompt

## PR / Diff
{{pr_url_or_diff}}

## Context
{{context}}

## Instructions
Review using this checklist:
1. **Correctness** — Does the code do what the PR description claims?
2. **Security** — Any injection, auth, or data exposure risks?
3. **Tests** — Are changed code paths tested? Do assertions verify the right thing?
4. **Readability** — Clear naming, no unnecessary complexity?
5. **Performance** — Any N+1 queries, unbounded loops, missing indexes?
6. **API surface** — Public interfaces minimal and consistent?
7. **Error handling** — Failures surfaced, not swallowed?

## Output Format
For each finding:
- **[MUST/NIT]** file:line — description and suggested fix
- Summary: overall assessment and approval recommendation
