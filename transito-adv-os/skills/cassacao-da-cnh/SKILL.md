---
name: cassacao-da-cnh
description: Defesa contra a CASSAÇÃO da CNH — art. 263 CTB, as 3 hipóteses TAXATIVAS (I dirigir com direito suspenso; II reincidência em 12 meses nos arts. 162 III, 163, 164, 165, 173, 174, 175; III condenação judicial por delito de trânsito) — e o caminho da reabilitação após 2 anos (art. 263 §2º, refazendo TODOS os exames de habilitação). Rito próprio (Res. 723/2018 alt. 844/2021), mesmo do processo de suspensão. Use quando o cliente foi "notificado de cassação", "vão cassar minha CNH", "cassação por dirigir suspenso/reincidência", "como reabilitar depois de cassada", ou defesa/recurso nesse processo.
---

# CASSACAO-DA-CNH

> Camada 3 (CNH). Cassação é a penalidade mais grave (perde a habilitação, não só suspende). As hipóteses do art. 263 são TAXATIVAS — cassar fora delas é nulidade. Reabilitação = recomeçar o processo do zero.

## Anexos obrigatórios (context/)
- `context/ctb-9503-97.md` — **grep art. 263** (caput I/II/III + §2º reabilitação) e os artigos da hipótese II (162 III, 163, 164, 165, 173, 174, 175). Ler o teor exato de cada um antes de afirmar reincidência.
- `context/resolucoes-contran-mapa.md` — rito da cassação = **Res. 723/2018 (alt. 844/2021)**, mesmo da suspensão (🟡 confirmar vigência 2026 e prazos).
- `context/jurisprudencia-transito.md` — Súmula 312 STJ (dupla notificação ✅) para vício de notificação no sancionador.

## Quando ativa
- Cliente **notificado da instauração de cassação** ou de cassação já aplicada.
- Flagrado **dirigindo durante a suspensão** (hipótese I) — a mais comum.
- **Reincidência em 12 meses** em uma das infrações do inciso II.
- **Condenação judicial** por crime de trânsito com efeito administrativo de cassação (III).
- Cliente quer saber **como/quando reabilitar**.

## Base legal ancorada — art. 263 CTB ✅ (3 hipóteses TAXATIVAS)
1. **I — dirigir com o direito de dirigir SUSPENSO** (flagrado conduzindo durante a suspensão vigente).
2. **II — reincidência, em 12 meses, nas infrações dos arts. 162 III · 163 · 164 · 165 · 173 · 174 · 175.** ⚠️ **grep cada artigo** no `context/` — só há cassação por II se a NOVA infração e a anterior estiverem **nesse rol** e dentro dos 12 meses. Fora do rol ou fora da janela = não cabe cassação (nulidade).
3. **III — condenação judicial por delito de trânsito** (efeito administrativo).

### Reabilitação — art. 263 §2º ✅
Decorridos **2 anos** da cassação, o interessado pode requerer a reabilitação, **submetendo-se a TODOS os exames** de habilitação (aptidão física/mental, avaliação psicológica, teórico e prático) — recomeça o processo do zero. Não é "renovação": é nova habilitação.

### Rito 🟡
Mesmo do processo de suspensão — **Res. 723/2018 (alt. 844/2021)**: instauração → notificação → defesa → JARI → 2ª instância. 🟡 prazos exatos *a confirmar*. Sem depósito prévio (SV 21 STF ✅).

## Teses de defesa (o que atacar)
- **Enquadramento fora das 3 hipóteses** → cassação é numerus clausus; se o fato não se subsume ao I/II/III, é nula.
- **Hipótese II — rol/janela**: a infração invocada não está no rol taxativo, ou não houve reincidência nos 12 meses, ou a "1ª" infração não é definitiva/foi anulada → cai o pressuposto.
- **Hipótese I — suspensão-base viciada**: se o processo de suspensão anterior era nulo/prescrito, a cassação por "dirigir suspenso" perde o alicerce (efeito cascata) → cross-link `processo-suspensao-direito-dirigir`.
- **Vício de notificação / cerceamento** (decisão-padrão) — Súmula 312 STJ ✅ + art. 5º LV CF.
- **Prescrição** da pretensão punitiva (Lei 9.873/99, ~5 anos — 🟡 a confirmar, sem repetitivo de trânsito).

## Passo a passo — o que produzir
1. **Enquadrar a hipótese** (I/II/III) e testar a taxatividade — grep os artigos.
2. **Auditar o pressuposto**: suspensão-base (I) válida? rol/janela (II) corretos? condenação (III) transitada?
3. **Defesa/recurso** no rito da 844/2021, atacando pressuposto + forma.
4. Persistindo o vício → judicial: `anulatoria-suspensao-cassacao` + `tutela-urgencia-transito`.
5. **Sem tese**: orientar honestamente sobre a reabilitação (2 anos + todos os exames) — planejar o retorno, não iludir.

## Postura honesta
- Cassação por hipótese I com suspensão-base válida e flagrante limpo é **difícil de reverter** — nesse caso o valor está em (a) checar vícios formais reais e (b) planejar a reabilitação. Não prometer anulação.
- "Reabilitar" NÃO é renovar: refaz-se **tudo**. Dizer o custo real ao cliente.

## Cross-link (soft)
Suspensão-base → `processo-suspensao-direito-dirigir`. Judicial → `anulatoria-suspensao-cassacao` + `mandado-de-seguranca-transito` + `tutela-urgencia-transito`. Crimes de trânsito (302-312, hipótese III) = **fora do escopo** deste plugin → `criminal`. Devolução/desbloqueio → `cnh-bloqueio-renovacao-reabilitacao`.

## Guard
As 3 hipóteses e o rol do inciso II saem **do `context/` via grep** — nunca de memória; a taxatividade é a espinha da defesa. Rito 723/2018 alt. 844/2021 e prazos = 🟡 confirmar no `validador-transito`. Peça fecha por `suprema-corte-transito`.

cassacao-da-cnh -> arts.: CTB 263 I/II/III + §2º (reabilitação 2 anos + todos os exames ✅); 162 III, 163, 164, 165, 173, 174, 175 (rol da reincidência ✅); Res. 723/2018 alt. 844/2021 (rito 🟡); Súmula 312 STJ (✅); SV 21 STF (✅); Lei 9.873/99 (prescrição 🟡).
