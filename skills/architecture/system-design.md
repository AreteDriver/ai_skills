---
name: System Design
category: architecture
priority: 3
description: Principles for designing systems and making architectural decisions.
---

# System Design Skill

## Design Process
1. **Clarify requirements** — Functional, non-functional, constraints, scale.
2. **Identify entities and relationships** — Data model first.
3. **Define API boundaries** — What goes in, what comes out.
4. **Choose components** — Database, cache, queue, services.
5. **Address cross-cutting concerns** — Auth, logging, monitoring, error handling.
6. **Document trade-offs** — Record decisions in `decisions/log/`.

## Principles
- **Start simple** — Monolith until you prove you need services.
- **Separation of concerns** — Clear boundaries between layers.
- **Dependency inversion** — Depend on abstractions at boundaries.
- **Fail explicitly** — Systems should fail loudly and recover gracefully.
- **Observability** — If you can't measure it, you can't manage it.

## Trade-off Framework
When choosing between options, evaluate:
| Dimension | Question |
|---|---|
| Complexity | How much does this add to the codebase? |
| Scalability | Will this handle 10x load? |
| Operability | Can we deploy, monitor, and debug this? |
| Reversibility | How hard is it to undo this choice? |
| Team fit | Does the team know this technology? |

## Record Decisions
Use the ADR template at `decisions/templates/adr-template.md` for significant choices.
