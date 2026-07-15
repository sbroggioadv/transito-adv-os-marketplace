---
description: Escolhe e redige o recurso JUDICIAL correto no processo de transito (ED, agravo de instrumento, agravo interno, apelacao, REsp/RE, agravo em recurso excepcional) com admissibilidade e tempestividade em dias uteis.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [decisao judicial a recorrer]
---

Voce foi acionado pelo comando `/recurso` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** recorrer da decisao judicial correta, no recurso certo (NAO confundir com recurso administrativo JARI/CETRAN).

## PROTOCOLO
1. Identificar a decisao (ancoras em `context/cpc-transito.md`): vicio (omissao/contradicao/obscuridade/erro) -> `embargos-de-declaracao` (5 dias, CPC 1.022-1.026; prequestiona antes do REsp/RE via 1.025); interlocutoria do rol 1.015 -> `agravo-de-instrumento`; monocratica do relator -> agravo interno (1.021); sentenca -> `apelacao-transito` (1.009); ultima instancia vs lei federal/CF -> `recursos-excepcionais` (REsp CF 105 III / RE CF 102 III); inadmissao de REsp/RE -> `contrarrazoes-e-agravos-excepcionais` (agravo do 1.042).
2. **Tempestividade: 15 dias uteis** (CPC 1.003 §5 + 219; ED = 5 dias) — dobro para a Fazenda.
3. **Barreira do transito:** REsp/RE nao passa em materia de fato (Sumula 7 STJ / 279 STF) — formular como questao de DIREITO.
4. Fechar pela `suprema-corte-transito` + `validador-transito`.

**Skill a acionar:** o recurso correspondente (`embargos-de-declaracao` / `agravo-de-instrumento` / `apelacao-transito` / `recursos-excepcionais` / `contrarrazoes-e-agravos-excepcionais`).
