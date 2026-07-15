---
name: peticao-inicial-transito
description: "Matriz da peticao inicial de acao judicial de transito: fixa a COMPETENCIA (Justica Estadual x Federal conforme o orgao autuador), o valor da causa (CPC 292) e os requisitos do art. 319 CPC, e roteia para a acao certa (anulatoria, MS, reparatoria). Use quando o operador for ao Judiciario contra multa/penalidade de transito e disser peticao inicial, vou ajuizar, propor acao contra o DETRAN/DNIT/DER, acao judicial de transito, entrar na justica contra a multa, qual a vara/competencia, contra quem processo, ou descrever caso novo que ja esgotou (ou vai pular) a via administrativa."
---

# PETICAO-INICIAL-TRANSITO — matriz da acao judicial

> Camada 6 (Judicial · standalone). Porta de entrada de TODA acao de transito no Judiciario. Fixa competencia + polo passivo + valor + requisitos ANTES de escolher a peca. Fecha por `suprema-corte-transito`.

## Anexos obrigatorios (context/)
- `context/metodologia-transito.md` (regras de ouro, via adm x judicial).
- `context/ctb-9503-97.md` (dispositivo autuador — grep do artigo) + `context/jurisprudencia-transito.md` (so ✅).
- Base processual: skill `base-processual-judicial-transito` (CPC filtrado — competencia, valor, tutela).

## Objetivo
Montar a cabeca da inicial sem erro estrutural: **vara/juizo correto**, **reu correto**, **valor da causa correto** e **art. 319 completo** — evitando emenda (321), indeferimento (330) e, pior, extincao por incompetencia absoluta.

## Quando ativar
- Cliente vai ao Judiciario (anulatoria, MS, reparatoria) contra multa/infracao/penalidade de transito.
- Duvida de competencia (Estadual x Federal), de quem colocar no polo passivo, ou de valor da causa.

## 1. COMPETENCIA — pela ESFERA do orgao autuador (CF art. 109, I)
A regra decisiva: **quem autuou/aplicou a penalidade define a Justica.**

| Orgao autuador | Natureza | Justica | Onde ajuizar |
|---|---|---|---|
| **DNIT** (rodovias federais) · **PRF** | autarquia/orgao FEDERAL | **Justica FEDERAL** | Vara Federal (CF 109, I — autarquia federal no polo) |
| **DETRAN** estadual · **DER** estadual · PM/PRE estadual | autarquia/orgao ESTADUAL | **Justica ESTADUAL** | Vara da Fazenda Publica Estadual |
| **Agente/guarda municipal**, autarquia municipal de transito (ex. orgao de mobilidade) | MUNICIPAL | **Justica ESTADUAL** | Vara da Fazenda Publica Municipal |

- **Polo passivo = a pessoa juridica** a que o orgao pertence: **Uniao/DNIT** (federal), **Estado ou autarquia estadual DETRAN/DER** (estadual), **Municipio** (municipal). O agente pessoa fisica NAO e reu na anulatoria/reparatoria (no MS, o coator e a autoridade — ver `mandado-de-seguranca-transito`).
- **Free flow / pedagio (art. 209-A):** a autuacao e do orgao viario (federal DNIT ou estadual DER) → segue a tabela. **Cobranca indevida de tag** (Sem Parar/ConectCar) e relacao de CONSUMO contra a operadora privada → **Justica Estadual comum** (ver `tag-e-cobranca-indevida`).

## 2. VALOR DA CAUSA — CPC 292
- **Anular multa/penalidade:** valor = **valor da multa discutida** (CPC 292, II/V — anulacao de ato de conteudo economico). Somar multiplicador ja conferido no tipo.
- **Reparacao (dano material/moral):** valor pretendido (292, V/VI) — quantum via `acao-reparatoria-transito` + `calculosjudiciais`.
- **MS / puramente declaratorio (destravar CNH/licenciamento sem multa quantificada):** valor estimado do proveito ou simbolico — atencao ao teto do JEC/JEF (ver abaixo).
- **Rito:** valor ate 60 salarios minimos contra Fazenda pode ir ao **Juizado Especial da Fazenda Publica** (Lei 12.153/09, estadual) ou **JEF** (Lei 10.259/01, federal) — sem advogado obrigatorio ate certo limite, mas confirmar conveniencia (perde reexame, mas ganha celeridade). 🟡 confirmar teto/vedacoes do JEF-JEFP.

## 3. REQUISITOS — art. 319 CPC (I a VII)
1. Juizo (a vara certa da tabela §1).
2. Qualificacao completa autor + reu (o ENTE, com CNPJ; endereco para citacao pela procuradoria).
3. Fatos + fundamentos juridicos (causa de pedir): o AIT/processo adm + o vicio (nulidade do AIT, dupla notificacao Sumula 312, prazo, cerceamento) — detalhe na acao especifica.
4. Pedido certo e determinado (324): anular AIT X / suspender penalidade / destravar CNH / condenar em reparacao.
5. Valor da causa (§2 acima).
6. Provas (docs indispensaveis, 320): AIT, NA, NP, extrato RENACH/prontuario, comprovantes.
7. Opcao pela audiencia 334 (contra Fazenda geralmente dispensavel — nao ha autocomposicao usual; pode pedir para nao designar).

## 4. Gestao processual transversal (checar SEMPRE antes de redigir)
- **Gratuidade** (CPC 98) se hipossuficiente.
- **Prazo em dobro da Fazenda** (CPC 183) — impacta a estrategia, nao a inicial.
- **Reexame necessario** (CPC 496) se a sentenca for contra a Fazenda acima do limite — orientar o cliente sobre o tempo.
- **Tutela de urgencia** desde a inicial se ha perigo (CNH bloqueada, veiculo apreendido, licenciamento travado) → cross-link `tutela-urgencia-transito` (CPC 300).

## Roteamento para a peca
Fixada a matriz, encaminhar:
- vicio do AIT/processo de multa → `acao-anulatoria-multa-infracao`;
- ato ilegal de autoridade (bloqueio CNH, recusa de renovacao, condicionar licenciamento a multa nao notificada) com direito liquido e certo → `mandado-de-seguranca-transito`;
- suspensao/cassacao viciada → `anulatoria-suspensao-cassacao`;
- dano (pedagio/concessionaria/cobranca/negativacao) → `acao-reparatoria-transito`.

## Postura honesta
- **A via judicial nao substitui a administrativa por padrao:** onde ainda cabe defesa/JARI/CETRAN (com efeito suspensivo e sem custo), muitas vezes vale esgotar primeiro (art. 18 Res.918 segura os pontos). Judicializar cedo pode ser mais caro e sem tutela garantida — decisao informada via `parecer-transito`.
- **Sumula 434 STJ:** o pagamento da multa **nao inibe** a discussao judicial — pode ajuizar mesmo se ja pagou (devolucao corrigida se procedente, CTB 286 §2). NAO citar Sumula 434 como "defesa previa" (isso e Sumula 312 + CTB 281).

## Entrega obrigatoria final
Cabeca da inicial (juizo/vara + partes) + valor da causa fundamentado + rol de documentos (art. 320) + indicacao da acao correta a redigir + alerta de tutela se houver perigo.

## Guard
Nenhum dispositivo/sumula/resolucao/prazo sem `validador-transito`. Competencia SEMPRE pela esfera do orgao autuador (CF 109, I). Nao redigir sem fixar reu e valor. Entrega pela `suprema-corte-transito` (R1-R4). Cross-link, nao duplicar: processual pesado → `civel-adv-os`; execucao fiscal da multa em divida ativa → `execucao-adv-os`; IPVA → `tributario`.
