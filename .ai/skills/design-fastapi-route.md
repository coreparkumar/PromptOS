# Skill: Design FastAPI Route

> Project Note: This skill is defined for project `PromptOS`.

## Purpose
Design a FastAPI route that fits the app's backend patterns for generation, formatting, and service workflows.

## Input
- route_purpose
- method
- request_schema
- response_schema
- backend_dependencies

## Output
- A concise implementation plan in markdown
- Shape:
  - endpoint
  - request model
  - response model
  - validation logic
  - service layer call
  - error handling

## Rules
- Keep request validation in schemas.
- Keep orchestration in service modules, not route bodies.
- Use predictable response shapes.
- Surface backend and model failures clearly.
- Do not couple routes directly to frontend-specific formatting.

## Behavior
- Favor thin routes and reusable service logic.
- Call out validation, storage, and model boundaries.
- Reflect existing FastAPI conventions in this project.

## Example Use
- Route purpose: generate raw structured content
- Method: POST
- Backend dependencies: prompt builder, Ollama service, export service

