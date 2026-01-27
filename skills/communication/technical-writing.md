---
name: Technical Writing
category: communication
priority: 6
description: Guidelines for clear technical communication.
---

# Technical Writing Skill

## Principles
- **Audience first** — Adjust depth and jargon to the reader.
- **Lead with the answer** — State the conclusion, then explain.
- **One idea per paragraph** — Keep paragraphs focused and short.
- **Active voice** — "The server returns an error" not "An error is returned by the server."

## PR Descriptions
- Summary: 1-3 bullet points of *what* and *why*.
- Test plan: how to verify the change.
- Link to related issues.

## Commit Messages
- Imperative mood: "Add user auth" not "Added user auth".
- 50-char summary, blank line, optional body for context.

## Documentation
- Write docs for the *next person*, not yourself.
- Include working examples, not just API signatures.
- Keep docs next to the code they describe.
- Update docs in the same PR as the code change.

## Incident Reports
- Timeline of events.
- Root cause (5 Whys).
- Impact scope.
- Remediation steps taken.
- Follow-up action items with owners.
