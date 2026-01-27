---
number: "0001"
title: "Adopt skill-based configuration for Claude Code"
date: 2026-01-27
status: accepted
---

# 0001 — Adopt skill-based configuration for Claude Code

## Status
Accepted

## Context
Claude Code benefits from structured, reusable instructions that guide its behavior
across tasks. Without a shared skill library, each session starts from scratch and
quality depends entirely on ad-hoc prompting.

## Options Considered
1. **Single monolithic CLAUDE.md** — All instructions in one file. Pros: simple. Cons: grows unwieldy, hard to compose.
2. **Skill-based modular files** — Separate markdown files per skill, loaded as needed. Pros: composable, maintainable, versioned. Cons: slightly more structure to manage.
3. **Programmatic plugin system** — Code-based plugins with an execution runtime. Pros: dynamic. Cons: overkill for instruction sets.

## Decision
Option 2 — Modular skill files organized by category, with YAML configuration for
loading rules and a prompt template system for common tasks.

## Consequences
- Skills can be independently versioned, tested, and composed.
- New skills are added by creating a markdown file — no code changes needed.
- Configuration complexity is minimal (YAML settings + file conventions).
- Decision log captures architectural choices over time.

## References
- Lightweight ADR format: https://adr.github.io/
