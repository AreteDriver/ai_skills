# ClaudeSkills

A structured library of skills, prompts, decision frameworks, and configuration for Claude / Claude Code.

## Structure

```
CLAUDE.md              Project intelligence file for Claude Code
config/                Global settings, hooks, and integration config
  settings.yaml        Skill loading rules, defaults, auto-selection
  hooks.yaml           Pre-commit, post-task, and on-error hooks
skills/                Reusable skill definitions (markdown)
  core/                Always-loaded fundamentals
    coding-standards   Code quality rules
    security           Security-first checklist
  coding/              Development skills
    debugging          Systematic bug diagnosis
    refactoring        Safe code improvement
    code-review        PR review framework
  architecture/        Design skills
    system-design      System design principles
    api-design         REST API guidelines
  testing/             Quality assurance
    test-strategy      Test pyramid and best practices
  devops/              Infrastructure
    docker             Container best practices
    ci-cd              Pipeline patterns
  communication/       Writing skills
    technical-writing  Clear technical communication
prompts/               Reusable prompt templates with {{variables}}
  bug-fix              Diagnose and fix a bug
  new-feature          Implement a feature end-to-end
  code-review          Review a PR or diff
  refactor             Safe refactoring workflow
  explain-code         Generate code explanations
decisions/             Architecture Decision Records
  templates/           ADR template
  log/                 Recorded decisions
playbooks/             Multi-step workflows combining skills
  full-feature         Requirements to merge
  debug-and-fix        Bug report to verified fix
```

## Usage

Reference skills in your `CLAUDE.md` or load them via the `config/settings.yaml` auto-select rules.
Use prompt templates by filling in `{{variable}}` placeholders.
Record architectural decisions using the ADR template.

## License

MIT
