# Skill: Format Social Post

> Project Note: This skill is defined for project `PromptOS`.

## Purpose
Transform raw or edited draft text into a platform-specific final post while preserving the main message.

## Input
- source_text
- platform
- tone
- audience
- output_style

## Output
- Strict JSON only
- Shape:
```json
{
  "title": "",
  "formatted_text": "",
  "hashtags": []
}
```

## Rules
- Return JSON only.
- Do not change the core claim unless explicitly asked.
- Respect the platform's expected cadence and formatting.
- Keep paragraphs short for social readability.
- Avoid markdown headings unless the platform calls for them.
- Hashtags must be relevant and not spammy.

## Behavior
- Preserve the author intent.
- Improve readability, rhythm, and scannability.
- Adjust line breaks and emphasis for the target platform.
- Favor clean formatting over clever formatting.

## Example Use
- Source text: A rough draft about local-first AI workflows
- Platform: LinkedIn
- Tone: Thoughtful
- Output style: High-clarity social post

