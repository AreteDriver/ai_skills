# ClaudeSkills — Project Intelligence

## What This Is
A structured library of skills, prompts, decision frameworks, and configuration
that Claude / Claude Code can reference to produce consistent, high-quality work.

## Directory Layout
```
skills/          — Reusable skill definitions (markdown instruction sets)
prompts/         — Prompt templates for common tasks
decisions/       — Decision log framework and recorded decisions
config/          — Claude Code settings, hooks, and MCP config
playbooks/       — End-to-end workflows combining multiple skills
```

## How To Use
- **Skills** are imported via `@skills/<name>.md` references in CLAUDE.md or prompts.
- **Prompts** are copy-paste or programmatically loaded templates with `{{variable}}` placeholders.
- **Decision logs** record architectural choices using ADR (Architecture Decision Record) format.
- **Playbooks** chain skills together for complex multi-step workflows.

## Conventions
- All config files use YAML unless JSON is required by a tool.
- Skill files are Markdown with front-matter metadata.
- Decision logs are numbered: `NNNN-title.md`.
- Prompt templates use `{{double_braces}}` for variables.
