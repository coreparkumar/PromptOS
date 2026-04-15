# Init Master Prompt

> Project Note: This master prompt is defined for project `PromptOS`.

Use this file at the start of a new transformation task when a project must be updated to match new requirements.

## Purpose
Turn a vague or evolving request into a structured PromptOS workflow that selects the right skills, rules, context, and deliverables before implementation begins.

## How To Use
Attach this file first, then attach:
- the most relevant files from `.ai/context/`
- one or more focused skills from `.ai/skills/`
- the required constraints from `.ai/rules/`
- a template from `.ai/templates/` when the task is multi-stage

## Master Prompt

You are operating inside `PromptOS`.

Your job is to transform an existing project according to new requirements in a structured, reusable, and implementation-aware way.

Follow this workflow exactly:

1. Understand the project
- summarize the current system or feature briefly
- identify what is already present
- identify what must change
- identify what can be reused

2. Understand the new requirements
- rewrite the requirements into a clear and implementation-friendly form
- separate functional requirements from constraints
- identify missing assumptions
- avoid vague interpretation when a concrete structure can be proposed

3. Select the PromptOS modules
- choose the most relevant skills
- choose the required rules
- choose the smallest useful set of context files
- choose a template if the task is multi-step
- explain the selection briefly

4. Produce a transformation plan
- current state
- target state
- files or areas likely to change
- risks
- validation points
- suggested implementation order

5. Produce the execution prompt
- create a clean, copy-paste-ready prompt that uses the selected PromptOS files
- keep it specific to the transformation task
- define expected output clearly

6. Keep outputs disciplined
- prefer structured outputs when parsing, validation, or reuse matters
- preserve security boundaries
- do not propose open-ended rewrites without scoping them
- break large changes into stages when needed

## Expected Output Shape
- Project summary
- Requirement breakdown
- Selected PromptOS files
- Transformation plan
- Execution prompt
- Risks and validation notes

## Example Invocation

Task:
Transform this project based on new requirements for architecture, workflow, and output structure.

Requirements:
- make the AI workflow reusable
- preserve secure boundaries
- add structured output handling
- improve portability across projects

Expected output:
- transformation plan
- selected PromptOS modules
- a final execution prompt ready to use

## Recommended Pairings
- for architecture changes: `design-electron-ipc.md`, `design-fastapi-route.md`, `enforce-electron-security.md`
- for workflow changes: `promptos-pipeline.md`, `full-pipeline-task.md`
- for content/output changes: `generate-structured-content.md`, `format-social-post.md`, `validate-json-output.md`
- for strict machine-safe responses: `json-only.md`
