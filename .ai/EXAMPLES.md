# Prompt Examples

> Project Note: These examples are defined for project `PromptOS`.

Copy-paste examples for using the `.ai/` system in a simple, user-friendly way.

## 1. Generate a LinkedIn Post

```text
Use:
.ai/skills/generate-structured-content.md
.ai/rules/json-only.md
.ai/context/goals.md

Task:
Generate a LinkedIn post about local-first AI tools for startup founders.

Input:
- Topic: Why local-first AI tools matter
- Audience: Startup founders
- Tone: Practical and thoughtful
- Word count target: 220
```

## 2. Format a Draft for Social Media

```text
Use:
.ai/skills/format-social-post.md
.ai/rules/json-only.md
.ai/context/goals.md

Task:
Format this rough draft into a polished LinkedIn post.

Input:
- Platform: LinkedIn
- Tone: Clear and confident
- Source text: <paste draft here>
```

## 3. Validate Model Output

```text
Use:
.ai/skills/validate-json-output.md
.ai/rules/json-only.md

Task:
Check whether this model response is valid for the app.

Input:
- Required fields: hook, body, cta, hashtags
- Forbidden fields: explanation, notes
- Raw response: <paste model output here>
```

## 4. Design a New IPC Flow

```text
Use:
.ai/skills/design-electron-ipc.md
.ai/rules/ipc-whitelist.md
.ai/rules/no-direct-ollama-from-renderer.md
.ai/context/architecture.md

Task:
Design a secure IPC flow for saving exported content as DOCX.
```

## 5. Design a FastAPI Route

```text
Use:
.ai/skills/design-fastapi-route.md
.ai/context/architecture.md
.ai/context/stack.md

Task:
Design a FastAPI route for generating structured raw content.

Requirements:
- Validate request payload
- Call service layer
- Return predictable response shape
```

## 6. Review an Electron Feature for Security

```text
Use:
.ai/skills/enforce-electron-security.md
.ai/rules/no-innerhtml.md
.ai/rules/ipc-whitelist.md
.ai/context/architecture.md

Task:
Review this renderer feature for security risks.

Input:
- File: electron/main.js
- Feature: export and save flow
```

## 7. Plan Ollama Backend Orchestration

```text
Use:
.ai/skills/orchestrate-ollama-backend.md
.ai/rules/json-only.md
.ai/context/architecture.md

Task:
Design the backend-side Ollama orchestration for structured content generation.

Input:
- Model: storyteller
- Output schema: hook, body, cta, hashtags
```

## 8. Use the Full PromptOS Pipeline

```text
Use:
.ai/skills/promptos-pipeline.md
.ai/context/architecture.md
.ai/context/goals.md

Task:
Design the full workflow for generating a LinkedIn post, reviewing it in the UI, formatting it, and exporting it as PDF.
```

## 9. Use Multiple Skills Together

```text
Use:
.ai/skills/promptos-pipeline.md
.ai/skills/generate-structured-content.md
.ai/skills/validate-json-output.md
.ai/skills/design-electron-ipc.md
.ai/rules/json-only.md
.ai/context/architecture.md

Task:
Implement a safe end-to-end generation flow with structured output and renderer-safe delivery.
```

## 10. Use a Template for a Larger Task

```text
Use:
.ai/templates/full-pipeline-task.md
.ai/skills/promptos-pipeline.md
.ai/skills/design-fastapi-route.md
.ai/skills/design-electron-ipc.md
.ai/rules/no-direct-ollama-from-renderer.md
.ai/context/architecture.md

Task:
Plan a new end-to-end workflow for generating platform-specific content and exporting it from the desktop app.
```

## Friendly Prompt Pattern

You do not always need to reference many files.

For smaller tasks, this is enough:

```text
Use the PromptOS pipeline skill, the JSON-only rule, and the architecture context.

Task:
Help me design the content generation flow for LinkedIn output.
```

For larger tasks, use the explicit file list:

```text
Use:
.ai/skills/promptos-pipeline.md
.ai/skills/design-fastapi-route.md
.ai/skills/design-electron-ipc.md
.ai/rules/json-only.md
.ai/rules/no-direct-ollama-from-renderer.md
.ai/context/architecture.md

Task:
Implement the full generation-to-export workflow for the app.
```

