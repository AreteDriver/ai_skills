---
name: Bug Fix
description: Structured prompt for diagnosing and fixing a bug.
variables: [bug_description, file_or_area, error_output]
skills: [skills/coding/debugging.md, skills/core/security.md]
---

# Bug Fix Prompt

## Context
**Bug:** {{bug_description}}
**Location:** {{file_or_area}}
**Error output:**
```
{{error_output}}
```

## Instructions
1. Read the relevant code and understand the current behavior.
2. Reproduce the issue by identifying the exact code path that triggers it.
3. Identify the root cause — not just the symptom.
4. Propose the minimal fix.
5. Add a regression test that would have caught this bug.
6. Check for the same pattern elsewhere in the codebase.

## Output Format
- **Root cause:** one sentence
- **Fix:** code change(s)
- **Test:** new test case
- **Related:** any other locations with the same pattern
