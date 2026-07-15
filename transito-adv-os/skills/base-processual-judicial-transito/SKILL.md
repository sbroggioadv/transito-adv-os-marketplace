---
name: base-processual-judicial-transito
description: "Espinha PROCESSUAL da via judicial de transito, STANDALONE (nao depende do plugin civel instalado): matriz da acao anulatoria de multa/penalidade, do mandado de seguranca (Lei 12.016/2009) contra ato da autoridade de transito, das tutelas de urgencia (CPC 300), da competencia (Justica Estadual x Federal conforme o orgao autuador) e do valor da causa. Entrega o esqueleto processual correto e vigente para as skills de peca judicial. Use quando a via administrativa se esgotou ou ha ilegalidade a atacar no Judiciario, para decidir anulatoria x MS, definir competencia/foro, calcular valor da causa, fundamentar tutela de urgencia, ou quando o operador disser vou pra Justica, cabe mandado de seguranca?, qual a competencia, onde protocolo, qual o valor da causa da anulatoria."
---

# BASE-PROCESSUAL-JUDICIAL-TRANSITO — Esqueleto da via judicial (standalone)

> Camada 1 (Fundacao). Modela o processual civil aplicado ao transito SEM exigir o plugin civel. Nao redige peca: entrega via, competencia, valor da causa e tutela corretos. Se o `civel` estiver instalado, aprofunda por cross-link — mas funciona sozinho.

## Anexos obrigatorios (context/)
- `context/metodologia-transito.md` — voz/metodo; quando chamada pelo `transito-master`.
- `context/processo-adm-fluxo-prazos.md` — para saber se a via administrativa foi esgotada / prazos que impactam o dies a quo judicial.

## Objetivo
Devolver, para levar o caso ao Judiciario: **qual acao** (anulatoria x MS x reparatoria), **competencia** (Estadual x Federal), **foro**, **valor da causa** e **cabimento/fundamento da tutela** — sem inventar dispositivo nem prometer resultado.

## Quando ativar
- A via administrativa acabou (recurso ao CETRAN negado) ou ha ato ilegal a atacar ja (bloqueio de CNH, licenciamento condicionado a multa nao notificada).
- Escolher entre **anulatoria** (dilacao probatoria, discute o merito/nulidade do AIT e do processo adm) e **mandado de seguranca** (direito liquido e certo, prova pre-constituida, ato de autoridade).
- Definir competencia/foro, valor da causa ou fundamentar pedido de tutela.

## Matriz de decisao (ancorado — dispositivos estaveis; confirmar nº no validador)
### 1. Qual acao
- **Acao anulatoria** (procedimento comum, CPC): quando precisa **provar** vicio do AIT / do processo administrativo (pericia, testemunha, alibi de local/data). Pedido: anular a autuacao/penalidade + baixa de pontos + repeticao do indebito se pago (Sumula 434 STJ — pagamento nao inibe a discussao).
- **Mandado de seguranca (Lei 12.016/2009):** ato de autoridade de transito com **ilegalidade/abuso** e **direito liquido e certo** (prova documental pronta). Tipicos: bloqueio/recusa de renovacao de CNH; **exigir multa nao notificada para licenciar (Sumula 127 STJ)**; suspensao/cassacao com vicio de notificacao (Sumula 312) ou prescrita.
  - **Prazo decadencial: 120 dias** da ciencia do ato coator (Lei 12.016/2009, art. 23).
  - **Coator = quem PRATICA o ato** (ex.: Diretor do DETRAN), nao o superior hierarquico. Erro de coator = extincao.
  - Liminar: art. 7º III (fumus + periculum).
- **Reparatoria/indenizatoria:** dano por pedagio/concessionaria/cobranca indevida ou negativacao (cross-link Camada 4 + `calculosjudiciais`).

### 2. Competencia (a pegadinha do transito)
- **Justica ESTADUAL** — regra: orgao autuador **estadual ou municipal** (DETRAN estadual, orgao de transito do municipio, guarda municipal).
- **Justica FEDERAL** — quando o orgao autuador/coator e **autarquia/orgao FEDERAL** (ex.: **DNIT**, **PRF** em rodovia federal): art. 109, I/VIII, CF (causa contra autarquia federal). Definir o orgao ANTES de escolher a Justica.
- Foro (Estadual): domicilio do autor ou do reu ente publico, conforme a acao; MS = sede da autoridade coatora.

### 3. Valor da causa
- Anulatoria de multa: valor da(s) multa(s) impugnada(s) / proveito economico (baixa de pontos + liberacao). Reparatoria: valor do dano + moral pretendido. Requisito da inicial (CPC 319).

### 4. Tutela de urgencia (CPC 300)
- Requisitos: **probabilidade do direito** + **perigo de dano/risco ao resultado util**. Aplicacoes: liberar CNH bloqueada, suspender lancamento de pontos/penalidade, destravar licenciamento/veiculo. Reversibilidade (§3º). MS usa a **liminar** propria (Lei 12.016/09 art. 7º III), nao a tutela do CPC.

## 🟡 PROIBIDO afirmar sem confirmar (-> `validador-transito`)
Numero exato de dispositivo do CPC/Lei 12.016 quando a peca vai cita-lo (confirmar a redacao vigente); competencia federal quando o orgao nao esta claramente identificado como federal — checar quem lavrou o AIT.

## Postura honesta
Anulatoria e MS nao sao intercambiaveis: MS exige direito **liquido e certo** (sem dilacao probatoria) — se o vicio depende de pericia, e anulatoria. Esgotamento da via administrativa nao e, em regra, condicao para o Judiciario (inafastabilidade, CF 5º XXXV), mas pesa na tutela. Nunca prometer liminar.

## Cross-link soft (nao duplicar)
Nulidade do AIT / vicio do processo adm (o merito) -> Camada 2 + `analise-auto-de-infracao`. Precedente (127/312/434, SV 21) -> `jurisprudencia-transito`. Peca pronta -> skills da Camada 6. Processual civil aprofundado (se instalado) -> `civel` (nao depender dele). Dano/calculo -> `calculosjudiciais`.

## Guard
Nenhuma competencia/valor/dispositivo entregue sem checar o orgao autuador (Estadual x Federal) e sem confirmar redacao/numero no `validador-transito` quando for para peca. MS: conferir coator + prazo de 120 dias. Peca fecha pela `suprema-corte-transito` (R4 forma/competencia/via).
