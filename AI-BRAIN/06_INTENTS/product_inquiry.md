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
