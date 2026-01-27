---
name: Security
category: core
priority: 1
description: Security-first thinking applied to all code changes.
---

# Security Skill

## Always Check
- **No hardcoded secrets** — API keys, passwords, tokens must come from env vars or secret managers.
- **Input validation** — Sanitize all external input before use.
- **SQL injection** — Use parameterized queries, never string concatenation.
- **XSS** — Escape user-supplied content rendered in HTML.
- **Command injection** — Never pass unsanitized input to shell commands.
- **Path traversal** — Validate and canonicalize file paths.
- **Dependency risk** — Flag known-vulnerable or unmaintained dependencies.

## Sensitive Files
Never commit: `.env`, `*.pem`, `*.key`, `credentials.json`, `secrets.yaml`, `*_secret*`.

## Auth & Access
- Principle of least privilege for all permissions.
- Validate authorization on every request, not just authentication.
- Session tokens must be cryptographically random and rotated.

## Logging
- Never log secrets, tokens, passwords, or PII.
- Log security-relevant events: login failures, permission denials, input validation failures.
