---
name: acao-reparatoria-transito
description: "Redige acao de reparacao de danos (material e moral) ligados a transito: dano por defeito de conservacao/animal na pista sob concessao (responsabilidade objetiva, Tema 1.122 STJ + CDC), cobranca indevida de tag/pedagio (devolucao em dobro art. 42 CDC), negativacao indevida por multa/cobranca. Use quando o operador disser acao de indenizacao de transito, danos na estrada por buraco/animal, processar a concessionaria de rodovia, cobranca indevida da tag/pedagio, negativaram meu nome por multa, quero devolucao em dobro, ou reparar prejuizo material/moral ligado a transito."
---

# ACAO-REPARATORIA-TRANSITO — indenizacao no dominio do transito

> Camada 6 (Judicial · standalone). Recupera dano material/moral do condutor/consumidor. Passa por `peticao-inicial-transito` (competencia/valor). Quantum via `calculosjudiciais`. Fecha por `suprema-corte-transito`.

## Anexos obrigatorios (context/)
- `context/jurisprudencia-transito.md` (**Tema 1.122 STJ**, racha domestico x silvestre, limite do fortuito externo — so ✅).
- `context/pedagio-e-consumo.md` (tag/free flow, CDC) + `context/ctb-9503-97.md` (art. 209/209-A — grep).

## Objetivo
Condenar o responsavel (concessionaria de rodovia, operadora de tag, orgao) a **reparar o dano** — material (conserto, prejuizo economico) e moral (abalo, negativacao) — com fundamento correto por cenario e quantum defensavel.

## Quando ativar
- Dano ao usuario em rodovia (buraco, defeito de conservacao, animal na pista, sinalizacao ausente).
- Cobranca indevida de pedagio/tag (debitou errado, cobrou apos cancelamento, autuou com tag ativa).
- **Negativacao indevida** (SPC/Serasa) por multa/cobranca sem lastro.

## Cenarios e fundamento (cada dano tem sua base)

### A. Concessionaria de rodovia — responsabilidade OBJETIVA
- **Base:** CF art. 37, §6 (prestadora de servico publico responde objetivamente) + **CDC art. 14** (fornecedor responde por defeito do servico, independe de culpa) + Lei 8.987/95 (concessoes). O usuario e **consumidor**.
- **Animal na pista — Tema 1.122 STJ (REsp 1.908.738/SP):** a concessionaria responde **independentemente de culpa** por danos de **animais DOMESTICOS** na pista (fortuito interno, risco da atividade). E ilegal jogar no usuario o onus de achar o dono.
- **Buraco / defeito de conservacao / ma sinalizacao:** mesma logica objetiva (defeito na prestacao do servico) — Tema 1.122 como precedente-farol. 🟡 sem sumula propria; citar Tema 1.122 como base e o caso como aplicacao.
- **RACHA / limite honesto:** animal **SILVESTRE** (fauna nativa) NAO entra no Tema 1.122 — ai a discussao migra para responsabilidade do **Estado/orgao ambiental** (divergencia). Nao vender Tema 1.122 como "qualquer animal".
- **Fortuito EXTERNO (excludente):** **assalto a mao armada** na rodovia e fortuito externo — afasta a responsabilidade da concessionaria (REsp 1.872.260/SP). 🟡 confirmar nº no `validador-transito`. Postura honesta: nem todo dano na estrada e indenizavel.

### B. Cobranca indevida de tag / pedagio (Sem Parar, ConectCar, Veloe)
- **Base:** relacao de consumo — **CDC art. 14** (falha do servico) + **art. 42, p.u.** (cobranca indevida → **devolucao em dobro** do que se pagou em excesso, salvo engano justificavel) + inversao do onus (art. 6, VIII).
- Autuacao de free flow (art. 209-A) com **tag ativa e saldo** = auto nulo; se houve cobranca/debito indevido, soma-se o pedido de restituicao.
- **Prova:** extrato da tag/conta (mostra saldo e o debito indevido).

### C. Negativacao indevida (SPC/Serasa)
- **Dano moral in re ipsa** pela inscricao indevida (jurisprudencia consolidada) — se nao havia debito legitimo (multa nao notificada, cobranca ja quitada, tag ativa).
- **Sumula 385 STJ** (limite honesto): havendo **negativacao preexistente legitima**, nao cabe dano moral por nova inscricao (so o cancelamento). 🟡 confirmar Sumula 385 no `validador-transito`. Checar o cadastro do cliente antes de prometer moral.

## Estrutura da peca
1. **Cabeca** (de `peticao-inicial-transito`): concessionaria/operadora e ré (Justica Estadual comum — relacao privada de consumo); ou o ente (se dano por omissao estatal); valor = soma material + moral estimado.
2. **Fatos:** o evento danoso + o nexo + a prova (BO, fotos do buraco/animal, orcamentos, extrato da tag, print da negativacao).
3. **Direito:** o fundamento do cenario (A/B/C) — objetiva CDC/Tema 1.122, ou art. 42 p.u., ou dano moral por negativacao.
4. **Danos:** material (documentado — orcamento/nota) + moral (quantum arbitrado, criterios; NAO inventar valor de tabela). Cross-link `calculosjudiciais` para liquidacao/atualizacao.
5. **Pedidos:** condenacao em reparacao material + moral; devolucao em dobro (se CDC 42); baixa da negativacao (com tutela — cross-link `tutela-urgencia-transito`); honorarios; inversao do onus (CDC).

## Postura honesta
- **Nem todo dano gera indenizacao:** fortuito externo (assalto), animal silvestre (Estado, nao concessionaria), culpa exclusiva da vitima excluem/reduzem.
- **Dano moral tem teto de bom senso:** promessa de "valor alto garantido" e falsa; o juiz arbitra por razoabilidade/proporcionalidade.
- **Sumula 385** pode barrar o moral se ha negativacao anterior legitima.

## Entrega obrigatoria final
Reparatoria redigida (cabeca + fatos com nexo + fundamento do cenario + danos material/moral discriminados + tutela se ha negativacao + pedidos com devolucao em dobro se cabivel) + checklist de provas + remessa do quantum a `calculosjudiciais`.

## Guard
Nenhuma sumula/tema/dispositivo sem `validador-transito` (Tema 1.122 so domesticos; Sumula 385 e REsp 1.872.260 a confirmar). Nao estender Tema 1.122 a animal silvestre. Nao arbitrar dano moral sem criterio. Entrega pela `suprema-corte-transito` (R1-R4). Cross-link, nao duplicar: cobranca indevida bancaria/consumo → `bancario-adv-os`/consumo; liquidacao/atualizacao do dano → `calculosjudiciais-adv-os`.
