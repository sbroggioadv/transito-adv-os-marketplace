---
name: triagem-transito
description: "Classifica a demanda de transito e roteia para as skills certas. A triagem CRITICA e a FASE: o cliente recebeu a Notificacao da Autuacao (NA) ou a Notificacao da Penalidade (NP)? — muda a peca. Depois define a trilha (multa/defesa, CNH suspensa/cassada/bloqueada, bafometro, pedagio/consumo, anulatoria/MS, recurso) e a via (administrativa x judicial). Use quando o operador descrever uma situacao de transito e nao souber o caminho, ou disser triagem, qual o caminho, que peca eu uso, em que fase estou, recebi uma multa, minha CNH esta suspensa, /triagem."
---

> **🖱️ Escolhas = botoes:** nas perguntas de **lista fechada** (fase NA/NP, trilha, aderiu ao SNE, via) use a ferramenta **AskUserQuestion** para mostrar **botoes clicaveis** (max. 4 por pergunta).

# TRIAGEM-TRANSITO

> Camada 0. Porta de classificacao. Chamada pelo `transito-master` no inicio de todo caso. Define **a FASE** (NA x NP) + trilha + via.

## Anexos obrigatorios (context/)
- `context/metodologia-transito.md` — mapa de skills + fluxo da porta unica — **grep + ler a faixa**.
- `context/processo-adm-fluxo-prazos.md` — para situar a fase e os prazos.

## Objetivo
Em poucas perguntas, dizer: **fase + trilha + via + skill(s) alvo + prazo em curso** e devolver o handoff para o `transito-master`.

## Primeira definicao — a FASE (SEMPRE, e critica)
**O cliente recebeu qual documento?**
- **Notificacao da Autuacao (NA)** — 1º aviso, abre a **defesa da autuacao** (defesa previa). Peca: `defesa-da-autuacao`. Ainda da para **indicar o real condutor** (`indicacao-de-condutor`).
- **Notificacao da Penalidade (NP)** — ja aplicou a multa/penalidade, abre o **recurso a JARI**. Peca: `recurso-jari` -> depois `recurso-cetran`.
- **So a cobranca / boleto / nada formal** — checar se houve dupla notificacao (Sumula 312); pode haver **nulidade** (`analise-auto-de-infracao`, `notificacao-e-prazos`).
> Errar a fase = peca errada. NA e NP sao DUAS notificacoes distintas. Confirmar tambem: **aderiu ao SNE?** (se sim, ciencia presumida 30 dias apos inclusao — muda o dies a quo).

## Tabela de roteamento (trilha -> skill alvo)
1. **MULTA / DEFESA** ("recebi uma multa", "quero contestar", "foi injusta") -> `analise-auto-de-infracao` (nulidades ranqueadas) -> conforme a fase: `defesa-da-autuacao` (NA) ou `recurso-jari`/`recurso-cetran` (NP); apoio: `notificacao-e-prazos`, `indicacao-de-condutor`, `enquadramento-e-multas-comuns`.
2. **CNH** ("estou perto do limite de pontos", "minha CNH foi suspensa/cassada/bloqueada", "nao consigo renovar", "toxicologico") -> `sistema-de-pontuacao` · `processo-suspensao-direito-dirigir` · `cassacao-da-cnh` · `cnh-bloqueio-renovacao-reabilitacao` · `exame-toxicologico`.
3. **BAFOMETRO** ("soprei/recusei o bafometro", "autuacao por embriaguez") -> `bafometro-e-recusa-administrativa` (165/165-A/277 — **so administrativo, sem o crime 306**).
4. **PEDAGIO & CONSUMO** ("multa de pedagio/free flow", "a tag nao debitou e vieram me cobrar", "acidente na rodovia por buraco/animal") -> `infracao-de-pedagio-e-free-flow` · `tag-e-cobranca-indevida` · `responsabilidade-concessionaria`.
5. **VEICULO** ("meu carro foi removido/apreendido", "vao levar a leilao", "licenciamento atrasado", "vendi e vieram multas") -> `remocao-apreensao-e-leilao` (art. 271/328) · `licenciamento-crlv-e-comunicacao-venda`.
6. **JUDICIAL** ("ja perdi na esfera administrativa", "quero anular na Justica", "mandado de seguranca", "quero indenizacao") -> `peticao-inicial-transito` + `acao-anulatoria-multa-infracao` / `mandado-de-seguranca-transito` / `anulatoria-suspensao-cassacao` / `tutela-urgencia-transito` / `acao-reparatoria-transito`.
7. **RECURSO JUDICIAL** ("recorrer da sentenca", "agravar da liminar", "REsp/RE") -> `apelacao-transito` · `agravo-de-instrumento` · `embargos-de-declaracao` · `recursos-excepcionais` · `contrarrazoes-e-agravos-excepcionais`.
8. **CONSULTIVO** ("vale a pena recorrer?", "qual minha chance?", "pago com desconto ou recorro?") -> `parecer-transito`; cruzamento multi-esfera -> `protocolo-p4-transito`.

## Gestao obrigatoria (sempre, antes da peca)
Toda peca passa por `base-legal-ctb` + a base processual da via (`base-processual-administrativo-transito` ou `base-processual-judicial-transito`) e o prazo e conferido em `notificacao-e-prazos` (dias corridos na via adm; dies a quo pelo SNE).

## Entrega obrigatoria final
- Fase (NA/NP) + trilha + via + skill(s) alvo + prazo em curso, em 3-5 linhas, e o handoff para o `transito-master`.

## Guard
Nao redigir peca aqui — so classificar e rotear. Na duvida da fase, perguntar de novo (a fase manda na peca). Demanda mista (ex.: multa de pedagio + acao contra a operadora): listar as skills na ordem certa para o master encadear (`protocolo-p4-transito`).
