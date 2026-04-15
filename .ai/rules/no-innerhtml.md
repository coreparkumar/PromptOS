> Project Note: This rule is defined for project `PromptOS`.

Never use `innerHTML` with user input or model output.

Always prefer:
- `textContent`
- `createElement`
- explicit DOM node construction

Reason:
- Prevents DOM XSS in Electron renderer code.
- Keeps rendering behavior predictable for AI-generated content.

