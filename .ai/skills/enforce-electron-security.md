# Skill: Enforce Electron Security

> Project Note: This skill is defined for project `PromptOS`.

## Purpose
Review or generate Electron code that follows the security model used in this project.

## Input
- file_or_feature
- proposed_code_or_task
- threat_surface

## Output
- A short security review or implementation checklist in markdown
- Shape:
  - risks
  - required changes
  - approved patterns
  - rejected patterns

## Rules
- Keep `contextIsolation` enabled.
- Keep `sandbox` enabled where possible.
- Deny unnecessary permission requests.
- Block unsafe navigation and window opening.
- Never use `innerHTML` with user-controlled content.
- Never expose unrestricted IPC or shell access to renderer code.

## Behavior
- Identify concrete Electron risks first.
- Prefer safe built-in patterns over convenience shortcuts.
- Map every recommendation to this project's architecture.

## Example Use
- File or feature: renderer export workflow
- Threat surface: user input rendering and file access

