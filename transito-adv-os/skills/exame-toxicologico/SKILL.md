---
name: exame-toxicologico
description: Defesa das autuações do exame toxicológico dos motoristas profissionais C/D/E — infrações NOVAS criadas pela Lei 14.599/2023 (art. 165-B não realizar o exame do 148-A; art. 165-C resultado POSITIVO; art. 165-D não fazer após 30 dias do vencimento). Cobre a obrigatoriedade e a periodicidade do art. 148-A (novo exame a cada 2 anos e 6 meses para C/D/E com menos de 70 anos) e as teses de defesa. Use quando o cliente for categoria C/D/E e falar em "toxicológico vencido", "multa por toxicológico", "art. 165-B/C/D", "exame de cabelo/pelo deu positivo", "renovação com toxicológico", ou defesa dessas autuações.
---

# EXAME-TOXICOLOGICO

> Camada 3 (CNH). As infrações 165-B/C/D são NOVAS (Lei 14.599/2023) — muitos modelos não as têm consolidadas. Ponto sensível: **o multiplicador da multa é 🟡 a confirmar** antes de citar valor.

## Anexos obrigatórios (context/)
- `context/leis-14071-14599-15428.md` — **Lei 14.599/2023**: grep **art. 165-B, 165-C, 165-D** e **art. 148-A** (obrigatoriedade + periodicidade). 🟡 **Confirmar a natureza e o multiplicador exato** (referido como **5×** no 165-B; 10× na reincidência) — mudou recentemente, não afirmar sem validar.
- `context/ctb-9503-97.md` — art. 148-A (caput: C/D/E comprovam resultado negativo; §2º periodicidade).
- `context/metodologia-transito.md` — cadeia de custódia / janela de detecção do exame.

## Quando ativa
- Condutor **categoria C, D ou E** autuado por toxicológico.
- "**Toxicológico vencido**" / "esqueci de fazer" / "fiz depois do prazo".
- "**Deu positivo**" no exame (cabelo/pelo) e veio autuação.
- Renovação da CNH C/D/E travada por toxicológico.
- Defesa/recurso das autuações 165-B/C/D.

## Base legal ancorada
### Obrigatoriedade e periodicidade — art. 148-A CTB (Lei 14.599/2023) ✅
- **Caput:** condutores **C, D e E** devem comprovar resultado **NEGATIVO** em exame toxicológico para **obtenção e renovação** da CNH.
- **§2º:** os C/D/E **com menos de 70 anos** fazem **novo exame a cada 2 anos e 6 meses** (2,5 anos), a partir da obtenção/renovação, **independentemente** da validade dos demais exames. ✅

### As 3 infrações novas — Lei 14.599/2023 🟡 (multiplicador a confirmar)
- **Art. 165-B** — dirigir veículo **sem realizar** o exame periódico do 148-A: multa (**5×** 🟡); reincidência em 12 meses → multa (10×) + **suspensão** do direito de dirigir.
- **Art. 165-C** — dirigir tendo obtido **resultado POSITIVO** no toxicológico: **gravíssima**, multa (**5×** 🟡); reincidência em 12 meses → 10× + suspensão.
- **Art. 165-D** — deixar de realizar o exame **após 30 dias** do vencimento do prazo: **gravíssima**, multa (**5×** 🟡).

⚠️ 165-B/C/D são **infrações administrativas** deste plugin — não confundir com o crime do art. 306 (psicoativo ao volante), que fica **fora do escopo** (→ `criminal`).

## Teses de defesa (o que atacar)
1. **Prazo/escalonamento** — conferir se o cliente estava efetivamente **obrigado na data** (regra de transição/escalonamento do art. 7º p.ú. da Lei 14.599/2023; obrigados desde 03/09/2017 têm prazo definido pelo CONTRAN — 🟡 confirmar). Autuação antes do prazo exigível = indevida.
2. **Contagem da periodicidade** — os **2 anos e 6 meses** contam da obtenção/renovação; erro de marco (Detran contou de data errada) derruba a autuação.
3. **Resultado positivo (165-C)** — **cadeia de custódia** e **janela de detecção** do exame de queratina (cabelo/pelo): coleta, laboratório credenciado, contraprova; **resultado de substância com uso médico/prescrição** documentado; erro de identificação da amostra.
4. **Laudo** — ausência de laudo válido / laboratório não credenciado / divergência de dados.
5. **Nulidades gerais do AIT** (art. 280/281) e da **dupla notificação** (Súmula 312 STJ) → `analise-auto-de-infracao`.

## Passo a passo — o que produzir
1. **Confirmar categoria e obrigatoriedade** na data (C/D/E; escalonamento).
2. **Enquadrar** a autuação (165-B não fez / 165-C positivo / 165-D após 30 dias) — a tese muda por tipo.
3. **Requerer/juntar** laudo, cadeia de custódia, comprovante do exame, prescrição médica (se positivo por uso terapêutico).
4. **Redigir defesa/recurso** com prazo/contagem/laudo + nulidades do AIT.
5. Suspensão por reincidência → `processo-suspensao-direito-dirigir`. Renovação travada → `cnh-bloqueio-renovacao-reabilitacao`.

## Postura honesta
- **Positivo (165-C) com cadeia de custódia íntegra e sem prescrição médica** é difícil de reverter no mérito — o ataque real é procedimental (coleta/laboratório/janela) ou formal (AIT), não "o exame errou". Não prometer anulação.
- **Nunca afirmar o valor/multiplicador** (5×/10×) sem validar — é o ponto que mais mudou. Marcar 🟡 e rotear ao validador.

## Cross-link (soft)
Nulidades do auto → `analise-auto-de-infracao`. Suspensão derivada → `processo-suspensao-direito-dirigir`. Renovação C/D/E → `cnh-bloqueio-renovacao-reabilitacao`. Valor da multa → `enquadramento-e-multas-comuns`/`calculosjudiciais`. Crime 306 = fora do escopo → `criminal`.

## Guard
Periodicidade 2,5 anos (<70) e categorias C/D/E saem **do `context/` via grep** ✅; **multiplicador/natureza de 165-B/C/D e o escalonamento = 🟡 confirmar no `validador-transito`** antes de citar valor. Jurisprudência só se ✅. Peça fecha por `suprema-corte-transito`.

exame-toxicologico -> arts.: CTB 148-A (caput C/D/E + §2º periodicidade 2,5 anos ✅), 165-B / 165-C / 165-D (infrações novas ✅ existência; multiplicador 5×/10× 🟡); Lei 14.599/2023 (art. 7º p.ú. escalonamento 🟡); Súmula 312 STJ (✅). Fora do escopo: art. 306.
