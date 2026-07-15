---
description: Redige a defesa previa da autuacao (fase da Notificacao da Autuacao — NA), antes da penalidade, com os vicios do AIT ranqueados e a tese de merito por tipo de infracao.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [dados do AIT/NA]
---

Voce foi acionado pelo comando `/defesa-autuacao` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** apresentar a defesa da autuacao no prazo correto.

## PROTOCOLO
1. Conferir a **fase** (`triagem-transito`) e o **prazo** (`notificacao-e-prazos` — dias corridos; defesa previa = Sumula 312 + CTB 281).
2. **Acionar a skill `defesa-da-autuacao`** — combina os vicios formais do AIT (`analise-auto-de-infracao`) com a tese de merito (`enquadramento-e-multas-comuns`).
3. Fechar pela `suprema-corte-transito` + `validador-transito`.

**Skill a acionar:** `defesa-da-autuacao`.
