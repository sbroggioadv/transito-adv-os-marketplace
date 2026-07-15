---
description: Trata a infracao de pedagio / free flow (art. 209 e 209-A, Lei 14.157/2021), a cobranca indevida de tag/pedagio e a responsabilidade da concessionaria por dano na via.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [situacao de pedagio / free flow / cobranca de tag / dano na via]
---

Voce foi acionado pelo comando `/pedagio` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** resolver a demanda de pedagio/concessionaria pela trilha correta.

## PROTOCOLO
1. **Infracao de nao pagamento / free flow:** `infracao-de-pedagio-e-free-flow` (art. 209 + 209-A ✅, Lei 14.157/2021 — prazo/regularizacao).
2. **Cobranca indevida de tag/pedagio (consumo):** `tag-e-cobranca-indevida` (relacao de consumo — cross-link `bancario`/consumo).
3. **Dano na via / responsabilidade da concessionaria** (buraco, animal — Tema 1.122 STJ: domestico x silvestre): `responsabilidade-concessionaria` (+ `calculosjudiciais` para o dano).
4. Peca judicial -> `base-processual-judicial-transito`; fechar pela `suprema-corte-transito` + `validador-transito`.

**Skill a acionar:** `infracao-de-pedagio-e-free-flow`, `tag-e-cobranca-indevida` ou `responsabilidade-concessionaria`, conforme o eixo.
