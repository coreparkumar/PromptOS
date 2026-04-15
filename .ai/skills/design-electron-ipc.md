# Skill: Design Electron IPC

> Project Note: This skill is defined for project `PromptOS`.

## Purpose
Design secure IPC contracts between renderer and main process for PromptOS.

## Input
- feature_name
- renderer_action
- payload_shape
- expected_response
- security_constraints

## Output
- A concise IPC design spec in markdown
- Shape:
  - channel name
  - request payload
  - response payload
  - validation rules
  - preload exposure
  - main-process handler notes

## Rules
- Never allow direct renderer access to Node APIs.
- Expose functionality through preload only.
- Use explicit channel names.
- Validate all incoming payload fields in main process.
- Do not design wildcard or pass-through channels.
- Do not route renderer requests directly to Ollama.

## Behavior
- Prefer narrow, purpose-built IPC handlers.
- Keep payloads small and typed.
- Surface failure states explicitly.
- Align with the app's preload-first architecture.

## Example Use
- Feature name: export final post
- Renderer action: save a generated post as PDF
- Expected response: success flag and saved file path

