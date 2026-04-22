---
tags: [vz_lupas, oculos, promotion, buying_signal, compre_1_leve_2]
type: pattern
pattern_type: buying_signal_promotion
client: vz_lupas
product_category: oculos
applies_to: [vz_lupas]
related_skills: [CLOSER, SDR]
related_flows: [SDR_ROUTING]
version: 1.0
last_updated: 2026-01-22
---

# Padrão: Sinal de Compra — Compre 1 e Leve 2

## Sinal

Oportunidade de cross-sell:
- Lead quer 1 óculos
- Promoção ativa: Compre 1 e Leve 2
- Lead pode ser convencido a comprar 2

## Intent

buying_signal (com facilitador promocional)

## Contexto

Lead qualificado, mas ainda não mencionou quantidade.
Compre 1 e Leve 2 é campanha ativa (Black Friday estendida).

## Ação

→ CLOSER ou SDR final (sugerir combo, aumentar AOV)

## Tática

1. **Mencionar natural**: "Tá em Compre 1 e Leve 2 agora"
2. **Sugerir**: "Quer pegar mais uma cor? Leva de graça!"
3. **Facilitar decisão**: sugerir 2 cores complementares
4. **Assumir**: "Qual vai ser? Preto e roxa?"

## Exemplo ✓ Correto

```
Lead: "Quero uma Juliet preta"
CLOSER: "Top! E bom saber que tá em Compre 1 e Leve 2.
        Quer pegar uma roxa também? Sai de graça!"

Lead: "Hm, não preciso"
CLOSER: "Entendo! Mas é investimento pra depois, já que sai grátis.
        Juliet roda anos. Qual outra cor você ia escolher?"

Lead: "Ah, talvez marrom..."
CLOSER: "Perfeito! Fica preta + marrom em um preço só.
        Qual seu CEP pra fechar?"
```

## Simulação de Preço Compre 1 e Leve 2

- Juliet R$ 237 × 2 = R$ 237 (leva preta + roxa)
- Radar R$ 189 × 2 = R$ 189 (leva preto + marrom)
- Combo variado: Juliet + Radar = R$ 237

## Erro Comum

```
Lead: "Quero Radar"
SDR: "Tá bom, qual seu CEP?" ← ERRADO (não mencionou promo)
Lead compra 1. AOV perdido.
```

## Correto

```
Lead: "Quero Radar"
SDR: "Top! Tá em Compre 1 e Leve 2. Quer outra cor? Sai de graça!"
→ Lead compra 2 (AOV +100%). ✓
```

## Quando Mencionar

- Sempre que lead escolher 1 produto
- SDR final ou CLOSER inicial
- Natural, sem parecer forçado

## Aplicável a

| Cliente | Categoria | Promoção equivalente |
|---------|-----------|---------------------|
| VZ Lupas | oculos | Compre 1 e Leve 2 |
| [Futuro cliente] | [categoria] | [nome da promoção similar] |

## Notas para Escala

Se outro cliente oferecer promoção do tipo "leve N pague 1":
1. Criar: `06_PATTERNS/buying_signal/[nome_promo_cliente].md`
2. Front-matter com `client: [cliente]` e tags do cliente
3. Referenciar este padrão em `similar_patterns: [compre_1_leve_2]`
4. Adicionar na seção "Aplicável a" acima
5. Atualizar `00_META/TAGS_INDEX.md` com o novo padrão
