---
description: Porta unica do plugin transito — descreva a demanda em linguagem natural e o orquestrador identifica a fase (administrativa NA/NP ou judicial), dirime todas as skills e conduz o caso ate a entrega.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [descricao da demanda de transito]
---

Voce foi acionado pelo comando `/transito-master` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** conduzir qualquer demanda de transito de ponta a ponta, na defesa do condutor.

## PROTOCOLO
1. **Acionar a skill `transito-master`** — le `context/metodologia-transito.md`, classifica via `triagem-transito`, carrega `memoria-de-caso-transito`.
2. Triar a **fase** SEMPRE: administrativa (NA -> defesa -> NP -> JARI -> CETRAN, dias corridos) x judicial (anulatoria/MS, dias uteis) — nunca confundir os prazos.
3. Conduz os desdobramentos conforme a fase e o objetivo, com anti-alucinacao por design (`anti-alucinacao-transito`).
4. Toda entrega fecha pela `suprema-corte-transito` (R1-R4) + `validador-transito`.

**Skill a acionar:** `transito-master`.
