# Erro: Timeout no Classifier

## Descrição

O CLASSIFIER não respondeu dentro do tempo limite esperado.

## Causa Comum

- Latência elevada na API
- Mensagem muito longa enviada ao CLASSIFIER
- Sobrecarga no fluxo n8n

## Ação Correta

1. Registrar o timeout no log diário
2. Retentar uma vez com a mesma mensagem
3. Se falhar novamente, usar fallback e notificar operador

## Fallback JSON

```json
{
  "intent": "unknown",
  "confidence": 0,
  "route": "SDR"
}
```
