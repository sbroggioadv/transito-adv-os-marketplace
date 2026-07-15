---
description: Classifica a demanda de transito (fase administrativa NA/NP ou judicial + objetivo) e indica a skill, o orgao e o prazo corretos.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [descricao do caso]
---

Voce foi acionado pelo comando `/triagem` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** classificar e rotear o caso.

## PROTOCOLO
1. **Acionar a skill `triagem-transito`** — identifica a fase (NA/NP/administrativo x judicial), o objetivo, a skill-alvo, o orgao autuador (Estadual x Federal) e o prazo aplicavel.
2. Conferir prazos em `notificacao-e-prazos` (administrativo = dias corridos).
3. Encaminhar ao `transito-master`.

**Skill a acionar:** `triagem-transito`.
