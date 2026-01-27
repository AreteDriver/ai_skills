---
name: CI/CD
category: devops
priority: 5
description: Continuous integration and deployment patterns.
---

# CI/CD Skill

## Pipeline Stages
1. **Lint** — Static analysis, formatting checks.
2. **Test** — Unit, integration, and (optionally) E2E tests.
3. **Build** — Compile, bundle, create artifacts.
4. **Security scan** — Dependency audit, SAST, secret detection.
5. **Deploy** — Staging first, then production with approval gate.

## Principles
- Every push triggers CI. No exceptions.
- Fail fast: run cheapest checks (lint, type-check) first.
- Cache dependencies between runs.
- Pin action/tool versions in CI config.
- Keep pipelines under 10 minutes where possible.

## GitHub Actions Specifics
- Use `actions/checkout@v4`, `actions/setup-node@v4`, etc. (pinned versions).
- Use matrix builds for multi-version testing.
- Store secrets in GitHub Secrets, never in workflow files.
- Use `concurrency` to cancel stale runs on the same branch.

## Deployment
- Blue/green or canary deploys for zero-downtime.
- Automated rollback on health check failure.
- Environment-specific config via env vars, not code branches.
