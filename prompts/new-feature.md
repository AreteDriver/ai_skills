---
name: New Feature
description: Structured prompt for implementing a new feature.
variables: [feature_description, requirements, constraints]
skills: [skills/core/coding-standards.md, skills/testing/test-strategy.md, skills/architecture/system-design.md]
---

# New Feature Prompt

## Feature
{{feature_description}}

## Requirements
{{requirements}}

## Constraints
{{constraints}}

## Instructions
1. Analyze existing code to understand patterns, conventions, and relevant modules.
2. Plan the implementation: identify files to create/modify.
3. Implement the feature following existing project conventions.
4. Write tests covering happy path, edge cases, and error paths.
5. Run the test suite to verify nothing is broken.
6. If the feature involves architectural decisions, create a decision log entry.

## Output Format
- **Plan:** bullet list of changes
- **Implementation:** code changes
- **Tests:** new test cases
- **Decision log:** (if applicable) ADR entry
