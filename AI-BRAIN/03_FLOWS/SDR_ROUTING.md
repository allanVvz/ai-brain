---
tags: [flow, sdr, routing, whatsapp]
type: flow
applies_to: [all]
related_skills: [SDR, CLOSER, CLASSIFIER, EXTRACTOR]
---

# Flow: SDR Routing

## Context

WhatsApp lead handling flow.

## Steps

1. **CLASSIFIER** — detect intent and assign route
2. **ROUTER** — send message to correct skill based on route
3. **SDR** — engage lead, qualify, suggest next step

## Rules

- Never skip CEP collection before quoting
- Always end message with a next step suggestion
- Route only to defined skills

## Known Errors

- JSON string issue: special characters in message break JSON parse — sanitize input before classification
