---
name: acao-anulatoria-multa-infracao
description: "Redige acao anulatoria (declaratoria de nulidade) de multa/infracao/penalidade de transito no Judiciario, articulando as nulidades do AIT (art. 280/281 CTB) e os vicios do processo administrativo: dupla notificacao (Sumula 312 STJ), NA fora dos 30 dias (art. 281 p.u. II), cerceamento de defesa. Use quando o operador disser anular a multa na justica, anulatoria de multa/infracao, acao para cancelar a autuacao, derrubar a penalidade no Judiciario, ja perdi na JARI/CETRAN e quero ir a justica, ou a multa esta indevida e quero anular judicialmente."
---

# ACAO-ANULATORIA-MULTA-INFRACAO — nulidade judicial da autuacao

> Camada 6 (Judicial · standalone). Leva ao juiz o vicio do AIT ou do processo administrativo de multa. Passa ANTES por `peticao-inicial-transito` (competencia/valor/reu). Fecha por `suprema-corte-transito`.

## Anexos obrigatorios (context/)
- `context/nulidades-do-ait.md` (as teses ranqueadas FORTE/MEDIA/FRACA — espinha da peca).
- `context/ctb-9503-97.md` (arts. 280/281/282 — grep) + `context/processo-adm-fluxo-prazos.md` (prazos NA/NP) + `context/jurisprudencia-transito.md` (Sumula 312/434, so ✅).

## Objetivo
Obter sentenca que **anule o AIT / a penalidade** por vicio formal ou material, com pedido de baixa dos pontos e devolucao do valor pago (se pago), fundada nas nulidades verificadas — sem prometer o que a tese nao entrega.

## Quando ativar
- Ha vicio concreto no AIT ou no processo de multa e o cliente quer decisao judicial (esgotou o adm, ou opta por ir direto).
- Cabe declaratoria de nulidade de ato administrativo (nao e MS quando ha necessidade de dilacao probatoria — se o direito e liquido e certo, ver `mandado-de-seguranca-transito`).

## Fundamento das nulidades (o merito da peca)
Base geral: **art. 281, p.u., I CTB** — auto arquivado quando "inconsistente ou irregular" (gancho de quase toda nulidade formal), combinado com o requisito violado do **art. 280**. Ranquear e escolher as FORTES:

**FORTES (carregam a acao):**
- **Ausencia de dupla notificacao** — recebeu so a NP, sem NA para defesa previa: **Sumula 312 STJ** (necessarias as notificacoes da autuacao E da penalidade) + CTB 280/281/282. Cerceamento de defesa (CF 5, LV).
- **NA expedida apos 30 dias** da infracao → arquivamento/insubsistencia: **art. 281, p.u., II CTB** + art. 4 §1 Res. 918/2022. Juntar a NA com data de expedicao/postagem.
- **Erro em local/data/hora** (fato impossivel, veiculo comprovadamente em outra cidade) — art. 280, II. Prova de alibi (nota fiscal, extrato de tag/pedagio, GPS).
- **Falta/erro na identificacao do orgao/agente autuador** ou orgao incompetente — art. 280, caput.
- **Equipamento sem afericao INMETRO vigente** na data (radar/etilometro) — art. 280 c/c Res. 432/2013; requerer que o orgao juntou o certificado; ausencia + cerceamento. 🟡 nao afirmar nº de portaria INMETRO sem `validador-transito`.

**MEDIAS (acoplar a uma forte):**
- **Enquadramento legal errado** (codigo nao bate com o fato narrado) — art. 280, I.
- **Sinalizacao irregular/ausente** — art. 90 CTB (nao se aplica sancao por sinalizacao nao visivel/insuficiente/incorreta); prova fotografica do trecho.
- **Cerceamento no julgamento adm** (decisao-padrao sem enfrentar argumentos; negativa de acesso a imagens/laudo).

**FRACA / MITO (desmentir — NAO usar como tese principal):**
- **"Falta de assinatura do condutor no AIT anula"** — FALSO. O AIT e valido sem assinatura do infrator (recusa/fuga/autuacao eletronica) — art. 280 preve "quando possivel". 🔴 mito de balcao.

## Estrutura da peca
1. **Cabeca** (de `peticao-inicial-transito`): vara/competencia (esfera do orgao), reu (o ente), valor (valor da multa).
2. **Fatos:** cronologia AIT → NA → NP → (defesa/JARI/CETRAN se houve) com as datas e os documentos.
3. **Direito:** as nulidades FORTES escolhidas, cada uma com dispositivo + Sumula 312 quando cabivel; afastar o mito da assinatura se o cliente insistir.
4. **Tutela de urgencia** (se ha perigo — pontos prestes a suspender, CNH travada): cross-link `tutela-urgencia-transito` (CPC 300).
5. **Pedidos:** declaracao de nulidade do AIT/penalidade; baixa dos pontos no RENACH; **devolucao do valor pago com correcao** (CTB 286 §2 + Sumula 434 STJ — pagamento nao inibe a discussao); honorarios; gratuidade se cabivel.

## Postura honesta
- **Nulidade nao e automatica:** o juiz exige vicio concreto e prejuizo (pas de nullite sans grief). "Anula qualquer multa" e promessa falsa.
- **Sumula 434 STJ** so cobre "pagou pode discutir/devolver" — nao e defesa previa (essa e Sumula 312 + CTB 281).
- **Prescricao:** a pretensao punitiva prescreve por analogia a Lei 9.873/99 (tese majoritaria, sem sumula de transito) — bom argumento, nao "batido". 🟡 nº de anos ao `validador-transito`. Nunca citar Tema 1.293 STJ (e ADUANEIRO, nao transito).

## Entrega obrigatoria final
Anulatoria redigida ponta a ponta (cabeca + fatos + nulidades FORTES fundamentadas + tutela se houver + pedidos com devolucao/baixa de pontos) + checklist de documentos (AIT, NA, NP, prontuario).

## Guard
Nenhum dispositivo/sumula/resolucao/prazo sem `validador-transito`. Nao usar o mito da assinatura como tese central. Entrega pela `suprema-corte-transito` (R1-R4). Cross-link, nao duplicar: direito liquido e certo sem prova a produzir → `mandado-de-seguranca-transito`; suspensao/cassacao → `anulatoria-suspensao-cassacao`; calculo da devolucao → `calculosjudiciais`.
