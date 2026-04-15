# Skill: Generate Structured Content

> Project Note: This skill is defined for project `PromptOS`.

## Purpose
Generate platform-aware social content in a strict machine-readable structure so the app can safely parse and render it.

## Input
- topic
- platform
- tone
- audience
- context
- word_count_target
- model_hint

## Output
- Strict JSON only
- Shape:
```json
{
  "hook": "",
  "body": "",
  "cta": "",
  "hashtags": []
}
```

## Rules
- Return valid JSON only.
- Do not wrap JSON in markdown fences.
- Do not include commentary, notes, or explanations.
- Keep platform voice aligned to the requested platform.
- Keep the body close to the requested word count target.
- Hashtags must be a JSON array of strings.
- Never invent unsupported app fields.

## Behavior
- Start with a strong opening hook.
- Write a clear, readable body with one main narrative arc.
- End with a practical CTA.
- Keep the output easy for downstream formatting.

## Example Use
- Topic: AI productivity for founders
- Platform: LinkedIn
- Tone: Practical and confident
- Audience: Startup founders
- Word count target: 220

