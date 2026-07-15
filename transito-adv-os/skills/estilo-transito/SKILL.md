---
name: estilo-transito
description: "Define a voz, a estrutura e o enderecamento das pecas do plugin (defesa da autuacao, recurso JARI/CETRAN, anulatoria, MS, recursos) e carrega o CHECKLIST ANTI-DESATUALIZACAO que impede o folclore de balcao: CONTRAN vigente (918/900/931/901, nunca as revogadas), art. 271 nao 262, pontuacao 20/30/40, prazo adm em dias CORRIDOS x judicial em dias UTEIS, Lei 15.428/2026 (CNH-e). Use sempre que outra skill for redigir uma peca de transito, para garantir tom correto, enderecamento certo (orgao adm x juizo) e terminologia vigente. Acionada internamente pelas skills de redacao."
---

# ESTILO-TRANSITO

> Tier 0 / transversal. Camada de estilo — consultada pelas skills de redacao **antes** de entregar a peca. Garante que nenhuma peca saia com dispositivo revogado ou prazo errado.

## Anexos / skills-fonte
- `context/metodologia-transito.md` (terminologia e regras de ouro).
- `resolucoes-contran-mapa.md` (vigentes × revogadas) — conferir antes de citar resolucao.

## ✅ CHECKLIST ANTI-DESATUALIZACAO (rodar em TODA peca, antes de entregar)
1. **Resolucao CONTRAN vigente?** Notificacao = **918/2022** · defesa+recurso JARI/CETRAN = **900/2022** · SNE = **931/2022** · CETRAN = **901/2022** · suspensao/cassacao = **723/2018 alt. 844/2021**. 🔴 **NUNCA** 619/2016, 299/2008, 692/2017, 622/2016 (revogadas).
2. **Remocao/leilao:** remocao ao deposito = **art. 271** · leilao = **art. 328**. 🔴 **art. 262 REVOGADO** (Lei 13.281/2016) — nao citar.
3. **Pontuacao:** **20/30/40** conforme nº de gravissimas em 12 meses (art. 261, Lei 14.071/2020, desde 12/04/2021); EAR = **40 fixo**. 🔴 Nao escrever "20 pontos e perde a CNH".
4. **Prazo — qual esfera?** Administrativo = dias **CORRIDOS** (art. 29 Res.918). Judicial = dias **UTEIS** (CPC 219). Declarar a esfera e nao trocar o regime.
5. **CNH-e:** **Lei 15.428/2026** — CNH fisica OU digital com fe publica (art. 159) + renovacao automatica RNPC (268-A §7º). Reforca tese contra autuacao por "falta de porte" (art. 232) quando havia CNH digital.
6. **NA ≠ NP:** notificacao da **autuacao** e a da **penalidade** sao fases distintas — a peca tem de dizer a qual responde.
7. **Correcoes travadas:** Sumula 434 ≠ defesa previa (e pagamento × discussao; defesa previa = Sumula 312) · Tema 1.293 e **aduaneiro**, nao transito · "CNH sem autoescola" = proposta, nao vigente.
8. **Mito desmentido:** "falta de assinatura do condutor/infrator anula" e tese **FRACA** (art. 280 pede so "quando possivel") — nao ancorar defesa nisso. Nao confundir com a falta de identificacao do AGENTE, que e tese FORTE.

## Enderecamento correto (nao confundir esfera)
- **Defesa da autuacao / recurso JARI** -> autoridade de transito que autuou/aplicou (adm).
- **Recurso CETRAN/CONTRANDIFE** -> 2ª instancia adm (30 dias, SV 21 sem deposito).
- **Anulatoria / reparatoria** -> Juizo competente (Justica Estadual, ou Federal se orgao federal — ex.: PRF/DNIT).
- **MS** -> Juizo competente contra a **autoridade coatora** (Lei 12.016/09).
- **Recursos judiciais** -> orgao ad quem correto (apelacao ao tribunal; REsp/RE ao presidente/vice da origem).

## Estrutura padrao por tipo
- **Defesa/recurso administrativo:** enderecamento ao orgao + qualificacao + fase/AIT + fundamentos (nulidades ranqueadas + dispositivo/resolucao vigente) + pedido (insubsistencia do AIT / provimento) + requerimento de efeito suspensivo (JARI, art. 285).
- **Peticao inicial judicial (CPC 319):** juizo competente + partes + fatos + fundamentos + pedido (com tutela de urgencia se cabivel) + valor da causa + provas.
- **Recurso judicial:** enderecamento + tempestividade (dias uteis) + preparo/gratuidade + razoes + pedido.

## Tom
Tecnico, objetivo, assertivo. **Sem promessa de resultado** (Codigo de Etica OAB). Nulidade apresentada pela forca real (FORTE/MEDIA/FRACA), nunca inflada. Citacoes so via `validador-transito`.

## Guard
Toda citacao legal/jurisprudencial/resolucao passa por `validador-transito`. Antes de entregar, `suprema-corte-transito` (R4 cuida de forma/competencia/via adm × judicial). Este checklist e obrigatorio — peca que falha em qualquer item volta para correcao.
