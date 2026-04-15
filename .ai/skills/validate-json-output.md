# Skill: Validate JSON Output

> Project Note: This skill is defined for project `PromptOS`.

## Purpose
Check whether an AI response is safe for programmatic parsing and conforms to the required schema.

## Input
- raw_response
- required_schema
- required_fields
- forbidden_fields

## Output
- Strict JSON only
- Shape:
```json
{
  "valid": true,
  "errors": [],
  "normalized_response": {}
}
```

## Rules
- Return JSON only.
- Mark `valid` as `false` if parsing would fail.
- Report missing fields explicitly in `errors`.
- Report extra forbidden fields explicitly in `errors`.
- Do not silently discard invalid structure without reporting it.
- Preserve values when they are valid.

## Behavior
- Attempt structural normalization when safe.
- Keep validation feedback precise and compact.
- Prefer deterministic repair suggestions over vague advice.

## Example Use
- Raw response: model output from content generation
- Required fields: hook, body, cta, hashtags
- Forbidden fields: explanation, notes

