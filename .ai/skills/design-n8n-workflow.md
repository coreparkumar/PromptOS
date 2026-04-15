# Skill: Design n8n Workflow

> Project Note: This skill is defined for project `PromptOS`.

## Purpose
Design or review an n8n workflow that fits PromptOS patterns for automation, structured data handling, and safe backend integration.

## Input
- workflow_goal
- trigger_type
- input_data
- processing_steps
- output_shape
- integration_constraints

## Output
- A concise workflow design spec in markdown
- Shape:
  - workflow summary
  - trigger and entry conditions
  - node-by-node flow
  - data transformations
  - error handling
  - output contract

## Rules
- Keep each node focused on one clear responsibility.
- Prefer explicit data mappings over implicit passthrough behavior.
- Validate inputs before calling external services.
- Keep secrets and credentials in n8n credential storage, never inline in prompts.
- Use structured JSON when downstream parsing or storage is required.
- Call out retries, fallback paths, and failure states explicitly.
- Do not bypass PromptOS backend constraints when the workflow touches AI generation.

## Behavior
- Favor simple, auditable workflow chains over overly clever branching.
- Make triggers, dependencies, and outputs easy to inspect.
- Highlight where validation, transformation, and side effects occur.
- Align workflow steps with PromptOS expectations for structured outputs and safe integrations.

## Example Use
- Workflow goal: automate post generation and approval handoff
- Trigger type: webhook
- Processing steps: validate payload, call backend generation endpoint, format output, send review notification
- Output shape: approved content payload and delivery status
