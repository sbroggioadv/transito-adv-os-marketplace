---
description: Redige o recurso ao CETRAN/CONTRANDIFE (2a e ultima instancia administrativa) apos o indeferimento pela JARI, encerrando a via administrativa antes do Judiciario.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [decisao da JARI a recorrer]
---

Voce foi acionado pelo comando `/recurso-cetran` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** esgotar a via administrativa com o recurso ao CETRAN.

## PROTOCOLO
1. Conferir o **prazo de 30 dias** da decisao da JARI (`notificacao-e-prazos`; Res. 900/2022 e 901/2022 — SV 21 STF: sem deposito previo).
2. **Acionar a skill `recurso-cetran`**.
3. Se negado, avaliar a via judicial (`base-processual-judicial-transito` -> `acao-anulatoria-multa-infracao` ou `mandado-de-seguranca-transito`).
4. Fechar pela `suprema-corte-transito` + `validador-transito`.

**Skill a acionar:** `recurso-cetran`.
