---
name: jurisprudencia-transito
description: "Busca de precedente de transito (STJ/STF) para fundamentar peca, recurso ou parecer: primeiro no corpus mapeado em context/jurisprudencia-transito.md (por tema, com selo de verificacao), e so se faltar busca ao vivo (WebSearch/WebFetch nativo; Firecrawl/Perplexity fallback) exigindo link de fonte oficial real. Zero acordao/sumula/tema inventado. Guarda as ancoras Sumula 312/127/434/585, SV 21, Tema 1.122 e as CORRECOES travadas (Sumula 434 NAO e defesa previa; Tema 1.293 e ADUANEIRO nao transito; Tema 1.122 so animal domestico). Use quando precisar de sumula, tema repetitivo, acordao ou tese de transito, ou quando o operador disser tem jurisprudencia sobre X, qual a sumula sobre notificacao/renovacao/pagamento, precedente para a nulidade do AIT, acha um acordao do STJ sobre transito."
---

# JURISPRUDENCIA-TRANSITO — Precedente de transito verificado

> Camada 1 (Fundacao). Entrega precedente cujo existir e teor foram confirmados. Trabalha colada ao `validador-transito` e ao guard `anti-alucinacao-transito` (+ guard global `anti-alucinacao-juridica`).

## Anexos obrigatorios (context/)
- `context/jurisprudencia-transito.md` — corpus por tema, com selo: **✅** (fonte primaria oficial aberta — citar) · **🟡** (secundaria confiavel / entendimento sem sumula — conferir inteiro teor antes de citar) · **🔴/NAO CONFIRMADO** (nunca citar).
- `context/metodologia-transito.md` — quando chamada pelo `transito-master`.

## Objetivo
Devolver precedente de transito **real, pertinente e citavel** com fonte verificavel, ou declarar honestamente que nao foi encontrado — nunca preencher a lacuna com acordao/sumula/tema inventado.

## Quando ativar
- Uma skill de peca/recurso/parecer precisa de respaldo jurisprudencial.
- O operador pede sumula, tema, leading case ou tese sobre notificacao, renovacao, pagamento, concessionaria, bafometro.
- Ha duvida se um precedente existe, esta vigente ou se aplica ao caso.

## Ancoras ✅ (verificadas em fonte oficial — pode citar; teor no anexo)
- **Sumula 312 STJ** — *"No processo administrativo para imposicao de multa de transito, sao necessarias as notificacoes da autuacao E da aplicacao da pena."* (1ª Secao, 11/05/2005). **Espinha da nulidade do AIT** — falta de qualquer das duas notificacoes anula.
- **Sumula 127 STJ** — *"E ilegal condicionar a renovacao da licenca de veiculo ao pagamento de multa, da qual o infrator nao foi notificado."* Base do MS contra DETRAN.
- **Sumula 434 STJ** — *"O pagamento da multa por infracao de transito nao inibe a discussao judicial do debito."* (1ª Secao, 24/03/2010). Se a penalidade cai, a Administracao devolve com correcao (CTB 286 §2º).
- **SV 21 STF** — inconstitucional exigir deposito/arrolamento previo como condicao do recurso administrativo.
- **Tema 1.122 STJ** — *concessionaria de rodovia responde OBJETIVAMENTE por danos de acidente com **animal DOMESTICO** na pista* (CDC + Lei 8.987/95). REsp 1.908.738/SP, merito 21/08/2024.
- **Sumula 585 STJ** — comunicacao de venda / responsabilidade do antigo proprietario (usar via `context/`; teor+aplicacao no anexo).
- **Art. 277 §3º CTB (recusa ao bafometro):** teor consolidado (STJ Inf. 612) — a recusa e infracao **AUTONOMA**, nao presume embriaguez e nao viola nemo tenetur na esfera adm. ✅ teor; nº do REsp-lider 🟡 (nao pinar sem confirmar).

## 🔴 CORRECOES travadas (nunca repetir o erro — sao trava anti-alucinacao)
1. **Sumula 434 STJ != "defesa previa".** 434 e **pagamento x discussao judicial**. Defesa previa ancora em **Sumula 312 + CTB art. 281** (+ CF 5º LV), NAO em uma "sumula 434 da defesa previa".
2. **Tema 1.293 STJ e ADUANEIRO, nao transito.** Nunca cita-lo como prescricao intercorrente de transito (o slug da noticia induz ao erro).
3. **Tema 1.122 so animal DOMESTICO.** Nao estender a **silvestre** (fauna nativa) — ai a discussao migra para responsabilidade do **Estado/orgao ambiental**. Nao vender como "qualquer animal".

## 🟡 Usar com ressalva (sem sumula/tema numerado — nao inventar numero)
- **Notificacao postal dispensa AR**, mas exige prova do **envio** — tese **pro-Administracao** (limita a nulidade por "nao recebi"). Nao citar como "Tema X" sem confirmar o numero.
- **Prescricao 5 anos** da pretensao punitiva por analogia a **Lei 9.873/1999** — jurisprudencia majoritaria, **sem sumula**. Citar como "por analogia", nao como sumula.
- **Prescricao intercorrente em transito** (processo parado > 3 anos, Lei 9.873/99 art. 1º §1º): campo **em construcao**, bom argumento, sem repetitivo/sumula de transito — avisar a divergencia.
- **CTB art. 281 §u II** (NA em 30 dias ou arquivamento): teor legal ✅; a consequencia de arquivamento e pacifica, mas sem tema numerado do STJ.

## Metodologia
1. **Corpus primeiro:** `grep -niE "notificacao|renovacao|pagamento|concessionaria|prescricao|bafometro" context/jurisprudencia-transito.md` e ler a faixa. ✅ -> citar. 🟡 -> conferir inteiro teor ao vivo antes. 🔴/racha -> nao citar; avisar a divergencia.
2. **Busca ao vivo (so se faltar no corpus ou 🟡):** `WebSearch`/`WebFetch` nativos; Firecrawl/Perplexity fallback. Fonte oficial: stj.jus.br, portal.stf.jus.br. Exigir **link real aberto** confirmando numero + teor.
3. **Validar antes de devolver:** `validador-transito` — orgao + numero + tese + data conferem e a fonte abre com o trecho? Sem isso, marcar NAO VERIFICADO e nao usar.
4. **Pertinencia:** distinguishing (o caso se encaixa?) + vinculacao (repetitivo/RG/SV — CPC 927).

## Entrega obrigatoria final
Tabela: orgao/numero · tese (1-2 linhas) · selo (✅ corpus / ✅ ao vivo) · link · pertinencia · vinculacao. Bloco de citacao pronto so para itens verificados. Nao confirmados ficam listados como "nao localizado".

## Guard
Zero acordao/sumula/tema inventado. So entra em peca o **✅** do corpus ou o confirmado ao vivo com link aberto. 🟡 sem conferencia e 🔴 NUNCA. Integra `validador-transito` + guards `anti-alucinacao-transito` / `anti-alucinacao-juridica`; gate final `suprema-corte-transito` (R3). Na duvida, remover e checar.
