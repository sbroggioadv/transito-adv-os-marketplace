---
description: Conduz o processo de suspensao do direito de dirigir (ou cassacao da CNH) — defesa e recurso na esfera administrativa (Res. 723/2018 alt. 844/2021) e/ou anulatoria judicial, com o sistema de pontos 20/30/40 vigente.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [notificacao de instauracao / motivo da suspensao ou cassacao]
---

Voce foi acionado pelo comando `/suspensao` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** defender o condutor na suspensao/cassacao pela via correta.

## PROTOCOLO
1. Identificar o gatilho: pontos (20/30/40 conforme nº de gravissimas em 12 meses — art. 261, Lei 14.071/2020; EAR = 40 fixo — `sistema-de-pontuacao`) ou infracao autossuspensiva; conferir a fase.
2. **Administrativo:** `processo-suspensao-direito-dirigir` (defesa + recurso; Res. 723/2018 alt. 844/2021). Cassacao -> `cassacao-da-cnh`.
3. **Judicial:** esgotada/viciada a via administrativa -> `anulatoria-suspensao-cassacao` (com `tutela-urgencia-transito` para segurar a CNH).
4. Fechar pela `suprema-corte-transito` + `validador-transito`.

**Skill a acionar:** `processo-suspensao-direito-dirigir` (adm.) ou `anulatoria-suspensao-cassacao` (judicial), conforme a fase; `cassacao-da-cnh` se for cassacao.
