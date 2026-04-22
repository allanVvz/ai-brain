# MANIFEST - Todos os Arquivos

Use este arquivo para confirmar que você tem TODOS os arquivos após clonar do GitHub.

## Checklist Completo

### 00_META
- [ ] README.md

### 01_RULES
- [ ] global.md
- [ ] output.md

### 02_SKILLS
- [ ] SDR.md
- [ ] CLOSER.md
- [ ] CLASSIFIER.md
- [ ] EXTRACTOR.md

### 03_FLOWS
- [ ] SDR_ROUTING.md

### 04_MEMORY
- [ ] patterns.md

### 05_ENTITIES/CLIENTS/VZ_LUPAS
- [ ] brand.md
- [ ] briefing.md
- [ ] products.md
- [ ] tone.md

### 06_INTENTS
- [ ] product_inquiry.md
- [ ] objection.md
- [ ] buying_signal.md

### 06_PATTERNS/price_inquiry
- [ ] price_before_product.md
- [ ] price_by_installment.md
- [ ] price_vs_competitor.md

### 06_PATTERNS/product_inquiry
- [ ] product_doubt.md
- [ ] product_material.md
- [ ] product_color_ask.md
- [ ] product_comparison.md

### 06_PATTERNS/objection
- [ ] objection_price_high.md
- [ ] objection_shipping_slow.md
- [ ] objection_no_warranty.md
- [ ] objection_no_need.md

### 06_PATTERNS/buying_signal
- [ ] visao_circular_tradein.md
- [ ] compre_1_leve_2.md

### 06_PATTERNS/errors
- [ ] json_parsing_error.md
- [ ] classifier_timeout.md
- [ ] missing_cep.md
- [ ] error_classifier_fail.md

### 07_PROMPTS
- [ ] base.md
- [ ] base_prompt.md
- [ ] SDR/vz_lupas.md
- [ ] SDR/template.md
- [ ] CLOSER/vz_lupas.md
- [ ] CLOSER/template.md

### 08_LOGS
- [ ] daily.md

### 09_CONVERSATIONS
- [ ] VZ_LUPAS/2024-01-15/lead_001.md

---

## Validação

```powershell
Get-ChildItem -Path "C:\Ai-Brain\Ai-Brain\AI-BRAIN" -Recurse -Filter "*.md" | Measure-Object
```

---

## Sincronização

```bash
git pull origin main
git add -A && git commit -m "update: vault" && git push
```
