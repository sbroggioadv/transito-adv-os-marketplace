---
name: parecer-transito
description: "Diagnostico HONESTO de viabilidade: vale a pena defender/recorrer? qual a chance real? Rankeia a forca da tese pelas nulidades do AIT (FORTE/MEDIA/FRACA), pesa custo x beneficio e explica o TRADE-OFF do desconto de 40% (aderir ao SNE e pagar 60% exige RENUNCIAR a defesa/recurso) contra o TRUNFO de recorrer (art. 18 Res.918 segura os pontos). Nao redige peca — decide se ha peca a redigir. Use quando disser vale recorrer?, qual a chance?, compensa brigar essa multa?, melhor pagar com desconto ou recorrer?, tenho chance de anular?, vale a pena o MS/anulatoria?"
---

# PARECER-TRANSITO — vale recorrer? qual a chance?

> Transversal / consultivo. **Nao redige peca — diz se ha peca a redigir.** Corta o folclore de balcao: nao promete "anula qualquer multa". A honestidade e o produto.

## Anexos / skills-fonte
- `nulidades-do-ait.md` (ranking FORTE/MEDIA/FRACA) e `processo-adm-fluxo-prazos.md` (prazos/desconto).
- `analise-auto-de-infracao`, `sistema-de-pontuacao`, `notificacao-e-prazos` — cross-link (insumos do diagnostico).

## Quando ativar
- "Vale recorrer?", "qual a chance?", "compensa brigar essa multa?", "melhor pagar com desconto ou recorrer?", "tenho chance de anular?", "vale o MS/anulatoria?".

## O que produzir — parecer em 5 blocos
1. **Fase e prazo (triar primeiro):** NA ou NP? Prazo vivo? (dias **corridos** no adm; dias **uteis** no judicial). Se o prazo virou, dizer — nao vender recurso morto.
2. **Forca da tese (ranking honesto):**
   - **FORTE** — falta/atraso da notificacao (Sumula 312, art. 281 p.u. II), erro de identificacao do veiculo/local, sinalizacao ausente (art. 90), equipamento sem afericao INMETRO, ponto lancado por infracao **nao definitiva** (art. 18 Res.918).
   - **MEDIA** — vicios formais menores do AIT (280), enquadramento discutivel.
   - **FRACA** — **"falta de assinatura do condutor/infrator anula" = MITO** (art. 280 pede a assinatura do infrator so "quando possivel"; a ausencia nao invalida — recusa/fuga/autuacao eletronica). Nao construir estrategia nisso. **NAO confundir** com a falta de identificacao do AGENTE autuador, que e tese **FORTE**.
3. **Custo x beneficio:** valor da multa (base art. 258: 293,47/195,23/130,16/88,38 + multiplicador do tipo 🟡) x honorarios/tempo x o que se ganha. Multa isolada e barata pode nao compensar acao judicial; **proximidade da suspensao** muda tudo.
4. **⚖️ O TRADE-OFF do desconto de 40% (o no da decisao):**
   - **Pagar com desconto** — art. 284 da 20% ate o vencimento; o **desconto de 40%** (pagar 60%) por adesao ao SNE **exige RENUNCIAR a defesa e ao recurso** (🟡 condicao/dispositivo vigente -> `validador-transito`). Economiza dinheiro, mas **assume a infracao E os pontos**.
   - **Recorrer (TRUNFO — art. 18 Res.918):** os pontos so vao ao RENACH **apos esgotados os recursos** -> recorrer **segura os pontos** enquanto tramita. Ouro para quem esta perto de 20/30/40.
   - **Regra pratica:** perto do limite de suspensao ou com tese FORTE -> recorrer (segura ponto + pode anular). Multa isolada barata, tese FRACA, longe do limite -> o desconto pode ser racional. **Decisao do cliente, informada** — nunca decidir por ele.
5. **Recomendacao + proximo passo:** trilha (defesa da autuacao / recurso JARI / CETRAN / anulatoria / MS) e a skill que executa — ou "nao vale, pague com desconto".

## Postura honesta (inviolavel)
Chance realista, nao esperanca vendida. Se a tese e FRACA, dizer. Se o prazo passou, dizer. Sem promessa de resultado (etica OAB). O desconto de 40% e as vezes a decisao certa — apresentar, nao esconder para vender peca.

## Cross-link (soft)
`triagem-transito` (fase) · `analise-auto-de-infracao` (nulidades) · `sistema-de-pontuacao` (proximidade da suspensao) · a skill de peca escolhida.

## Guard
Multiplicador de multa, desconto de 40% e prazos exatos marcados 🟡 -> `validador-transito` antes de afirmar numero. Parecer nao dispensa a revisao da peca depois pela `suprema-corte-transito`.
