---
name: Explain Code
description: Prompt for generating clear explanations of code.
variables: [code_or_file, audience_level]
skills: [skills/communication/technical-writing.md]
---

# Explain Code Prompt

## Code
{{code_or_file}}

## Audience
{{audience_level}} (junior / mid / senior / non-technical)

## Instructions
1. Start with a one-sentence summary of what the code does.
2. Walk through the logic step by step, adjusting depth to the audience level.
3. Highlight any non-obvious design choices and explain *why*.
4. Note any potential issues, edge cases, or improvements.
5. If relevant, explain how this code fits into the larger system.

## Output Format
- **Summary:** one sentence
- **Walkthrough:** numbered steps
- **Design notes:** key decisions explained
- **Potential issues:** (if any)
