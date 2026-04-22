# Erro: Classificação Falha

## Sinal Detectado

CLASSIFIER retorna:
- Intenção errada detectada
- Confidence muito baixa (<0.5)
- Route incoerente com sinal

## Tipo de Erro

`classifier_fail`

## Contexto

Lead enviou mensagem ambígua ou fora do escopo:
- "Oi" (sem contexto)
- "Como você tá?" (social, não comercial)
- Spam ou promoção de outro brand
- Mensagem incompreensível

## Ação

→ ERROR_HANDLING (remediar, tentar novamente, fallback)

## Remediação

1. **Retry**: tentar classificar novamente com mais contexto
2. **Se ainda falhar**: escalar para SDR fallback
3. **Fallback**: "Oi! Qual óculos você curte?" (re-qualificar)

## Exemplo de JSON com Erro

```json
{
  "intent": "other",
  "confidence": 0.3,
  "route": "FAQ"
}
```

## Exemplo de JSON Correto

```json
{
  "intent": "price_inquiry",
  "confidence": 0.92,
  "route": "SDR"
}
```

## Fallback SDR

Se CLASSIFIER falhar 2x:

```
SDR: "Oi! Tudo bem? 😎
     Qual óculos você curte? Temos Juliet, Radar, Gascan..."
```

## Log de Erro

Registrar em `08_LOGS/daily.md`:

```json
{
  "type": "classifier_fail",
  "timestamp": "",
  "input": "",
  "confidence": 0,
  "intent_detected": "other",
  "action_taken": "fallback_SDR",
  "resolution": ""
}
```

## Prevenção

- Sanitizar input antes de enviar ao CLASSIFIER
- Threshold mínimo de confidence: 0.5
- Se abaixo: fallback imediato, sem retry desnecessário
