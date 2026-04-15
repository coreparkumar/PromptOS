> Project Note: This rule is defined for project `PromptOS`.

IPC must be explicit and narrow.

Rules:
- Only expose approved methods through preload.
- Do not expose raw `ipcRenderer`.
- Do not design generic pass-through channels.
- Validate payloads in main process before acting on them.
- Keep request and response shapes stable.

Reason:
- Reduces privilege leakage between renderer and main.
- Makes the app easier to audit and maintain.

