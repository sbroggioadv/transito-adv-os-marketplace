---
name: base-processual-administrativo-transito
description: "Fonte de verdade do RITO administrativo de transito: fluxo NA->defesa da autuacao->NP->recurso JARI->CETRAN, com os prazos EXATOS (dias CORRIDOS, art. 29 Res. 918/2022), o dies a quo de cada fase, o mapa de resolucoes CONTRAN vigentes (918/900/931/901) e o SNE. Guarda o TRUNFO (art. 18 Res.918: pontos so vao ao RENACH apos esgotados os recursos) e a SV 21 STF (recurso sem deposito). Use quando precisar saber em que fase o cliente esta, qual o prazo de defesa/recurso, quando conta o prazo, se a NA estourou 30 dias, qual resolucao rege a notificacao, como funciona o SNE, ou quando o operador disser recebi uma multa/notificacao e nao sei o prazo, qual o rito administrativo, defesa previa ou recurso, prazo da JARI/CETRAN."
---

# BASE-PROCESSUAL-ADMINISTRATIVO-TRANSITO — Rito e prazos da esfera administrativa

> Camada 1 (Fundacao). O coracao do produto (o fosso). Nao redige peca: entrega o fluxo, a fase e o prazo corretos e vigentes. Triar a fase (NA ou NP?) e a 1ª coisa — muda a peca.

## Anexos obrigatorios (context/)
- `context/processo-adm-fluxo-prazos.md` — fluxo + tabela de prazos por linha (fonte por artigo).
- `context/resolucao-918-2022.md` — Res. CONTRAN 918/2022 verbatim (notificacao/multas/indicacao/prazos). **Grep, nao ler inteiro.**
- `context/resolucoes-contran-mapa.md` — vigentes x revogadas (nunca citar revogada).
- `context/metodologia-transito.md` — quando chamada pelo `transito-master`.

## Objetivo
Devolver, para o caso: **fase atual** (defesa da autuacao x recurso da penalidade), **prazo** (com dies a quo e contagem em dias corridos), **fundamento** (CTB + artigo da Res.918) e o **trunfo** aplicavel — sem inventar prazo.

## Quando ativar
- Triar em que fase o cliente esta (recebeu **NA** = defesa da autuacao; recebeu **NP** = recurso a JARI).
- Calcular/checar prazo de defesa, indicacao de condutor, recurso JARI ou CETRAN.
- Duvida se a NA estourou 30 dias (arquivamento) ou se o SNE ja presumiu ciencia.

## O fluxo (ancorado — ✅)
```
INFRACAO -> AIT (art. 280 CTB; sem prazo p/ lavrar)
 -> [1] NOTIFICACAO DA AUTUACAO (NA): orgao tem ATE 30 dias CORRIDOS da infracao
        (art. 4º Res.918 / art. 281 §u II CTB). Estourou -> ARQUIVAMENTO do AIT. TESE FORTE.
 -> [2] DEFESA DA AUTUACAO (="defesa previa"): prazo NAO INFERIOR A 30 dias da NA (art. 4º §2º).
        No MESMO prazo: INDICACAO do real condutor (art. 5º Res.918).
 -> [3] JULGAMENTO (art. 9º): acolhida -> AIT cancelado. Indeferida -> aplica penalidade + NP:
        ATE 180 dias da infracao (sem defesa) / ATE 360 dias (com defesa) — art. 9º §2º/§3º.
 -> [4] NOTIFICACAO DA PENALIDADE (NP) (art. 12 Res.918 / art. 282 CTB): traz valor, desconto e
        DATA DE VENCIMENTO (= prazo-limite do recurso).
 -> [5] RECURSO A JARI (1ª inst.): ate o VENCIMENTO da NP, min. 30 dias (art. 285 CTB). Efeito suspensivo.
 -> [6] RECURSO AO CETRAN/CONTRANDIFE (2ª inst.): 30 dias da ciencia da decisao da JARI (arts. 288/289
        CTB) — 🟡 confirmar nº de dias na Res. 900/2022. SEM deposito previo (SV 21 STF). ✅
 -> Esgotada a via adm -> pontos vao ao RENACH (art. 18 Res.918). Resta o JUDICIAL (anulatoria/MS).
```

## 3 armadilhas de prazo (travar sempre)
1. **Dias CORRIDOS, nao uteis** (art. 29 Res.918: "dias consecutivos" — exclui o dia da notificacao, inclui o do vencimento, prorroga p/ 1º dia util se cair em fim de semana/feriado). "Dias uteis" e **erro de internet** que faz perder prazo. 🔴 mito.
2. **NA != NP** — sao duas notificacoes distintas. Perder a defesa da autuacao (30 dias da NA) NAO impede o recurso a JARI, mas queima a 1ª janela (mais barata, melhor p/ vicio da NA). Triar a fase ANTES de escolher a peca.
3. **SNE presume ciencia em 30 dias** apos a inclusao no sistema, mesmo sem abrir o app (art. 10 §6º Res.918, por analogia). Perguntar "aderiu ao SNE/CDT?" e ajustar o dies a quo.

## Trunfos e regras de ouro (✅)
- **Art. 18 Res.918 — TRUNFO:** as penalidades so vao ao RENACH **apos esgotados os recursos** (JARI + 2ª inst.). **Recorrer SEGURA os pontos** — ouro para quem esta perto do limite de suspensao.
- **Art. 13 Res.918:** enquanto pende recurso com efeito suspensivo, sem restricao de licenciamento/transferencia.
- **SV 21 STF:** inconstitucional exigir deposito/arrolamento previo como condicao do recurso administrativo. ✅
- **Descontos (trade-off informado):** **20%** = pagamento ate o vencimento (paga 80% — art. 284 CTB / art. 20 Res.918). **40%** = recebe pela NP via SNE E **renuncia a defesa/recurso** (paga 60% — art. 284 §1º / art. 21 Res.918). Se ha tese de nulidade, recorrer pode valer mais que o desconto. ✅
- **Prescricao** da acao punitiva regida pela **Lei 9.873/1999** (art. 36 Res.918). ✅ que remete; 🟡 o **nº de anos** aplicavel por analogia (5 anos / 3 intercorrente) — confirmar antes de citar.

## 🟡 PROIBIDO afirmar sem confirmar (-> `validador-transito`)
Prazos exatos da **Res. 900/2022** (2ª instancia) e da **Res. 844/2021** (suspensao/cassacao); **nº de anos** da prescricao (Lei 9.873/99 por analogia); nº de resolucao do **free flow**. Marcar "a confirmar".

## Postura honesta
Resolucao vigente e **918/2022** (nao 619/2016), **900/2022** (nao 299/2008 nem 692/2017), **931/2022** (nao 622/2016), **901/2022**. Arquivamento por NA fora dos 30 dias e nulidade objetiva forte; prescricao intercorrente em transito e campo **em construcao** (bom argumento, sem repetitivo/sumula — ver `jurisprudencia-transito`).

## Cross-link soft (nao duplicar)
Dispositivo do CTB -> `base-legal-ctb`. Precedente (Sumula 312/127, SV 21) -> `jurisprudencia-transito`. Ida ao Judiciario -> `base-processual-judicial-transito`. Suspensao/cassacao (rito proprio) -> skills da Camada 3.

## Guard
Nenhum prazo/rito entregue sem confirmar no anexo (grep no `resolucao-918-2022.md` / `processo-adm-fluxo-prazos.md`) e sem checar vigencia da resolucao em `resolucoes-contran-mapa.md`. Na duvida, `validador-transito` e bloqueia. Peca fecha pela `suprema-corte-transito` (R3 prazos/dies a quo).
