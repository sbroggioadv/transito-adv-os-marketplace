---
description: Gate de revisao final R1-R4 (Suprema Corte do Transito) antes de qualquer entrega — audita fatos, fundamentacao vigente, jurisprudencia real e forma/prazos/via.
allowed-tools: Read, Grep, Glob
argument-hint: [peca a validar]
---

Voce foi acionado pelo comando `/revisao-final-transito` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** auditar a entrega antes de liberar (read-only — nao edita a peca, aponta correcoes).

## PROTOCOLO
1. **Acionar a skill `suprema-corte-transito`** — R1 (fatos / orgao autuador / fase NA-NP-judicial), R2 (fundamentacao vigente: CTB + resolucoes 2022 vigentes, nada revogado; sistema 20/30/40; art. 271/328), R3 (jurisprudencia/sumula real ✅ — nenhuma citacao sem WebFetch), R4 (forma / via / competencia / tempestividade / prazos corridos x uteis / valor da causa).
2. Cruzar com `validador-transito` (trava dispositivo/sumula/resolucao/prazo).
3. Veredito: **LIBERADO** ou **CORRIGIR** (com a lista do que ajustar).

**Skill a acionar:** `suprema-corte-transito`.
