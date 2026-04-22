---
tags: [intent, product_inquiry, routing, generic]
type: intent
applies_to: [all]
related_skills: [SDR]
related_flows: [SDR_ROUTING]
related_patterns: [product_doubt, product_material, product_color_ask, product_comparison]
---

# Intent: Consulta de Produto

## Descrição

Lead quer saber sobre um produto específico — características, modelos, disponibilidade.

## Sinais

- "como é o Juliet?"
- "qual a diferença entre os modelos?"
- "tem o Gascan?"
- "me fala sobre o Radar"

## Ação

- Roteado para: `SDR`
- Extrair produto mencionado via `EXTRACTOR`
- Responder com características do produto via `05_ENTITIES/VZ_LUPAS`

## Output esperado do CLASSIFIER

```json
{
  "intent": "product_inquiry",
  "confidence": 0.85,
  "route": "SDR"
}
```
