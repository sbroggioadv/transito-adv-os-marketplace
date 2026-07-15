---
description: Redige a acao anulatoria de multa/penalidade de transito (procedimento comum, CPC) quando ha vicio a provar, com competencia (Estadual x Federal), valor da causa e tutela de urgencia.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [caso a anular na Justica]
---

Voce foi acionado pelo comando `/anulatoria` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** levar ao Judiciario o que exige dilacao probatoria (pericia, testemunha, alibi de local/data).

## PROTOCOLO
1. Definir a via com `base-processual-judicial-transito`: **anulatoria** (precisa provar o vicio) x **MS** (direito liquido e certo, prova pronta -> `mandado-de-seguranca-transito`).
2. **Acionar a skill `acao-anulatoria-multa-infracao`** — pedido de anulacao + baixa de pontos + repeticao do indebito se pago (Sumula 434 STJ). Ancoras em `context/cpc-transito.md` (319 inicial, 292 valor da causa, 300 tutela; CF 109 I para competencia).
3. Se houver urgencia (CNH bloqueada, pontos iminentes) -> `tutela-urgencia-transito` (CPC 300).
4. Fechar pela `suprema-corte-transito` (R4 via/competencia) + `validador-transito`.

**Skill a acionar:** `acao-anulatoria-multa-infracao`.
