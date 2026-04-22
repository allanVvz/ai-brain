---
tags: [tock_fatal, moda_feminina, buying_signal, kit_estreia, revendedora]
type: pattern
pattern_type: buying_signal_conversion
client: tock_fatal
product_category: moda_feminina
applies_to: [tock_fatal]
related_skills: [CLOSER, SDR]
related_flows: [SDR_ROUTING]
version: 1.0
last_updated: 2026-04-22
---

# Padrão: Sinal de Compra — Kit de Estreia (Tock Fatal)

## Sinal

Lead demonstra interesse em começar a revender:
- "quero começar a vender moda"
- "como funciona para revender?"
- "tenho que ter CNPJ?"
- "qual o mínimo pra comprar?"
- "nunca revendi, por onde começo?"
- "quanto preciso investir?"

## Intent

buying_signal (iniciante + baixo risco)

## Contexto

Lead está no início do funil — nunca revendeu ou está avaliando fornecedores.
Kit de estreia é o produto de conversão principal para esse perfil.
Diferenciais "sem mínimo" e "sem CNPJ" são os desbloqueadores de objeção.

## Ação

→ CLOSER (apresentar kit de estreia, remover objeções de risco)

## Tática

1. Validar perfil: "você quer revender ou comprar pra uso próprio?"
2. Se revendedora iniciante: reforçar sem mínimo + sem CNPJ
3. Apresentar kit de estreia como primeiro passo
4. Mencionar giro rápido (modal vende o ano todo)
5. Coletar CEP para calcular frete
6. Sugerir próximo passo concreto

## Exemplo ✓ Correto

```
Lead: "Quero começar a vender moda, mas nunca fiz isso"
SDR: "Boa! A gente tem kit de estreia perfeito pra quem tá começando.
     Sem mínimo, sem CNPJ. Você quer revender ou comprar pra você?"

Lead: "Revender"
SDR: "Ótimo! Modal e tricot são os que vendem mais rápido.
     Qual sua cidade pra eu calcular o frete?"

Lead: "Porto Alegre"
CLOSER: "Perfeito! Kit de estreia chega rapidinho em POA.
        Quer que eu monte um kit pra você começar essa semana?"
```

## Objeções Comuns Neste Padrão

| Objeção | Resposta |
|---------|----------|
| "Preciso de CNPJ?" | Não — vendemos sem CNPJ para qualquer pessoa |
| "Qual o mínimo?" | Sem mínimo — compra 1 peça se quiser |
| "E se não vender?" | Modal e tricot têm alto giro — dificilmente encalha |
| "É muito caro?" | Kit de estreia é montado com peças de alto giro e preço acessível |

## Aplicável a

| Cliente | Categoria | Produto equivalente |
|---------|-----------|---------------------|
| Tock Fatal | moda_feminina | Kit de estreia para revendedoras |
| [Futuro cliente de atacado sem mínimo] | [categoria] | [kit equivalente] |

## Notas para Escala

Padrão aplicável a qualquer cliente de atacado que ofereça:
1. Sem mínimo de compra
2. Kit de entrada para novos revendedores
3. Produto de alto giro como isca inicial
