---
name: base-legal-ctb
description: "Recupera e explica dispositivos do CTB (Lei 9.503/97) vigente sob demanda das outras skills do plugin transito. Localiza o artigo por grep em context/ctb-9503-97.md, traz texto verbatim + finalidade + requisitos + pegadinha, e cruza com context/leis-14071-14599-15428.md e context/resolucoes-contran-mapa.md para checar reforma e resolucao vigente. Cobre multa (258), pontos (259), processo adm (280-290), medidas adm (269-271), suspensao/cassacao (261/263), alcool (165/165-A/277), toxicologico (148-A/165-B/C/D), pedagio (209/209-A), CNH (159 + Lei 15.428/2026), indicacao (257). Use quando precisar do texto exato/vigente de um artigo do CTB, ou quando o operador disser qual o art. do CTB sobre X, o que diz o CTB sobre multa/ponto/suspensao/alcool, base legal, esse artigo ainda esta em vigor, esse art. nao foi revogado?"
---

# BASE-LEGAL-CTB — Recuperador de dispositivos do CTB (Lei 9.503/97)

> Camada 1 (Fundacao). Fonte de verdade do CTB para as demais skills. Nao redige peca: entrega o dispositivo correto, VIGENTE e explicado — nunca de memoria.

## Anexos obrigatorios (context/)
- `context/ctb-9503-97.md` — CTB consolidado (texto vigente). **Nunca ler inteiro:** localizar o artigo por grep e ler so a faixa.
- `context/leis-14071-14599-15428.md` — reformas (14.071/2020 pontuacao+validade CNH; 14.599/2023 toxicologico; **15.428/2026 pos-cutoff** CNH digital/RNPC). Ler SEMPRE antes de citar artigo potencialmente alterado.
- `context/resolucoes-contran-mapa.md` — resolucao CONTRAN vigente x revogada (o dispositivo remete a regulamento).
- `context/metodologia-transito.md` — quando chamada pelo `transito-master`.

## Objetivo
Devolver, para qualquer artigo/inciso/paragrafo do CTB: **texto exato vigente** + **finalidade** + **requisitos** + **pegadinha/status de reforma** — sem reproduzir o codigo inteiro e sem inventar redacao.

## Quando ativar
- Outra skill (analise do AIT, defesa, recurso, suspensao, bafometro, pedagio, peca judicial) precisa do dispositivo fundante.
- O operador pergunta qual artigo rege a infracao/penalidade/medida, ou pede o texto literal de um art. do CTB.
- Ha duvida se o artigo esta vigente ou foi alterado/revogado.

## Metodologia
1. **Localizar por grep**, nunca abrir o anexo inteiro: `grep -n "^Art\. 261\b" context/ctb-9503-97.md` (ajuste o numero) ou por tema `grep -niE "suspensao|pontos|alcool" context/ctb-9503-97.md`.
2. **Ler so a faixa** (do artigo ate o proximo `Art.`), copiar a redacao **verbatim**.
3. **Checar reforma** em `leis-14071-14599-15428.md` antes de entregar.
4. **Explicar em 4 blocos:** texto vigente -> finalidade -> requisitos/incisos -> pegadinha.

## Ancoras firmes (pode citar direto — ja verificadas)
- **Art. 258** valores base: gravissima **R$ 293,47** · grave **R$ 195,23** · media **R$ 130,16** · leve **R$ 88,38**. Fator multiplicador (x2/x3/x5/x10...) vem no PROPRIO tipo — ver 🟡 abaixo.
- **Art. 259** pontos: gravissima **7** · grave **5** · media **4** · leve **3**.
- **Art. 261** suspensao por pontos em 12 meses (Lei 14.071/2020, desde 12/04/2021): **20 pts** se 2+ gravissimas · **30 pts** se 1 gravissima · **40 pts** se nenhuma. EAR = **40 fixo**. II = infracao autossuspensiva.
- **Art. 263** cassacao (3 hipoteses): I dirigir com direito suspenso · II reincidencia 12m nos arts. 162-III/163/164/165/173/174/175 · III condenacao por delito de transito. §2º reabilitacao apos **2 anos** (refaz todos os exames).
- **Art. 269-271** medidas adm; **art. 271** = remocao ao deposito (restituicao so com pagamento de taxas/estada). ⚠️ **art. 262 REVOGADO** (Lei 13.281/2016) — NUNCA citar; leilao = **art. 328**.
- **Art. 280/281** requisitos do auto + arquivamento (281 §u: I inconsistente/irregular; **II se a NA nao for expedida em 30 dias**). **282** NP · **282-A** notificacao eletronica (base do SNE) · **284** pagamento com desconto · **285** recurso a autoridade (JARI, efeito suspensivo) · **286** recurso sem recolher valor · **288/289** 2ª instancia (CETRAN).
- **Art. 257 §7º** indicacao do condutor: **30 dias** da NA (ampliado de 15 pela Lei 14.071/2020). **§8º** NIC (PJ que nao indica) — multa autonoma.
- **Art. 159** CNH: validade escalonada §10 (10 anos <50 · 5 anos 50-<70 · 3 anos >=70). **Caput reescrito pela Lei 15.428/2026:** CNH fisica OU digital, **fe publica**, equivale a documento de identidade. **Art. 268-A §7º** (Lei 15.428/2026): renovacao **automatica** via RNPC.
- **Art. 165** dirigir sob influencia de alcool/psicoativo: gravissima + suspensao **12 meses**. **165-A** recusa ao teste = infracao **AUTONOMA**, mesma penalidade. **277** procedimento de fiscalizacao (etilometro, exame, sinais).
- **Art. 148-A** toxicologico C/D/E (Lei 14.599/2023): resultado negativo + reexame a cada **2 anos e 6 meses** para <70 anos. **165-B/165-C/165-D** infracoes novas (dirigir sem exame / positivo / apos 30 dias do vencimento).
- **Art. 209** transpor bloqueio viario / balanca: **grave** + multa. **209-A** free flow (Lei 14.157/2021).
- **Art. 232** conduzir sem documento de porte: **leve** + retencao — tese contra autuacao quando havia **CNH-e** (fe publica, art. 159 + Lei 15.428/2026).

## 🟡 PROIBIDO afirmar sem confirmar (marcar "a confirmar" -> `validador-transito`)
- **Multiplicador exato** de gravissima (ex.: 165 = "dez vezes"; 165-B = "cinco vezes"; NIC 2x): confirmar no proprio tipo antes de calcular valor final.
- **Faixa exata do prazo de suspensao** (art. 261) e regra EAR de reciclagem preventiva.
- **Rol fechado das infracoes autossuspensivas.**
- Composicao atual do CONTRAN (art. 10 — mexido por 14.071 e 14.599).

## Postura honesta
Lei VIGENTE 2026 manda. Nao citar art. 262 (revogado), nao dizer "20 pontos e perde" (e 20/30/40), nao tratar "CNH sem autoescola" como vigente (e proposta). Multiplicador/valor final so com o tipo aberto.

## Cross-link soft (nao duplicar)
Fluxo/prazos administrativos -> `base-processual-administrativo-transito`. Precedente -> `jurisprudencia-transito`. Execucao fiscal da multa -> `execucao`. IPVA -> `tributario` (fora).

## Guard
Nenhum dispositivo entregue sem confirmar a redacao no anexo via grep e o status de reforma em `leis-14071-14599-15428.md`. Na duvida de vigencia/numero/multiplicador, acionar `validador-transito` e bloquear. Toda peca que use isto fecha pela `suprema-corte-transito`.
