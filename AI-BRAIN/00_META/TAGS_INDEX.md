---
tags: [meta, index, tags, relationships]
type: meta
applies_to: [all]
---

# Índice de Tags e Relacionamentos

## Por Cliente

### tock_fatal

- **Categoria de produto**: moda_feminina
- **Entidade**: `05_ENTITIES/CLIENTS/TOCK_FATAL/`
- **Índice**: `05_ENTITIES/CLIENTS/TOCK_FATAL/index.md`

| Tipo | Arquivos |
|------|---------|
| Entidade | brand.md, briefing.md, tone.md, audience.md |
| Competidores | competitors/zafira.md, competitors/supervaidosa.md, competitors/nina_luxo.md (draft) |
| Padrões exclusivos | kit_estreia_tock_fatal |
| Prompts | SDR/tock_fatal.md, CLOSER/tock_fatal.md |
| Skills | SDR, CLOSER, CLASSIFIER, EXTRACTOR |
| Flows | SDR_ROUTING |

---

### vz_lupas

- **Categoria de produto**: oculos
- **Entidade**: `05_ENTITIES/CLIENTS/VZ_LUPAS/`
- **Índice**: `05_ENTITIES/CLIENTS/VZ_LUPAS/index.md`

| Tipo | Arquivos |
|------|---------|
| Entidade | brand.md, briefing.md, products.md, tone.md |
| Padrões exclusivos | compre_1_leve_2, visao_circular_tradein, product_comparison |
| Prompts | SDR/vz_lupas.md, CLOSER/vz_lupas.md |
| Skills | SDR, CLOSER, CLASSIFIER, EXTRACTOR |
| Flows | SDR_ROUTING |

---

## Por Categoria de Produto

### oculos

- **Clientes**: vz_lupas, [futuros clientes]
- **Padrões relevantes**: compre_1_leve_2, visao_circular_tradein, product_comparison
- **Notas**: Promoções tipo "Compre 1 Leve 2" são comuns nesta categoria

---

## Por Tipo de Padrão

### buying_signal_conversion

| Padrão | Cliente | Arquivo |
|--------|---------|---------|
| kit_estreia_tock_fatal | tock_fatal | `06_PATTERNS/buying_signal/kit_estreia_tock_fatal.md` |

### buying_signal_promotion

| Padrão | Cliente | Arquivo |
|--------|---------|---------|
| compre_1_leve_2 | vz_lupas | `06_PATTERNS/buying_signal/compre_1_leve_2.md` |

### buying_signal_trade_in

| Padrão | Cliente | Arquivo |
|--------|---------|---------|
| visao_circular_tradein | vz_lupas | `06_PATTERNS/buying_signal/visao_circular_tradein.md` |

### price_inquiry (genérico)

| Padrão | Aplica a | Arquivo |
|--------|----------|---------|
| price_before_product | all | `06_PATTERNS/price_inquiry/price_before_product.md` |
| price_by_installment | all | `06_PATTERNS/price_inquiry/price_by_installment.md` |
| price_vs_competitor | all | `06_PATTERNS/price_inquiry/price_vs_competitor.md` |

### product_inquiry

| Padrão | Aplica a | Arquivo |
|--------|----------|---------|
| product_doubt | all | `06_PATTERNS/product_inquiry/product_doubt.md` |
| product_material | all | `06_PATTERNS/product_inquiry/product_material.md` |
| product_color_ask | all | `06_PATTERNS/product_inquiry/product_color_ask.md` |
| product_comparison | vz_lupas | `06_PATTERNS/product_inquiry/product_comparison.md` |

### objection (genérico)

| Padrão | Aplica a | Arquivo |
|--------|----------|---------|
| objection_price_high | all | `06_PATTERNS/objection/objection_price_high.md` |
| objection_shipping_slow | all | `06_PATTERNS/objection/objection_shipping_slow.md` |
| objection_no_warranty | all | `06_PATTERNS/objection/objection_no_warranty.md` |
| objection_no_need | all | `06_PATTERNS/objection/objection_no_need.md` |

### error (genérico)

| Padrão | Aplica a | Arquivo |
|--------|----------|---------|
| json_parsing_error | all | `06_PATTERNS/errors/json_parsing_error.md` |
| classifier_timeout | all | `06_PATTERNS/errors/classifier_timeout.md` |
| missing_cep | all | `06_PATTERNS/errors/missing_cep.md` |
| error_classifier_fail | all | `06_PATTERNS/errors/error_classifier_fail.md` |

---

## Por Skill

### SDR
- Flows: SDR_ROUTING
- Padrões: price_before_product, price_by_installment, product_doubt, product_material, product_color_ask, product_comparison, missing_cep
- Prompts: SDR/vz_lupas.md, SDR/template.md

### CLOSER
- Flows: SDR_ROUTING
- Padrões: compre_1_leve_2, visao_circular_tradein, objection_price_high, objection_shipping_slow, objection_no_warranty, objection_no_need, price_vs_competitor
- Prompts: CLOSER/vz_lupas.md, CLOSER/template.md

### CLASSIFIER
- Flows: SDR_ROUTING
- Padrões (errors): json_parsing_error, classifier_timeout, error_classifier_fail
- Intents: buying_signal, objection, product_inquiry

### EXTRACTOR
- Padrões (errors): json_parsing_error, missing_cep

---

## Como Escalar para Novo Cliente

Para adicionar um novo cliente (ex: `cliente_x` com categoria `moda`):

1. Criar pasta: `05_ENTITIES/CLIENTS/CLIENTE_X/`
2. Criar arquivos: `brand.md`, `briefing.md`, `products.md`, `tone.md`, `index.md`
3. Front-matter em cada arquivo:
```yaml
client: cliente_x
product_category: moda
applies_to: [cliente_x]
```
4. Se tiver padrões exclusivos → criar em `06_PATTERNS/[tipo]/[nome_cliente_x].md`
5. Criar prompts em `07_PROMPTS/SDR/cliente_x.md` e `07_PROMPTS/CLOSER/cliente_x.md`
6. Atualizar este índice com o novo cliente
