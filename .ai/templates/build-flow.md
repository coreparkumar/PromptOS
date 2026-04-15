# Template: Build Flow

> Project Note: This template is defined for project `PromptOS`.

Use:
- `.ai/context/architecture.md`
- `.ai/context/stack.md`
- Relevant skill files from `.ai/skills/`
- Relevant constraints from `.ai/rules/`

Task:
Implement the following feature for PromptOS.

Feature:
- <describe feature>

Requirements:
- <functional requirement 1>
- <functional requirement 2>
- <functional requirement 3>

Constraints:
- Follow the Electron -> preload -> IPC -> FastAPI -> Ollama architecture.
- Keep renderer code free from direct backend-runtime access.
- Use strict JSON outputs if the feature depends on AI generation.
- Keep security-sensitive logic explicit.

Deliver:
- implementation plan
- affected files
- request/response shapes
- validation notes
- security notes

