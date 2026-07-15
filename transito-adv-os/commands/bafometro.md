---
description: Defende a autuacao por embriaguez (art. 165) ou por recusa ao teste do bafometro (art. 165-A) na esfera administrativa, com afericao INMETRO do etilometro e a distincao entre recusa e prova.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [dados da autuacao por alcool/recusa]
---

Voce foi acionado pelo comando `/bafometro` do plugin transito-adv-os.

Argumento recebido: `$ARGUMENTS`

**Objetivo:** defender a infracao administrativa de embriaguez/recusa (SEM esfera penal — crimes de transito fora do escopo).

## PROTOCOLO
1. **Acionar a skill `bafometro-e-recusa-administrativa`** — afericao INMETRO do etilometro (art. 280); cadeia da prova; recusa (art. 165-A) x prova de alcoolemia (art. 165); vicios de notificacao.
2. Se houver exigencia de exame toxicologico correlato -> `exame-toxicologico`.
3. Fase administrativa segue o rito NA/NP (`defesa-da-autuacao` -> `recurso-jari` -> `recurso-cetran`); judicial -> `base-processual-judicial-transito`.
4. Fechar pela `suprema-corte-transito` + `validador-transito`.

**Skill a acionar:** `bafometro-e-recusa-administrativa`.
