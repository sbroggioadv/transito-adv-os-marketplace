---
description: Redige mandado de seguranca (Lei 12.016/2009) contra ato ilegal da autoridade de transito com direito liquido e certo — bloqueio de CNH, exigencia de multa nao notificada para licenciar (Sum. 127), suspensao viciada.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [ato coator + prova documental]
---

Voce foi acionado pelo comando `/mandado-seguranca` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** atacar ato de autoridade com ilegalidade/abuso e prova pre-constituida.

## PROTOCOLO
1. Checar cabimento com `base-processual-judicial-transito`: **direito liquido e certo** (sem dilacao — se depende de pericia, e anulatoria).
2. **Acionar a skill `mandado-de-seguranca-transito`** — ancoras em `context/cpc-transito.md`: coator = quem PRATICA o ato; **prazo decadencial de 120 dias** (art. 23); liminar do **art. 7º III**; **sem honorarios** (art. 25 + Sum. 105 STJ / 512 STF); competencia Estadual x Federal (CF 109 I — DNIT/PRF = Federal).
3. Fechar pela `suprema-corte-transito` + `validador-transito`.

**Skill a acionar:** `mandado-de-seguranca-transito`.
