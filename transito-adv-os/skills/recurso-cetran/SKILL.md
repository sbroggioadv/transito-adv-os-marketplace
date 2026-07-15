---
name: recurso-cetran
description: Redige o recurso ao CETRAN/CONTRANDIFE (2ª instância administrativa) contra a decisão da JARI, prazo de 30 dias, sem depósito prévio (SV 21). Use quando a JARI NEGOU o recurso do cliente, quando ele pergunta "a JARI negou, e agora?", "cabe recurso pra segunda instância?", "posso recorrer de novo da multa?", ou para esgotar a via administrativa antes de ir ao Judiciário.
---

# Recurso ao CETRAN / CONTRANDIFE (2ª instância)

## 1. Quando ativa
Ativa quando a **JARI negou** (total ou parcialmente) o recurso — é a **2ª e última instância administrativa**. Confirme a fase por `triagem-transito`: precisa existir uma **decisão da JARI** notificada ao cliente. Esgotar aqui é pré-requisito estratégico para segurar pontos ao máximo (art. 18 Res.918) e, se necessário, ir ao Judiciário (`acao-anulatoria-multa-infracao`).

Órgão competente:
- Multas **estaduais/municipais** → **CETRAN** do estado.
- Multas de órgão da **União** (ex.: PRF/DNIT) → **CONTRANDIFE** / colegiado especial.

## 2. Base legal ancorada
- **art. 288 CTB** — das decisões da JARI cabe recurso ao órgão de 2ª instância, prazo de **30 dias** da publicação/notificação da decisão.
- **art. 289 CTB** — o recurso de 2ª instância deve ser julgado em até **24 meses**; define os colegiados (União: colegiado especial; Estados/Municípios/DF: CETRAN e CONTRANDIFE).
- **SV 21 STF** — é **inconstitucional** exigir depósito prévio (ou arrolamento) como condição de admissibilidade de recurso administrativo. Combine com **art. 286 CTB** (recurso da multa sem recolhimento).
- **Res. CONTRAN 901/2022** — diretrizes de regimento/gestão dos CETRAN e CONTRANDIFE (2ª instância).
- Contagem em dias **corridos** (art. 29 Res.918).
- 🟡 **A confirmar no `validador-transito`:** número exato de dias e formalidades do recurso de 2ª instância na **Res. CONTRAN 900/2022** — o CTB fixa 30 dias (art. 288); confirme se a 900/2022 mantém e detalha antes de afirmar rito.

## 3. Passo a passo
1. **Tempestividade:** conte **30 dias corridos** da ciência da decisão da JARI.
2. **Ataque a decisão da JARI**, não só o AIT: aponte se a JARI usou decisão-padrão sem enfrentar os argumentos (cerceamento, art. 5º LV CF) — isso é tese própria da 2ª instância.
3. **Reforce as nulidades** de `analise-auto-de-infracao` que a JARI ignorou.
4. **Efeito suspensivo:** mantido enquanto pende (art. 18 Res.918) — reafirme que os pontos seguem fora do RENACH.
5. **Sem depósito:** se o órgão condicionar a admissão a qualquer pagamento, invoque SV 21 + art. 286.
6. **Endereçamento:** ao CETRAN (estadual) ou CONTRANDIFE (União), conforme o órgão autuador.

## 4. Estrutura da peça
- Endereçamento ao CETRAN/CONTRANDIFE + nº do processo/AIT + referência à decisão da JARI recorrida.
- Tempestividade (30 dias corridos, art. 288).
- Preliminar de nulidade da decisão da JARI (cerceamento/decisão-padrão), quando cabível.
- Mérito: reiteração e aprofundamento das teses.
- Pedidos: reforma da decisão da JARI + cancelamento da penalidade/pontos; manutenção do efeito suspensivo; dispensa de depósito (SV 21 + art. 286).

## 5. Postura honesta
Esgotar a via administrativa **não garante êxito** — muitas 2ª instâncias mantêm a JARI. O valor real é: (a) segurar pontos por mais tempo (art. 18 Res.918) e (b) **abrir a porta judicial** com a via administrativa esgotada. Diga isso ao cliente; não venda o CETRAN como decisão fácil de reverter.

## 6. Cross-link e fechamento
Decisão da JARI → `recurso-jari`; vícios → `analise-auto-de-infracao`; prazos → `notificacao-e-prazos`; após esgotar → `acao-anulatoria-multa-infracao` / `mandado-de-seguranca-transito` / `tutela-urgencia-transito`. **Fecha pela `suprema-corte-transito` (R1-R4)** + `validador-transito`.
