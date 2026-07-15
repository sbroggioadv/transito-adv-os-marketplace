---
name: bafometro-e-recusa-administrativa
description: Defesa ADMINISTRATIVA da autuação por embriaguez (art. 165) e por RECUSA ao teste (art. 165-A / art. 277 §3º) — a recusa é infração AUTÔNOMA, penalidade idêntica à do 165, e não presume embriaguez. Monta a defesa técnica (aferição INMETRO do etilômetro, margem de erro, cadeia de custódia, sinais genéricos insuficientes — Res. CONTRAN 432/2013 + art. 277). SEM o crime do art. 306 (fora do escopo — cross-link criminal). Use quando o cliente foi autuado por "bafômetro", "embriaguez", "recusa ao teste", "art. 165/165-A", "Lei Seca administrativa", "soprou/não soprou", ou defesa/recurso dessas autuações.
---

# BAFOMETRO-E-RECUSA-ADMINISTRATIVA

> Camada 3 (CNH). **Escopo travado: só ADMINISTRATIVO** (autuação/suspensão/recusa/defesa). O crime do art. 306 fica FORA deste plugin (→ `criminal`). Aqui defende-se a multa gravíssima + a suspensão de 12 meses.

## Anexos obrigatórios (context/)
- `context/ctb-9503-97.md` — **grep art. 165, 165-A e 277** (§§; meios de prova). Ler a penalidade (multa 10× + suspensão 12 meses) e a forma de constatação.
- `context/jurisprudencia-transito.md` — **recusa = infração autônoma do art. 277 §3º / art. 165-A** (STJ: não presume embriaguez, não viola nemo tenetur na esfera adm.) ✅.
- `context/leis-14071-14599-15428.md` — art. 165-A criado/estruturado (Lei 13.281/2016).
- `context/metodologia-transito.md` — checklist de prova do etilômetro. 🟡 **nº e periodicidade da portaria INMETRO do etilômetro = a confirmar** antes de citar.

## Quando ativa
- Autuação por **art. 165** (dirigir sob influência de álcool/psicoativo).
- Autuação por **art. 165-A** (recusar-se ao teste/exame/perícia, na forma do art. 277).
- Cliente "**soprou e deu**", "**me recusei a soprar**", "só fizeram teste de sinais".
- Defesa da autuação, recurso à JARI/2ª instância, ou processo de suspensão derivado.

## Base legal ancorada
### Embriaguez — art. 165 CTB ✅
Infração **gravíssima**, multa **10×** (dobrável na reincidência em 12 meses) + **suspensão do direito de dirigir por 12 meses** + medida administrativa (retenção/recolhimento da CNH).

### Recusa — art. 165-A / art. 277 §3º CTB ✅ (infração AUTÔNOMA)
Recusar-se ao teste do etilômetro/exame é infração **autônoma**, com penalidade **idêntica** à do 165 (gravíssima, 10×, suspensão 12 meses). A jurisprudência (STJ) é clara: **a recusa não se confunde com a embriaguez, não a presume, e a sanção dispensa a prova do álcool** — pune-se o descumprimento do dever de submeter-se ao procedimento; **não viola nemo tenetur** na esfera administrativa. ✅ ⇒ na recusa, alegar "não estava bêbado" é irrelevante para a infração — a tese muda de eixo (atacar a validade da abordagem/notificação, não a embriaguez).

### Meios de constatação — art. 277 + Res. CONTRAN 432/2013 ✅
Etilômetro, exame de sangue/laboratorial, exame clínico, **sinais de alteração da capacidade psicomotora**, vídeo/fotos, testemunhas.

## Defesa técnica (o que requerer/atacar)
1. **Aferição do etilômetro pelo INMETRO** — exigir na defesa que o órgão junte o **certificado de aprovação + verificação metrológica vigente na data** do teste (🟡 portaria INMETRO/periodicidade *a confirmar*). Órgão não junta → combinar com **cerceamento de defesa**.
2. **Margem de erro** — valores **próximos ao limite**, descontada a incerteza metrológica, podem não atingir o patamar sancionador (🟡 aplicar o valor de erro conforme a norma metrológica).
3. **Cadeia de custódia** — divergência de **hora/local/nº de série** entre o AIT e o termo do teste; identificação do agente.
4. **Sinais genéricos insuficientes** — termo que só diz "embriagado" **sem descrever sintomas concretos** (fala arrastada, odor etílico, desequilíbrio) = insuficiência probatória; falta de assinatura do agente no termo.
5. **Vídeo/imagens** que contrariem os sinais alegados.
6. **Nulidades gerais do AIT** (art. 280/281) e da **dupla notificação** (Súmula 312 STJ) → `analise-auto-de-infracao`.

## Passo a passo — o que produzir
1. **Triar a autuação**: é 165 (teste positivo / clínico / sinais) ou 165-A (recusa)? A tese muda.
2. **Requerer os documentos** (certificado INMETRO, termo de constatação, vídeo) já na defesa.
3. **Redigir a defesa/recurso** com as teses aplicáveis + nulidades do AIT.
4. Suspensão derivada de 12 meses → `processo-suspensao-direito-dirigir`.
5. Persistindo → judicial: `acao-anulatoria-multa-infracao` + `tutela-urgencia-transito`.

## Postura honesta
- **Recusa (165-A) com abordagem regular é difícil de derrubar** — a autonomia da infração é jurisprudência firme; não vender "recusa não dá em nada". O ataque real é procedimental (validade da ordem/notificação/termo), não "não estava bêbado".
- Etilômetro **com aferição vigente e valor bem acima do limite** deixa a margem de erro frágil — nesse caso priorizar cadeia de custódia e sinais, sem prometer anulação.
- ⚠️ Se houver **também** ação penal (art. 306), avisar o cliente e remeter a `criminal` — este plugin **não** cobre o crime.

## Cross-link (soft)
Nulidades do auto → `analise-auto-de-infracao`. Suspensão → `processo-suspensao-direito-dirigir`. Judicial → `acao-anulatoria-multa-infracao` + `tutela-urgencia-transito`. **Crime art. 306 → `criminal` (fora do escopo).**

## Guard
Autonomia da recusa (277 §3º/165-A) e penalidade (10× + 12 meses) saem **do `context/` via grep** + jurisprudência só se ✅. **Portaria INMETRO e margem de erro = 🟡 a confirmar no `validador-transito`** — nunca citar número de portaria de memória. Não tratar o crime do 306. Peça fecha por `suprema-corte-transito`.

bafometro-e-recusa-administrativa -> arts.: CTB 165 (gravíssima, 10×, suspensão 12m ✅), 165-A / 277 §3º (recusa autônoma ✅ — STJ não presume embriaguez), 277 (meios de prova ✅); Res. CONTRAN 432/2013 (etilômetro ✅; portaria INMETRO 🟡); Súmula 312 STJ (✅). Fora do escopo: CP/CTB art. 306.
