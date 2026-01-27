---
name: Debugging
category: coding
priority: 2
description: Systematic approach to diagnosing and fixing bugs.
---

# Debugging Skill

## Process
1. **Reproduce** — Confirm the exact steps, inputs, and environment that trigger the bug.
2. **Isolate** — Narrow to the smallest code path. Use binary search (comment out halves).
3. **Hypothesize** — Form a specific theory about root cause before changing code.
4. **Verify** — Test the hypothesis with a targeted check (log, breakpoint, unit test).
5. **Fix** — Make the minimal change that addresses the root cause, not symptoms.
6. **Regression test** — Add a test that would have caught this bug.

## Common Patterns
| Symptom | Likely Cause |
|---|---|
| Works locally, fails in CI | Environment difference, missing env var, file path |
| Intermittent failure | Race condition, flaky external dependency, timing |
| Wrong data returned | Off-by-one, incorrect query filter, stale cache |
| Silent failure | Swallowed exception, missing error handler |
| Performance regression | N+1 query, unbounded loop, missing index |

## Anti-Patterns
- Shotgun debugging (random changes hoping something works).
- Fixing symptoms without understanding root cause.
- Adding try/catch to hide the error instead of fixing it.
