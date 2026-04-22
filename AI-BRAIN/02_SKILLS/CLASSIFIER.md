---
tags: [skill, classifier, routing, json]
type: skill
applies_to: [all]
related_flows: [SDR_ROUTING]
---

# Skill: CLASSIFIER

## Output Format

```json
{
  "intent": "",
  "confidence": 0,
  "route": ""
}
```

## Rules

- Output JSON only
- No text outside the JSON block
- `confidence` is a number between 0 and 1
- `route` must match a defined flow or skill name
