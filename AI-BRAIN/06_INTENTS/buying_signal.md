---
tags: [intent, buying_signal, routing, generic]
type: intent
applies_to: [all]
related_skills: [CLOSER]
related_flows: [SDR_ROUTING]
related_patterns: [compre_1_leve_2, visao_circular_tradein]
---

# Intent: Sinal de Compra

## Descrição

Lead demonstra urgência, interesse concreto ou intenção de fechar.

## Sinais

- "quero comprar"
- "como faço o pedido?"
- "aceita pix?"
- "preciso pra essa semana"
- "pode mandar o link"
- "fechado, como pago?"

## Ação

- Roteado para: `CLOSER`
- Não qualificar novamente — lead já está pronto
- Empurrar direto para fechamento

## Output esperado do CLASSIFIER

```json
{
  "intent": "buying_signal",
  "confidence": 0.95,
  "route": "CLOSER"
}
```
