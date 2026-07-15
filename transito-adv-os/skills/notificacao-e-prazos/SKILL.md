---
name: notificacao-e-prazos
description: Calcula prazos e ataca vícios de notificação no processo administrativo de trânsito (NA≠NP, dias corridos, SNE, arquivamento por NA fora de 30 dias, prescrição). Use quando precisar saber "qual o prazo pra defesa/recurso?", "a notificação chegou tarde demais?", "quando começa a contar?", "aderi ao SNE, muda alguma coisa?", "essa multa já prescreveu?", ou para calcular o dies a quo antes de qualquer peça.
---

# Notificação e Prazos (o relógio do processo administrativo)

## 1. Quando ativa
É a skill de **cálculo de prazo e vício de notificação** — consultada antes de qualquer peça (`defesa-da-autuacao`, `recurso-jari`, `recurso-cetran`) para fixar o **dies a quo** e checar se há nulidade de notificação (a mais forte das teses). Ativa em qualquer pergunta sobre prazo, data de chegada, SNE ou prescrição.

## 2. O fluxo e os prazos (dias CORRIDOS)
```
INFRAÇÃO → AIT (art. 280, sem prazo p/ lavrar)
   → [NA] Notificação da Autuação: órgão tem ATÉ 30 dias da infração
        estourou? → ARQUIVAMENTO do AIT (tese FORTE, objetiva)
   → [DEFESA da autuação]: prazo ≥ 30 dias da expedição da NA
   → [NP] Notificação da Penalidade: até 180 dias da infração (sem defesa) / 360 dias (com defesa)
   → [RECURSO JARI]: até o vencimento da NP (mín. 30 dias)
   → [RECURSO CETRAN]: 30 dias da decisão da JARI
   → esgotado → pontos ao RENACH (art. 18 Res.918)
```

## 3. Base legal ancorada
- **art. 281, p.ú., II CTB / art. 4º §1º Res. 918/2022** — NA não expedida em **30 dias** → arquivamento do AIT. **Súmula 312 STJ**: dupla notificação (autuação + penalidade) é obrigatória; só NP, sem NA, é nula.
- **art. 4º §2º Res. 918/2022** — defesa da autuação: **≥ 30 dias** da expedição da NA (≥15 dias para NA anterior a 12/04/2021, §6º).
- **art. 9º §§2º/3º Res. 918/2022** — NP até **180 dias** (sem defesa prévia) ou **360 dias** (com defesa) da infração.
- **art. 285 CTB / art. 12 IV Res. 918** — recurso JARI até o **vencimento da NP** (a data de vencimento = data-limite do recurso).
- **art. 288 CTB** — recurso CETRAN: **30 dias** da decisão da JARI.
- **art. 29 Res. 918/2022** — contagem em **dias CONSECUTIVOS (corridos)**: exclui o dia da notificação, inclui o do vencimento, prorroga ao 1º dia útil se cair em fim de semana/feriado.

## 4. As três armadilhas de prazo
1. **Dias corridos, NÃO úteis.** Há material de internet dizendo "dias úteis" para a 918/2022 — está **ERRADO** e faz perder prazo. Conte corridos por padrão (art. 29); só use úteis se a norma específica daquele ato disser expressamente. **Mito a desmentir.**
2. **NA ≠ NP.** São duas notificações distintas. "Defesa prévia" (contra a NA) é fase diferente do "recurso" (contra a NP). Sempre **triar em que fase o cliente está** antes de escolher a peça.
3. **SNE presume ciência em 30 dias.** Quem aderiu ao **SNE** (Sistema de Notificação Eletrônica, Res. 931/2022) é considerado notificado **30 dias após a inclusão** no sistema, **mesmo sem abrir** o app (analogia ao art. 10 §6º Res.918). Pergunte "você aderiu ao SNE/CDT?" e ajuste o dies a quo — a notificação eletrônica dispensa edital (art. 14 §4º Res.918).

## 5. Prescrição
- **art. 36 Res. 918/2022** — a prescrição da ação punitiva rege-se pela **Lei 9.873/1999**.
- 🟡 **A confirmar no `validador-transito`:** o **número de anos** aplicável (referência comum: **5 anos** para a pretensão punitiva e **3 anos** de prescrição intercorrente quando o processo fica parado >3 anos por inércia do órgão, por analogia à Lei 9.873/99). Não afirme o número em peça sem confirmar — é ponto sensível.

## 6. Trunfo: efeito suspensivo e RENACH
Enquanto pende recurso com efeito suspensivo, **os pontos NÃO entram no RENACH** (art. 18 Res.918) e o veículo fica sem restrição (art. 13). **Recorrer segura os pontos** — argumento decisivo para quem está perto do teto de suspensão (20/30/40 conforme gravíssimas, Lei 14.071/2020).

## 7. O que produzir
Uma **linha do tempo do caso**: data da infração → data de expedição da NA → prazo da defesa → data da NP → vencimento (prazo JARI) → decisão JARI (prazo CETRAN), marcando SNE (sim/não) e cada dies a quo. Aponte se algum prazo do **órgão** estourou (tese de arquivamento) e qual janela do **cliente** ainda está aberta.

## 8. Cross-link
Vícios do auto → `analise-auto-de-infracao`; peças por fase → `defesa-da-autuacao` / `recurso-jari` / `recurso-cetran`; estado do caso → `memoria-de-caso-transito`. Todo prazo/dispositivo passa pelo `validador-transito`.
