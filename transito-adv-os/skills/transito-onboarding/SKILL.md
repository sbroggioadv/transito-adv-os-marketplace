---
name: transito-onboarding
description: "Wizard de configuracao do plugin transito ao perfil do escritorio. Cria a pasta transito/ com identidade (nome, OAB, escritorio, cidade, e-mail), areas de atuacao (defesa administrativa / judicial / ambas), tom e modo de fluxo. Usa context/metodologia-transito.md para explicar o que o plugin faz. Use quando o operador disser configurar transito, instalar transito, primeira vez, comecar, /start-transito, onboarding transito."
---

> **🖱️ Escolhas = botoes:** em campos de **lista fechada** (areas de atuacao, tom, modo de fluxo, atualizar/recriar, sim/nao) use a ferramenta **AskUserQuestion** para mostrar **botoes clicaveis** (max. 4 por pergunta; se houver mais, divida em 2). **Texto livre** (nome, OAB, escritorio, cidade, e-mail) segue como pergunta digitada normal.

# TRANSITO ONBOARDING

> Camada 0. Wizard de configuracao inicial. Linguagem acolhedora, sem jargao. Configura o plugin ao perfil do escritorio.

## Anexos obrigatorios (context/)
- `context/metodologia-transito.md` — para explicar o que o plugin faz (fluxo do processo, fases, trilhas) — **grep + ler a faixa**.

## Objetivo
Configurar o plugin ao escritorio em poucas perguntas e explicar, em linguagem simples, o que ele cobre: a defesa do condutor do auto de infracao ao recurso, passando por CNH (pontos/suspensao/cassacao), bafometro administrativo, pedagio/consumo e as acoes judiciais (anulatoria/MS) — sempre com a verdade vigente 2026.

## Quando ativar
`/start-transito` ou "configurar transito", "instalar transito", "primeira vez", "onboarding transito". Cria/atualiza `transito/perfil.md` no diretorio de trabalho.

## Regras do wizard
Uma pergunta por vez, acolhedor. Listas fechadas = AskUserQuestion (botoes). Texto livre = pergunta digitada. Ao fim, gravar e confirmar.

## Blocos de pergunta
1. **Identidade (texto livre):** nome, OAB (nº/UF), escritorio, cidade, e-mail.
2. **Areas de atuacao (botoes, multi):** Defesa administrativa (auto de infracao, JARI, CETRAN) · CNH (pontos/suspensao/cassacao/bafometro) · Pedagio & consumo · Judicial (anulatoria/MS/reparacao) · Tudo.
3. **Tom das pecas (botoes):** Tecnico-formal · Direto e objetivo · Combativo.
4. **Modo de fluxo (botoes):** Checkpoint (confirma a cada etapa) · Continuo.

## Explicacao do plugin (apresentar ao fim, em 4 frases)
- **O que cobre:** defende o condutor do **auto de infracao ao recurso** (defesa da autuacao -> JARI -> CETRAN), cuida da **CNH** (pontos 20/30/40, suspensao, cassacao, bafometro, toxicologico), **pedagio/free flow + cobranca indevida de tag** e as **acoes judiciais** (anulatoria, mandado de seguranca, reparacao).
- **A verdade vigente:** trabalha com a lei de 2026 (inclui a **Lei 15.428/2026** — CNH digital com fe publica) e as **Resolucoes CONTRAN consolidadas de 2022**, nunca com as revogadas — e conta prazo em **dias corridos** na esfera administrativa (onde muita gente perde o prazo).
- **Postura honesta:** ranqueia as nulidades (FORTE/MEDIA/FRACA), desmente o mito da "falta de assinatura" e nunca promete "anular qualquer multa".
- **Como usar:** depois daqui, basta falar o que precisa — a porta unica (`transito-master` -> `triagem-transito`) cuida do roteamento; a 1ª pergunta sera sempre "voce recebeu a Notificacao da Autuacao ou da Penalidade?".

## Gravacao
Criar `transito/perfil.md`. Se ja existir, perguntar (botoes) Atualizar ou Recriar.

## Entrega obrigatoria final
- `transito/perfil.md` + resumo da configuracao + sugestao do primeiro comando (`/triagem` ou `/transito-master`).

## Guard
Nao inventar dados do operador. As areas de atuacao sao preferencia, nao trava: a `triagem-transito` roteia qualquer caso que chegar, independentemente do que foi marcado aqui.
