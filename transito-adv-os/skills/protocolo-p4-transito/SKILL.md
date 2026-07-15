---
name: protocolo-p4-transito
description: "Cruzamento multi-esfera de um mesmo fato de transito: administrativa (defesa/JARI/CETRAN) x judicial (anulatoria/MS/reparatoria) x consumo (CDC contra operadora de pedagio/tag). Mapeia as frentes que rodam em PARALELO sem uma atropelar a outra, evita litispendencia/coisa julgada cruzada e sequencia os prazos. Ex.: autuacao de pedagio com tag ativa -> defesa administrativa + anulatoria da multa + reparatoria/CDC contra a operadora. Nao redige as pecas — orquestra quem redige. Use quando disser da pra atacar por varios lados?, administrativo e judicial ao mesmo tempo?, cabe processar a concessionaria tambem?, e o pedagio, defendo e processo?, estrategia multi-frente."
---

# PROTOCOLO-P4-TRANSITO — cruzamento administrativo × judicial × consumo

> Transversal. Um fato, varias esferas. **Orquestra as frentes** (nao duplica o conteudo das skills de peca). Diferencial estrutural: independencia das instancias bem usada.

## Anexos / skills-fonte
- `context/metodologia-transito.md`, `processo-adm-fluxo-prazos.md`, `pedagio-e-consumo.md`.
- Skills de execucao (cross-link, cada uma redige a sua peca): `defesa-da-autuacao`, `recurso-jari`, `recurso-cetran`, `acao-anulatoria-multa-infracao`, `mandado-de-seguranca-transito`, `acao-reparatoria-transito`, `tag-e-cobranca-indevida`.

## Quando ativar
- "Da pra atacar por varios lados?", "administrativo e judicial ao mesmo tempo?", "cabe processar a concessionaria/operadora tambem?", "e o pedagio, defendo e processo?", "estrategia multi-frente".

## As 3 esferas (independentes — art. 935 CC: a esfera adm nao vincula a civel/judicial)
1. **Administrativa** — dentro do proprio orgao: defesa da autuacao (NA) -> recurso JARI -> CETRAN. Barata, suspende a exigibilidade, **segura os pontos** (art. 18 Res.918). Sempre a 1a linha.
2. **Judicial** — quando a via adm falha ou ha ato ilegal de autoridade: `acao-anulatoria-multa-infracao` (desconstituir a multa/penalidade) ou `mandado-de-seguranca-transito` (contra bloqueio de CNH, recusa de renovar, exigencia de multa nao notificada para licenciar — Sumula 127).
3. **Consumo** — contra a **operadora** (Sem Parar/ConectCar/Veloe) ou concessionaria: `tag-e-cobranca-indevida`/`acao-reparatoria-transito` sob **CDC** (falha do servico art. 14, cobranca indevida art. 42 p.u., dano). Polo passivo **privado**, distinto do orgao de transito.

## Como cruzar sem se atropelar
1. **Mapear o fato uma vez** e listar todas as frentes cabiveis (memoria de caso).
2. **Nao litigar a mesma pretensao contra o mesmo reu em duas vias** (litispendencia). O truque e que os **pedidos e reus sao distintos**: anular a multa (contra o orgao) ≠ indenizar por cobranca indevida (contra a operadora) — rodam em paralelo legitimamente.
3. **Sequenciar prazos:** adm corre em dias **corridos** e tem prazo curto -> proteger primeiro (nao perder a defesa/recurso). Judicial em dias **uteis**. A tutela de urgencia judicial pode ser necessaria **enquanto** a adm tramita (ex.: liberar CNH ja bloqueada).
4. **Aproveitar prova entre esferas:** o extrato da tag (com saldo/tag ativa) serve na defesa adm **e** na reparatoria CDC.
5. **Fechar a matriz:** quem faz o que, em que esfera, com que prazo e qual skill executa.

## Exemplo-tipo (pedagio/free flow — art. 209-A)
Autuacao de evasao com **tag ativa e saldo**: (a) `defesa-da-autuacao` — auto nulo, faltou dolo de evasao (extrato prova o debito/tentativa); (b) se mantida, `recurso-jari`/`recurso-cetran`; (c) `tag-e-cobranca-indevida` — CDC contra a operadora que nao debitou (falha do servico + eventual cobranca/negativacao indevida). Tres frentes, dois polos passivos, uma so prova-chave.

## Postura honesta
Nem todo caso comporta 3 frentes — abrir so as que tem tese. Reparatoria/dano moral exige **dano concreto** (negativacao, apreensao, perda de emprego), nao mero aborrecimento. Nao multiplicar acoes para inflar honorario.

## Cross-link (soft)
Todas as skills de peca citadas acima + `parecer-transito` (decide se vale cada frente) + `calculosjudiciais` (quantum da reparatoria).

## Guard
Cada peca gerada pelas frentes passa individualmente por `validador-transito` + `suprema-corte-transito`. Este protocolo so **orquestra** — nao sela peca.
