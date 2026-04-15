> Project Note: This rule is defined for project `PromptOS`.

Never call Ollama directly from the renderer.

Required flow:
- Renderer
- Preload
- IPC
- FastAPI backend
- Ollama

Reason:
- Preserves security boundaries.
- Centralizes validation, logging, and timeout handling.
- Prevents renderer code from becoming a direct model client.

