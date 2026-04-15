> Project Note: This rule is defined for project `PromptOS`.

When a task requires structured output, return strict JSON only.

Rules:
- No markdown fences
- No prose before or after JSON
- No comments
- No trailing commas
- Match the required schema exactly

Reason:
- The app depends on deterministic parsing and validation.

