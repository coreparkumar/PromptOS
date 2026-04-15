# Template: Full Pipeline Task

> Project Note: This template is defined for project `PromptOS`.

Use:
- `.ai/skills/promptos-pipeline.md`
- `.ai/context/architecture.md`
- `.ai/context/goals.md`
- relevant supporting skills from `.ai/skills/`
- relevant constraints from `.ai/rules/`

Task:
Implement, review, or improve a full PromptOS workflow.

Workflow Goal:
- <describe the end-to-end workflow objective>

Input:
- Topic: <topic>
- Audience: <audience>
- Platform: <platform>
- Tone: <tone>
- Model: <model>
- Output format: <output format>
- Export target: <export target>

Requirements:
- keep the full flow aligned with intake -> generate raw -> review/edit -> format -> export
- preserve Electron security boundaries
- keep model calls on the backend
- use structured outputs where parsing is required
- make validation and failure handling explicit

Deliver:
- workflow plan
- stage-by-stage ownership
- request and response shapes
- IPC and backend touchpoints
- validation points
- failure states
- implementation notes

Optional Supporting Skills:
- `.ai/skills/generate-structured-content.md`
- `.ai/skills/format-social-post.md`
- `.ai/skills/validate-json-output.md`
- `.ai/skills/design-electron-ipc.md`
- `.ai/skills/design-fastapi-route.md`
- `.ai/skills/enforce-electron-security.md`
- `.ai/skills/orchestrate-ollama-backend.md`

