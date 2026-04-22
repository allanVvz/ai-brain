---
tags: [pattern, product_inquiry, comparison, vz_lupas, oculos]
type: pattern
pattern_type: product_inquiry
client: vz_lupas
product_category: oculos
applies_to: [vz_lupas]
related_skills: [SDR]
related_flows: [SDR_ROUTING]
---

# Padrão: Comparação Entre Produtos

## Sinal

Lead compara produtos:
- "Qual a diferença entre Juliet e Radar?"
- "Qual é melhor, Gascan ou Radar?"
- "Qual dura mais?"
- "Qual é mais confortável?"

## Intent

product_inquiry

## Contexto

Lead está qualificando, não quer escolher errado.
Resposta certa converte; resposta errada perde.

## Ação

→ SDR (descrever diferenças + sugerir baseado em estilo)

## Tática

1. **NÃO** comparar preço (ainda não é hora)
2. Comparar: **estilo + uso**
3. Fazer 1 pergunta: qual estilo o lead curte
4. Sugerir baseado na resposta
5. Próximo passo: cores + CEP

## Comparações Comuns

### Juliet vs Radar

```
Lead: "Qual a diferença entre Juliet e Radar?"
SDR: "Juliet é clássica, ótima pra lifestyle casual.
     Radar é mais esportiva, leve, pra atividades.
     Você curte mais casual ou atividade?"

Lead: "Casual"
SDR: "Então Juliet bate! Que cor você prefere?"
```

### Gascan vs Juliet

```
Lead: "Gascan ou Juliet?"
SDR: "Depende do seu estilo! Gascan é oversized, statement, muito Instagram.
     Juliet é clássica, roda em qualquer lugar.
     Qual é mais você?"
```

### Durabilidade/Conforto

```
Lead: "Qual é mais durável?"
SDR: "Todas duram anos! A diferença é estilo mesmo.
     Qual você acha mais seu: casual, esportivo ou statement?"
```

## Erro Comum

```
Lead: "Qual é melhor?"
SDR: "Radar é mais caro, Juliet é mais barata" ← ERRADO
```

## Correto

```
Lead: "Qual é melhor?"
SDR: "Melhor depende do seu estilo!
     Você curte mais casual ou esportivo?" ← CERTO

Lead: "Casual"
SDR: "Então Juliet! Que cor?"
```
