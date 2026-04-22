# Erro: JSON Inválido

## Descrição

O CLASSIFIER retornou um JSON malformado ou a mensagem do lead continha caracteres que quebraram o parse.

## Causa Comum

- Aspas dentro da mensagem do lead não escapadas
- Caracteres especiais: `"`, `\`, emojis em campos JSON
- Resposta do LLM com texto fora do bloco JSON

## Ação Correta

1. Sanitizar a mensagem do lead antes de enviar ao CLASSIFIER
2. Remover ou escapar caracteres problemáticos
3. Se o JSON retornado for inválido, retentar com fallback de intent `unknown`

## Fallback JSON

```json
{
  "intent": "unknown",
  "confidence": 0,
  "route": "SDR"
}
```
