---
name: mandado-de-seguranca-transito
description: "Redige mandado de seguranca (Lei 12.016/09) contra ato de autoridade de transito quando ha direito liquido e certo e prova pre-constituida: bloqueio de CNH, recusa de renovacao, exigencia de multa NAO notificada para licenciar (Sumula 127 STJ), suspensao/cassacao com vicio de notificacao. Use quando o operador disser mandado de seguranca de transito, MS contra o DETRAN/DNIT, o Detran travou minha CNH/licenciamento, recusaram renovar minha habilitacao, estao exigindo multa que nao fui notificado, impetrar seguranca, ato ilegal da autoridade de transito."
---

# MANDADO-DE-SEGURANCA-TRANSITO — MS contra ato de autoridade

> Camada 6 (Judicial · standalone). Via rapida quando o direito e liquido e certo e a prova ja esta pronta (documental). Passa por `peticao-inicial-transito` para a esfera/competencia. Fecha por `suprema-corte-transito`.

## Anexos obrigatorios (context/)
- `context/jurisprudencia-transito.md` (**Sumula 127** e **Sumula 312** STJ, **SV 21** STF — so ✅).
- `context/ctb-9503-97.md` (arts. 159/281/282 — grep) + `context/processo-adm-fluxo-prazos.md` (dies a quo, SNE).
- Base: skill `base-processual-judicial-transito` (MS, Lei 12.016/09, tutela).

## Objetivo
Obter **liminar + seguranca** que destrave o ato ilegal (liberar CNH, obrigar a renovacao, afastar a exigencia de multa nao notificada), sem custo de deposito e com celeridade — quando cabe MS (direito liquido e certo, prova documental, ato de autoridade).

## Quando ativar (cabimento — Lei 12.016/09 art. 1)
Ha **ato/omissao ilegal de autoridade** + **direito liquido e certo** + **prova pre-constituida** (documental, sem dilacao). Casos tipicos:
- **Condicionar licenciamento/renovacao ao pagamento de multa NAO notificada** — **Sumula 127 STJ** (ilegal condicionar a renovacao da licenca ao pagamento de multa da qual o infrator nao foi notificado).
- **Bloqueio de CNH / recusa de renovacao** por processo viciado.
- **Suspensao/cassacao com vicio de notificacao** — **Sumula 312 STJ** (falta a NA ou a NP).
- **Autuacao por falta de porte (art. 232)** havendo CNH-e/CRLV-e com fe publica (art. 159, Lei 15.428/2026) — documento digital comprova o porte.

> Se o caso exige **produzir prova** (pericia, testemunha, controversia de fato), NAO e MS → `acao-anulatoria-multa-infracao` ou `anulatoria-suspensao-cassacao`.

## Regras estruturais do MS (nao errar)
- **Autoridade coatora = quem PRATICA o ato** (ex.: Diretor do DETRAN, Superintendente do DNIT), **nao** a hierarquicamente superior. Errar o coator gera extincao.
- **Pessoa juridica de direito publico** a que o coator se vincula e notificada para ingressar (art. 7, II).
- **Competencia pela esfera:** coator FEDERAL (DNIT/PRF) → Justica Federal; ESTADUAL (DETRAN/DER) → Justica Estadual. Se o coator for autoridade de alto escalao (ex.: Secretario de Estado), pode haver **competencia originaria do TJ/TRF** — checar a hierarquia do coator. 🟡 confirmar foro por prerrogativa do coator.
- **Prazo decadencial: 120 dias** da **ciencia** do ato coator (art. 23). Ato **omissivo/continuado** (bloqueio que persiste) renova a lesao — atencao ao dies a quo (SNE presume ciencia 30 dias apos inclusao).
- **Sem deposito previo / sem custas de garantia** — **SV 21 STF** veda condicionar recurso/impugnacao a deposito.

## Estrutura da peca
1. **Cabeca:** juizo competente (esfera do coator); impetrante; **autoridade coatora** (nome/cargo/endereco funcional) + pessoa juridica interessada.
2. **Fatos:** o ato ilegal + a prova documental que ja o demonstra (extrato RENACH, tela do sistema, NP sem NA, protocolo de renovacao negada).
3. **Direito liquido e certo:** Sumula 127/312 conforme o caso; ilegalidade/abuso de poder; art. 159 (CNH-e) se porte.
4. **Liminar (art. 7, III):** fumus (ilegalidade evidente pela sumula) + periculum (dano pela demora — CNH e instrumento de trabalho/locomocao; licenciamento vencendo). Pedir **suspensao do ato** ate o julgamento.
5. **Pedidos:** concessao da seguranca para anular/afastar o ato; determinar a liberacao/renovacao/licenciamento; oficio a autoridade. Honorarios NAO cabem em MS (art. 25) — advertir o cliente.

## Postura honesta
- **MS nao serve para tudo:** exige direito liquido e certo. Multa que depende de discutir enquadramento, pericia de radar ou versao dos fatos → nao e MS (risco de denegacao por necessidade de dilacao) → anulatoria.
- **Sumula 127** cobre multa **nao notificada**; se houve notificacao regular e o cliente so nao pagou, a exigencia pode ser legitima — nao vender MS onde nao cabe.
- **Prazo de 120 dias** e decadencial e nao se interrompe — se ja passou, migrar para acao ordinaria (anulatoria), que nao tem esse prazo.

## Entrega obrigatoria final
MS redigido (cabeca com coator correto + fatos + direito liquido e certo + pedido de liminar fundamentado + pedidos) + rol de documentos pre-constituidos + alerta do prazo de 120 dias e da inexistencia de honorarios.

## Guard
Nenhuma sumula/dispositivo/prazo sem `validador-transito`. Confirmar SEMPRE: (a) direito liquido e certo com prova documental; (b) coator correto (quem pratica o ato); (c) prazo de 120 dias. Entrega pela `suprema-corte-transito` (R1-R4). Cross-link, nao duplicar: caso com dilacao probatoria → `acao-anulatoria-multa-infracao`; suspensao/cassacao → `anulatoria-suspensao-cassacao`.
