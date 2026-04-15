# PromptOS Architecture

> Project Note: This context is defined for project `PromptOS`.

PromptOS follows this runtime flow:

Electron Renderer
-> Preload Bridge
-> IPC
-> Electron Main
-> FastAPI Backend
-> Ollama

## Core Rules
- No direct renderer-to-Ollama calls
- No unrestricted renderer access to Node APIs
- Use preload as the capability boundary
- Keep backend orchestration separate from UI formatting
- Prefer structured model outputs when the app needs parsing

## Design Intent
- Local-first AI workflow
- Secure Electron boundaries
- Backend-owned LLM execution
- Repeatable content generation and formatting flows

