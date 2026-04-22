# Erro: CEP Ausente

## Descrição

O fluxo tentou calcular frete ou confirmar entrega sem ter o CEP do lead.

## Causa Comum

- SDR pulou a etapa de coleta de CEP
- EXTRACTOR não encontrou CEP na conversa
- Lead não forneceu o CEP após ser solicitado

## Ação Correta

1. Nunca avançar para cotação de frete sem CEP
2. Se CEP ausente, retornar ao SDR para solicitar
3. Solicitar CEP de forma direta: "Me passa seu CEP pra eu calcular o frete?"

## Regra

- CEP é obrigatório antes de qualquer cotação
- Bloquear o fluxo se CEP não estiver presente
