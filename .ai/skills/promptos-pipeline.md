# Skill: PromptOS Pipeline

> Project Note: This skill is defined for project `PromptOS`.

## Purpose
Coordinate the full PromptOS workflow from task intake through skill selection, rule attachment, context grounding, execution, and output validation.

## Input
- task_goal
- selected_skills
- selected_rules
- selected_context
- expected_output
- validation_needs

## Output
- A structured workflow plan in markdown
- Shape:
  - task summary
  - skill selection
  - rule selection
  - context grounding
  - execution flow
  - validation points
  - reuse notes

## Rules
- Follow the workflow: intake -> choose skills -> attach rules -> attach context -> execute -> validate.
- Keep each skill narrowly scoped.
- Prefer structured outputs when reuse or parsing matters.
- Make validation explicit when output will be reused programmatically.
- Preserve user intent through the full workflow.
- Keep project-specific notes visible so the skillset stays portable.

## Behavior
- Break larger tasks into reusable prompt modules.
- Show why each skill, rule, and context file is being used.
- Keep the flow understandable for day-to-day prompting, not just expert use.
- Prefer repeatable prompt patterns over one-off complex instructions.

## Example Use
- Task goal: Create a reusable founder-style content generation workflow
- Selected skills: generate structured content, validate JSON output
- Selected rules: JSON-only, prompt-usage
- Selected context: goals, stack
- Expected output: repeatable prompt pattern and structured content
