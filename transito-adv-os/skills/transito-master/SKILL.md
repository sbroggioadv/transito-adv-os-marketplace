---
name: transito-master
description: "Orquestrador do plugin transito (defesa do condutor) e porta unica do Direito do Transito administrativo + judicial. Recebe qualquer demanda em linguagem natural, identifica a FASE (recebeu Notificacao da Autuacao ou da Penalidade?) e a trilha, e DIRIME (seleciona e conduz) TODAS as skills pertinentes sem esquecer nenhuma, fechando pela suprema-corte-transito. Use quando o operador descrever uma tarefa de transito sem chamar skill especifica, ou disser transito-master, recebi uma multa, fui autuado, vou recorrer, minha CNH esta suspensa/cassada/bloqueada, bafometro, multa de pedagio, quero anular a multa, mandado de seguranca de transito, /transito-master."
---

# TRANSITO-MASTER — Orquestrador (defesa do condutor)

> Camada 0. Porta unica do plugin transito-adv-os. Dirige TODAS as skills necessarias por tarefa, sem esquecer nenhuma. Foco: administrativo (o fosso) + civel-anulatoria/MS + recursos. **Sem penal** (crimes 302-312 fora do escopo v0.1).

## Anexos obrigatorios (context/)
- `context/metodologia-transito.md` (mapa de uso, fluxo, regras de ouro) — **ler primeiro, sempre**.
- Demais anexos sob demanda (CTB por grep do artigo; `resolucao-918-2022.md`; `resolucoes-contran-mapa.md`; jurisprudencia; pedagio; veiculo).

## Objetivo
Transformar qualquer demanda de transito em entrega correta e validada, conduzindo o ciclo sem perder o estado e sem esquecer nenhuma exigencia (prazo, fase, via).

## Metodologia
1. **Ler** `context/metodologia-transito.md`.
2. **Classificar** via `triagem-transito` — a triagem CRITICA e a FASE: recebeu **NA** (Notificacao da Autuacao) ou **NP** (Notificacao da Penalidade)? Sao fases distintas e mudam a peca. Depois: trilha + aderiu ao SNE? (define o dies a quo).
3. **Carregar** `memoria-de-caso-transito` (AIT, fase, datas NA/NP, pontos, SNE, processos em curso).
4. **Fundacao SEMPRE (Camada 1):** antes/junto de qualquer peca, acionar `base-legal-ctb` + a base processual da via (`base-processual-administrativo-transito` para defesa/JARI/CETRAN; `base-processual-judicial-transito` para anulatoria/MS) + `jurisprudencia-transito`. Esse e o "nao esquecer nada".
5. **Conduzir a trilha** (roteada pela triagem):
   - **Multa/defesa administrativa:** `analise-auto-de-infracao` -> `defesa-da-autuacao` (contra a NA) -> `recurso-jari` -> `recurso-cetran`; apoio: `notificacao-e-prazos`, `indicacao-de-condutor`, `enquadramento-e-multas-comuns`.
   - **CNH suspensa/cassada/bloqueada:** `sistema-de-pontuacao` · `processo-suspensao-direito-dirigir` · `cassacao-da-cnh` · `cnh-bloqueio-renovacao-reabilitacao` · `exame-toxicologico`.
   - **Bafometro (administrativo):** `bafometro-e-recusa-administrativa` (165/165-A/277; **sem o crime 306**).
   - **Pedagio/consumo:** `infracao-de-pedagio-e-free-flow` · `tag-e-cobranca-indevida` · `responsabilidade-concessionaria`.
   - **Veiculo:** `remocao-apreensao-e-leilao` (art. 271/328) · `licenciamento-crlv-e-comunicacao-venda`.
   - **Judicial:** `peticao-inicial-transito` -> `acao-anulatoria-multa-infracao` / `mandado-de-seguranca-transito` / `anulatoria-suspensao-cassacao` / `tutela-urgencia-transito` / `acao-reparatoria-transito`.
   - **Recurso judicial:** `apelacao-transito` · `agravo-de-instrumento` · `embargos-de-declaracao` · `recursos-excepcionais` · `contrarrazoes-e-agravos-excepcionais`.
   - **Consultivo:** `parecer-transito` (vale recorrer? chance?) · `protocolo-p4-transito` (cruzamento adm x judicial x consumo).
6. **Gate final:** toda entrega passa pela `suprema-corte-transito` (R1-R4) + `validador-transito`.
7. **Atualizar** `memoria-de-caso-transito` (ato praticado, proximo passo, prazo).

## Regras de ouro
- **Prazos ADMINISTRATIVOS em dias CORRIDOS** (art. 29 Res. 918/2022), NAO uteis. **Prazos JUDICIAIS em dias uteis** (CPC 219). Nao confundir as duas vias.
- **Fluxo adm:** NA (orgao expede em ate 30 dias da infracao, senao arquiva — Sumula 312) -> defesa da autuacao (≥30 dias) -> NP (ate 180/360 dias) -> JARI (ate o vencimento da NP) -> CETRAN (30 dias, sem deposito — SV 21).
- **Pontuacao 20/30/40** (art. 261, Lei 14.071/2020), nunca "20 e perde". **TRUNFO:** pontos so vao ao RENACH apos esgotados os recursos (art. 18 Res.918) — recorrer segura os pontos.
- **Postura honesta:** nulidades ranqueadas FORTE/MEDIA/FRACA; "falta de assinatura anula" e MITO; nunca prometer "anula qualquer multa".
- **Cross-link, nao duplicar:** processual civel -> `civel-adv-os`; execucao fiscal da multa -> `execucao-adv-os`; crimes de transito -> GAP (fora); cobranca indevida de tag -> `bancario-adv-os`/consumo; calculo de reparacao -> `calculosjudiciais-adv-os`; IPVA -> `tributario`.

## Entrega obrigatoria final
- Artefato da skill acionada, validado pela `suprema-corte-transito` + `memoria-de-caso-transito` atualizado + proximo passo/prazo.

## Guard
Nenhum dispositivo/sumula/resolucao/prazo sem `validador-transito`. Nunca produzir peca sem fixar a FASE (NA x NP) e a via (adm x judicial). Na duvida de vigencia/existencia, bloquear e checar (`anti-alucinacao-transito`).
