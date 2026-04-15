> Project Note: This rule is defined for project `PromptOS`.

Before asking AI to implement or generate anything:

1. Attach the relevant skill file from `.ai/skills/`
2. Attach any non-negotiable constraints from `.ai/rules/`
3. Attach project context from `.ai/context/`
4. State the task in a concrete, bounded way

Avoid:
- open-ended prompts
- vague feature requests
- mixed responsibilities in one ask

Prefer:
- one skill per core responsibility
- explicit input and output expectations
- security and schema constraints up front

