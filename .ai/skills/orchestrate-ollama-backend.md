# Skill: Orchestrate Ollama Backend Calls

> Project Note: This skill is defined for project `PromptOS`.

## Purpose
Design or review backend-side LLM calling logic for Ollama in a way that is structured, observable, and safe for the app.

## Input
- task_name
- model_name
- prompt_goal
- input_data
- expected_output_schema

## Output
- A backend orchestration plan in markdown
- Shape:
  - prompt strategy
  - request payload
  - timeout expectations
  - parsing strategy
  - storage/logging expectations
  - failure handling

## Rules
- All LLM calls must originate from the backend.
- Favor structured outputs when downstream parsing is required.
- Record enough context for debugging failed generations.
- Keep prompt instructions aligned with JSON-safe outputs.
- Do not let renderer-defined prompts bypass backend constraints.

## Behavior
- Separate prompt construction from transport logic.
- Prefer deterministic schema-driven generation patterns.
- Include retry and timeout considerations when useful.
- Align with local-first model execution through Ollama.

## Example Use
- Task name: generate raw LinkedIn content
- Model name: storyteller
- Expected output schema: hook, body, cta, hashtags

