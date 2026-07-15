---
name: defesa-da-autuacao
description: Redige a defesa da autuação (defesa prévia) contra a Notificação da Autuação (NA), a 1ª e mais barata janela de defesa. Use quando o cliente RECEBEU a NA (ainda não a NP/penalidade) e quer contestar a multa, quando pergunta "recebi a notificação da multa, o que faço?", "cabe defesa prévia?", ou para atacar vícios do AIT antes de virar penalidade. Não confundir com recurso à JARI (esse é contra a NP).
---

# Defesa da Autuação (defesa prévia)

## 1. Quando ativa
Ativa quando o cliente está na **1ª fase** do processo administrativo: recebeu a **Notificação da Autuação (NA)** e ainda **não** foi aplicada a penalidade. Confirme a fase por `triagem-transito` — se ele já recebeu a **NP** (Notificação da Penalidade), a peça é outra (`recurso-jari`), não esta.

Por que importa: a defesa da autuação é a **janela mais barata e mais fácil** de derrubar a multa por vício da NA/AIT, antes de virar penalidade e pontos. Perder essa janela **não** impede o recurso à JARI depois, mas perde a chance mais forte.

## 2. Base legal ancorada
- **art. 281 CTB** — a autoridade julga a consistência do auto; arquiva se inconsistente/irregular (p.ú. I) ou se a NA não saiu em 30 dias (p.ú. II).
- **art. 282 CTB** — não apresentada ou indeferida a defesa prévia, aplica-se a penalidade e expede-se a NP.
- **art. 4º §2º Res. CONTRAN 918/2022** — prazo da defesa da autuação: **não inferior a 30 dias** contados da **expedição da NA**. (NA anterior a 12/04/2021: não inferior a 15 dias — art. 4º §6º.)
- **art. 29 Res. 918/2022** — prazo em **dias CORRIDOS** (consecutivos): exclui o dia da notificação, inclui o do vencimento, prorroga ao 1º dia útil se cair em fim de semana/feriado. **Nunca dias úteis** — ver `notificacao-e-prazos`.
- **Súmula 312 STJ** — dupla notificação obrigatória (autuação + penalidade).

## 3. Passo a passo
1. **Rode `analise-auto-de-infracao`** — levante os vícios do AIT ranqueados FORTE/MÉDIA/FRACA. A defesa prévia é forte justamente para atacar vício da própria NA (prazo dos 30 dias, campos do art. 280).
2. **Cheque o prazo:** conte os ≥30 dias corridos a partir da **expedição** da NA. Se o cliente aderiu ao **SNE**, o dies a quo é a ciência presumida (30 dias após a inclusão no sistema) — ver `notificacao-e-prazos`.
3. **Endereço:** dirige-se à **autoridade autuadora** (o órgão que lavrou — Detran, PRF, prefeitura), não à JARI.
4. **Prova:** junte a NA, o AIT, e o que sustenta o vício (álibi de local/data; foto da sinalização; requerimento do certificado INMETRO).
5. **Pedido:** arquivamento do AIT e cancelamento da autuação (art. 281 p.ú.).
6. Se, no mesmo prazo, o caso for de **indicação do real condutor**, use `indicacao-de-condutor` (é o mesmo prazo, peça distinta).

## 4. Estrutura da peça
- Endereçamento à autoridade autuadora + nº do AIT/placa/data.
- Tempestividade (prazo ≥30 dias corridos da NA).
- Fatos.
- Fundamentos: art. 280 (campo violado) + art. 281 p.ú. I + súmula/anexo aplicável.
- Pedido de arquivamento; subsidiariamente, produção de prova (juntada do certificado do equipamento).

## 5. Postura honesta
A defesa prévia **não tem efeito suspensivo automático** dos pontos como o recurso — ela busca cancelar antes da penalidade. Se o único vício é FRACO (ex.: só a "falta de assinatura"), avise o cliente da baixa chance e pese o **desconto de 40%** (SNE + renúncia à defesa, art. 21 Res.918) contra o custo de defender — decisão informada (`parecer-transito`). Nunca prometa cancelamento certo.

## 6. Cross-link e fechamento
Vícios → `analise-auto-de-infracao`; prazos/SNE → `notificacao-e-prazos`; indicação → `indicacao-de-condutor`; se indeferida, próxima fase → `recurso-jari`. **Toda peça fecha pela `suprema-corte-transito` (R1-R4)** + `validador-transito` antes de entregar.
