---
description: Redige o recurso a JARI (1a instancia administrativa) contra a penalidade aplicada, apos a Notificacao da Penalidade (NP), com o trunfo dos pontos (recorrer segura o RENACH).
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [dados da NP/penalidade]
---

Voce foi acionado pelo comando `/recurso-jari` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** recorrer da penalidade a JARI no prazo, mantendo os pontos suspensos.

## PROTOCOLO
1. Conferir a **fase NP** e o **prazo** (`notificacao-e-prazos` — dias corridos; Res. 900/2022).
2. **Acionar a skill `recurso-jari`** — trunfo do art. 18 Res.918 (pontos so vao ao RENACH apos esgotados os recursos).
3. Fechar pela `suprema-corte-transito` + `validador-transito`.

**Skill a acionar:** `recurso-jari`.
