---
name: suprema-corte-transito
description: "Gate de qualidade final do plugin transito. Aplica 4 validacoes (R1 fatos/fase/prazos, R2 fundamentacao vigente — CONTRAN consolidada nunca revogada, art. 271 nao 262, Lei 15.428/2026, R3 prazos corridos + dies a quo NA/NP/SNE, R4 forma/competencia/via adm x judicial) antes de qualquer entrega. Use SEMPRE antes de entregar defesa, recurso, peca ou parecer; acionada pelo transito-master ao fechar qualquer ato. Tambem quando o operador disser revisao final, valida antes de entregar, confere a peca, /revisao-final-transito."
---

# SUPREMA-CORTE-TRANSITO — Gate R1-R4

> Camada 0. Auditoria final obrigatoria. Nenhuma entrega sai sem passar por aqui.

## Anexos obrigatorios (context/)
- `context/ctb-9503-97.md`, `context/leis-14071-14599-15428.md`, `context/resolucao-918-2022.md`, `context/resolucoes-contran-mapa.md`, `context/processo-adm-fluxo-prazos.md`, `context/jurisprudencia-transito.md`, `context/metodologia-transito.md` — **grep + ler a faixa**, nunca despejar inteiro.

## As 4 validacoes

**R1 — Fatos, fase e prazos.** Os fatos batem com o caso (`memoria-de-caso-transito`)? **A FASE esta certa** — a peca corresponde a etapa em que o cliente esta (defesa da autuacao contra a NA x recurso a JARI/CETRAN contra a NP x acao judicial)? Ha prazo em curso e ele foi respeitado (ver R3)? Os documentos-chave (AIT, NA com data de expedicao, NP com vencimento, extrato do prontuario) foram considerados?

**R2 — Fundamentacao vigente.** Cada dispositivo/resolucao existe e esta vigente (cruzar com `ctb-9503-97.md` e `resolucoes-contran-mapa.md`)? Travas duras: **NUNCA** Res. 619/2016, 299/2008, 692/2017, 622/2016 (revogadas) — usar **918/2022, 900/2022, 931/2022, 901/2022, 723/2018 alt. 844/2021**. **art. 262 REVOGADO** — remocao = **art. 271**, leilao = **art. 328**. Pontuacao = **20/30/40** (art. 261), nunca "20 e perde". CNH digital com fe publica + renovacao automatica RNPC = **Lei 15.428/2026** (art. 159 / 268-A §7º). Toda sumula/tema/acordao passou pelo `anti-alucinacao-transito` + `validador-transito` e consta como ✅ em `jurisprudencia-transito.md`? Sumula 434 so para "pagamento nao inibe discussao" (nunca "defesa previa"); nunca Tema 1.293 (aduaneiro) como prescricao de transito; nunca "CNH sem autoescola" como direito vigente.

**R3 — Prazos corridos + dies a quo.** **Via administrativa = dias CORRIDOS** (art. 29 Res. 918/2022) — exclui o dia da notificacao, inclui o do vencimento, prorroga ao 1º dia util. **Via judicial = dias uteis** (CPC 219). O **dies a quo** esta certo? NA (orgao ate 30 dias da infracao, senao arquiva); defesa da autuacao (≥30 dias da expedicao da NA); NP (ate 180 dias sem defesa / 360 com defesa); JARI (ate o vencimento da NP); CETRAN (30 dias da decisao da JARI). **Aderiu ao SNE? ciencia presumida 30 dias apos inclusao** (mesmo sem abrir). MS = 120 dias da ciencia (Lei 12.016/09 art. 23).

**R4 — Forma, competencia e via.** A **via** esta certa (administrativa x judicial)? Enderecamento ao orgao correto (autoridade autuadora / JARI / CETRAN / vara)? Na via judicial: **competencia** (Justica Estadual x Federal conforme o orgao autuador — DNIT/PRF federal), valor da causa, requisitos CPC 319, tutela se cabivel, **SV 21 STF** (recurso adm sem deposito). Pedidos claros e coerentes com a tese? Postura honesta preservada (nulidade ranqueada; nada de "anula qualquer multa")?

## Metodologia
1. Rodar R1 -> R2 -> R3 -> R4 em ordem.
2. Marcar cada item OK / CORRIGIR.
3. Se CORRIGIR, devolver a skill de origem; nao entregar.
4. So liberar quando R1-R4 = OK.

## Entrega obrigatoria final
- Veredito (LIBERADO / CORRIGIR) + lista do que foi checado + correcoes.

## Guard
Na duvida em R2/R3, default e remover/checar ao vivo. Fase errada (peca de defesa quando ja era recurso), prazo perdido por contar dias uteis na via administrativa, resolucao revogada ou art. 262 = reprova. Nao "passar pano".
