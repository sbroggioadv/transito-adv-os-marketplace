---
name: anti-alucinacao-transito
description: "Guard local anti-alucinacao do plugin transito, acoplado ao guard global anti-alucinacao-juridica. Bloqueia QUALQUER citacao de dispositivo/resolucao/sumula/tema/prazo que tente entrar em peca sem verificacao real; carrega as 7 verdades duras + as correcoes travadas + os itens 🟡 proibidos. Use antes de citar qualquer fundamento de transito, ou quando o operador disser valida essa jurisprudencia, essa sumula esta vigente, essa resolucao ainda vale, esse artigo foi revogado, confere essa ementa, antes de citar, e verdade que aos 20 pontos perde a CNH."
---

# ANTI-ALUCINACAO-TRANSITO — Guard local

> Camada 0. Trava de seguranca. Nenhuma citacao — legal, infralegal ou jurisprudencial — entra em peca sem passar por aqui. Acoplada ao guard global `anti-alucinacao-juridica`. Trabalha junto do `validador-transito` (antes de selar) e da `suprema-corte-transito` (R2/R3).

## Anexos obrigatorios (context/)
- `context/resolucoes-contran-mapa.md` — vigentes x revogadas (o mapa anti-armadilha) — **grep + ler a faixa**.
- `context/ctb-9503-97.md` + `context/leis-14071-14599-15428.md` — conferir existencia/redacao/vigencia de dispositivo.
- `context/jurisprudencia-transito.md` — corpus com selos ✅/🟡; so ✅ e citavel.

## Objetivo
Impedir que dispositivo, resolucao, sumula, tema ou prazo **inexistente, revogado, alterado ou nao verificado** entre numa peca. Veredito binario por citacao: **VALIDADO** ou **BLOQUEADO**. O produto vende a verdade vigente, nao o folclore de balcao.

## As 7 VERDADES DURAS (repetir quando pertinente, NUNCA contrariar)
1. **Pontuacao = 20/30/40** conforme nº de gravissimas em 12 meses (art. 261, Lei 14.071/2020, desde 12/04/2021) — NUNCA "20 pontos e perde". **EAR = 40 fixo**.
2. **Resolucoes CONTRAN vigentes:** **918/2022** (notificacao/multas), **900/2022** (defesa + recurso JARI/CETRAN), **931/2022** (SNE), **901/2022** (CETRAN), **723/2018 alt. 844/2021** (suspensao/cassacao). **NUNCA** 619/2016, 299/2008, 692/2017, 622/2016 (revogadas).
3. **art. 262 CTB REVOGADO** (Lei 13.281/2016) — remocao ao deposito = **art. 271**, leilao = **art. 328** (Lei 13.160/15).
4. **Lei 15.428/2026** (05/06/2026, pos-cutoff): CNH fisica OU digital com **fe publica** (art. 159) + **renovacao automatica via RNPC** (art. 268-A §7º). Nenhum modelo de jan/2026 tem — capturada do Planalto.
5. **Prazos administrativos em dias CORRIDOS** (art. 29 Res. 918) — "dias uteis" e erro de internet que faz perder prazo. **NA ≠ NP** (fases distintas). **SNE presume ciencia 30 dias** apos inclusao, mesmo sem abrir.
6. **TRUNFO (art. 18 Res. 918):** os pontos so vao ao RENACH **apos esgotados os recursos** — recorrer segura os pontos.
7. **Postura honesta:** nulidades do AIT ranqueadas FORTE/MEDIA/FRACA; o **"falta de assinatura anula" e MITO** (tese FRACA — desmentir); nunca prometer "anula qualquer multa".

## Correcoes travadas (nao repetir os erros da pesquisa)
- **Sumula 434 STJ ≠ "defesa previa".** Ela diz que **o pagamento nao inibe a discussao judicial**. Defesa previa = **Sumula 312 STJ** (dupla notificacao) + CTB art. 281 §ú. Citar 434 SO para pagamento x discussao.
- **Tema 1.293 STJ e ADUANEIRO, NAO transito** — nunca cita-lo como prescricao intercorrente de transito. Prescricao de transito = **Lei 9.873/99 por analogia** (5 anos; intercorrente 3 anos), tese majoritaria SEM sumula/tema proprio (usar com ressalva honesta).
- **"CNH sem autoescola" (2025) = PROPOSTA, nao vigente** — Res. 1020/2025 nao e isso; curso em CFC segue obrigatorio.
- **Tema 1.122 STJ so animais DOMESTICOS** (concessionaria responde objetiva) — nao estender a silvestres (ai e responsabilidade do Estado). Assalto a mao armada = fortuito externo (REsp 1.872.260/SP).

## Ancoras ✅ (citaveis apos conferir no anexo)
Sumula 312 STJ (dupla notificacao — espinha da nulidade) · Sumula 127 STJ (renovacao/licenciamento nao condicionado a multa nao notificada) · Sumula 434 STJ (pagamento x discussao) · SV 21 STF (recurso adm sem deposito) · Tema 1.122 STJ (concessionaria x animal domestico) · Sumula 585 STJ (comunicacao de venda) · art. 209 + 209-A (free flow, Lei 14.157/2021) · art. 258 (multa 293,47/195,23/130,16/88,38) · art. 259 (pontos 7/5/4/3) · fluxo NA(30d)->defesa(≥30d)->NP(180/360)->JARI->CETRAN(30d).

## 🟡 PROIBIDO afirmar sem verificacao (marcar "a confirmar" -> `validador-transito`)
Multiplicadores exatos (NIC 2× do art. 257 §8º, toxicologico 5× do art. 165-B), nº da portaria INMETRO do etilometro, prazos exatos da Res. 900/2022 e 844/2021, nº de anos da prescricao (5/3 por analogia a Lei 9.873/99), nº da resolucao do free flow, rol fechado das infracoes autossuspensivas, faixa exata do prazo de suspensao (art. 261), composicao atual do CONTRAN (art. 10).

## Metodologia
1. Recebida uma citacao, classificar: dispositivo/resolucao (lei) ou jurisprudencia.
2. **Dispositivo/resolucao:** grep no anexo — existe, esta vigente, tem a redacao alegada? Bater contra as verdades duras §1-4. Revogada/errada -> BLOQUEADO.
3. **Jurisprudencia:** achar em `jurisprudencia-transito.md`. **✅** -> VALIDADO; **🟡** -> abrir inteiro teor ao vivo (`WebSearch`/`WebFetch`; Firecrawl/Perplexity fallback) na fonte oficial (STJ/STF/TJ); **nao consta** -> busca ao vivo obrigatoria.
4. **Acionar o guard global** `anti-alucinacao-juridica` em paralelo.
5. **Veredito por citacao:** VALIDADO (com fonte) ou BLOQUEADO (motivo: inexistente / revogado / 🟡 nao aberto / contraria verdade dura / correcao travada). Na duvida -> BLOQUEADO.

## Entrega obrigatoria final
- Lista de citacoes com veredito (VALIDADO/BLOQUEADO) + fonte/ponteiro + motivo. As bloqueadas saem da peca. Entrega o resultado para a `suprema-corte-transito` (R2/R3).

## Guard
Default no incerto e **BLOQUEAR**. Nada inventado, nada revogado (nunca 619/2016 nem art. 262), nada 🟡 sem conferencia ao vivo, nunca "20 e perde", nunca Sumula 434 como defesa previa, nunca Tema 1.293 como transito.
