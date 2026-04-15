# AI Prompt Operating System

> Project Note: This skillset is defined for project `PromptOS`.

This folder is the reusable AI workflow layer for `PromptOS`.

It helps turn one-off prompting into a repeatable system built around:

- skills
- rules
- context
- templates

## Folder Structure

```text
.ai/
  context/
  rules/
  skills/
  templates/
```

## What Each Folder Does

### `skills/`
Atomic AI capabilities.

Use a skill when you want the model to perform one focused job such as:
- generating structured content
- formatting a social post
- designing Electron IPC
- designing a FastAPI route
- enforcing Electron security

### `rules/`
Non-negotiable constraints.

Use rules to prevent unsafe or inconsistent outputs.

Examples:
- no `innerHTML`
- JSON-only output
- explicit IPC boundaries
- no direct renderer-to-Ollama calls

### `context/`
Project awareness.

Use context files to remind the model how this app is built and what matters most.

Examples:
- architecture
- stack
- goals

### `templates/`
Reusable higher-level prompt flows.

Use a template when a task needs multiple skills and constraints combined in one repeatable pattern.

Examples:
- building a backend feature
- generating a LinkedIn post
- implementing a secure Electron feature

## Recommended Workflow

Before asking AI to do anything:

1. Pick the relevant skill from `.ai/skills/`
2. Add the necessary constraints from `.ai/rules/`
3. Add project context from `.ai/context/`
4. Use a template from `.ai/templates/` if the task is larger
5. Write a concrete task with a clear output

## Simple Usage Pattern

Example:

```text
Use:
.ai/skills/generate-structured-content.md
.ai/rules/json-only.md
.ai/context/goals.md

Task:
Generate a LinkedIn post about local-first AI workflows for founders.
```

## Development Usage Pattern

Example:

```text
Use:
.ai/skills/design-electron-ipc.md
.ai/skills/enforce-electron-security.md
.ai/rules/ipc-whitelist.md
.ai/rules/no-direct-ollama-from-renderer.md
.ai/context/architecture.md

Task:
Design a safe IPC flow for exporting generated content as PDF.
```

## VS Code Snippets

Snippets are available in:

- `.vscode/snippets.code-snippets`

Useful prefixes:
- `ai-skill`
- `ai-rule`
- `ai-context`
- `ai-template`
- `ai-json`

## Why This Exists

This system is designed to help the project move from:

- ad hoc prompts

to:

- reusable AI skills with explicit boundaries

That makes AI outputs:

- more consistent
- easier to validate
- easier to reuse
- safer for this Electron + FastAPI + Ollama architecture

