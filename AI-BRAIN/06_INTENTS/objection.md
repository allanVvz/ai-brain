---
tags: [intent, objection, routing, generic]
type: intent
applies_to: [all]
related_skills: [CLOSER]
related_flows: [SDR_ROUTING]
related_patterns: [objection_price_high, objection_shipping_slow, objection_no_warranty, objection_no_need]
---

# Intent: Objeção

## Descrição

Lead coloca uma objeção — preço alto, frete, qualidade, prazo.

## Sinais

- "tá caro"
- "demora muito pra chegar"
- "tem garantia?"
- "achei mais barato em outro lugar"
- "não sei se vale"

## Ação

- Roteado para: `CLOSER`
- Identificar tipo de objeção via padrão em `06_PATTERNS/objection/`
- Não reclassificar dentro do CLOSER

## Output esperado do CLASSIFIER

```json
{
  "intent": "objection",
  "confidence": 0.9,
  "route": "CLOSER"
}
```
