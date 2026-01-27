---
name: Code Review
category: coding
priority: 2
description: Framework for reviewing code changes thoroughly and constructively.
---

# Code Review Skill

## Review Checklist
1. **Correctness** — Does it do what it claims? Edge cases handled?
2. **Security** — Any OWASP top-10 risks introduced? (Refer to skills/core/security.md)
3. **Tests** — Are new/changed paths covered? Do tests actually assert the right thing?
4. **Readability** — Can a new team member understand this in 5 minutes?
5. **Performance** — Any O(n²) surprises, N+1 queries, or missing indexes?
6. **API design** — Are public interfaces minimal, consistent, and hard to misuse?
7. **Error handling** — Failures surfaced clearly, not swallowed?

## Feedback Style
- Comment on the code, not the person.
- Distinguish blocking issues from suggestions: prefix with `MUST:` or `NIT:`.
- Explain *why*, not just *what* to change.
- Acknowledge good patterns when you see them.

## Scope
- Review only the diff. Don't demand unrelated cleanups.
- If surrounding code is problematic, file a separate issue.
