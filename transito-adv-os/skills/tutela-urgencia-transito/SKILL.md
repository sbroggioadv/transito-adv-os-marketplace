---
name: tutela-urgencia-transito
description: "Formula o pedido de tutela de urgencia (CPC 300) nas acoes de transito para liberar a CNH, suspender pontuacao/penalidade/suspensao, destravar licenciamento ou liberar o veiculo apreendido, articulando fumus boni iuris e periculum in mora tipicos do dominio. Use quando o operador disser tutela de urgencia de transito, liminar para liberar a CNH, suspender a suspensao/pontos, destravar o licenciamento, pedido de urgencia contra o DETRAN/DNIT, preciso voltar a dirigir ja, liberar o carro do patio, ou anexar a tutela a uma anulatoria/MS de transito."
---

# TUTELA-URGENCIA-TRANSITO — o pedido liminar do dominio

> Camada 6 (Judicial · standalone). Nao e acao autonoma: instrui a inicial da anulatoria/MS/reparatoria ou vem incidental. Modela o fumus + periculum tipicos de transito. Fecha por `suprema-corte-transito`.

## Anexos obrigatorios (context/)
- Base: skill `base-processual-judicial-transito` (CPC 300-302 filtrado; no MS, liminar do art. 7, III Lei 12.016/09).
- `context/processo-adm-fluxo-prazos.md` (art. 18 Res.918 — pontos/efeito suspensivo) + `context/jurisprudencia-transito.md` (so ✅).

## Objetivo
Conseguir a **decisao liminar** que devolve ao cliente, ja, o bem ameacado (dirigir, licenciar, o veiculo), demonstrando os dois requisitos do art. 300 CPC de forma concreta e ancorada no caso.

## Quando ativar
- Ha **perigo de dano** enquanto a acao tramita: CNH suspensa/bloqueada, pontos prestes a suspender, licenciamento vencendo, veiculo no patio acumulando taxas, negativacao ativa.
- Acopla-se a: `acao-anulatoria-multa-infracao`, `mandado-de-seguranca-transito`, `anulatoria-suspensao-cassacao`, `acao-reparatoria-transito`.

## Requisitos — CPC 300 (via ordinaria) / art. 7, III Lei 12.016/09 (no MS)
- **Fumus boni iuris (probabilidade do direito):** a tese de merito ja demonstrada documentalmente — nulidade do AIT (Sumula 312), multa nao notificada (Sumula 127), pontos de infracao nao definitiva (art. 18 Res.918), etc. Quanto mais a prova estiver pronta, mais forte.
- **Periculum in mora (perigo de dano/risco ao resultado util):** ver tabela de perigos tipicos abaixo.
- **Reversibilidade (300 §3):** demonstrar que a medida e reversivel (voltar a dirigir nao consome o direito da Fazenda) — afasta a vedacao do §3.
- **Caucao (300 §1, facultativa):** oferecer se ajudar a convencer.

## Perigos tipicos (periculum ja mapeado) — usar o que se aplica
| Situacao | Pedido liminar | Periculum concreto |
|---|---|---|
| CNH suspensa/cassada/bloqueada em discussao | suspender a penalidade e **devolver o direito de dirigir** | CNH e instrumento de trabalho/locomocao; dano de dificil reparacao |
| Perto do limite de pontos, multa sub judice | **suspender a inclusao dos pontos** no RENACH (reforca art. 18 Res.918) | evitar a suspensao antes do julgamento |
| Licenciamento travado por multa nao notificada | **destravar o licenciamento/CRLV** | veiculo irregular = apreensao + multa gravissima (art. 230) |
| Veiculo removido ao patio (art. 271) | **liberar o veiculo** sem exigir a multa impugnada | taxas diarias de estada crescentes; risco de leilao (art. 328) |
| Negativacao por cobranca indevida (tag/pedagio) | **suspender/baixar a negativacao** | abalo de credito continuado |

## Estrutura do pedido
1. **Topico proprio na inicial** ("DA TUTELA DE URGENCIA") apos os fundamentos de merito.
2. **Fumus:** remeter a fundamentacao ja exposta + o documento que a prova.
3. **Periculum:** o dano concreto e iminente (a linha da tabela), com a prova (extrato RENACH, NP, aviso de vencimento, guia de patio, negativacao).
4. **Reversibilidade + caucao** se pertinente.
5. **Pedido:** deferimento **inaudita altera parte** (o dano nao espera o contraditorio) + astreinte (CPC 537) se a autoridade descumprir + oficio ao orgao para cumprir (destravar sistema).

## Postura honesta
- **Contra a Fazenda ha cautela extra:** o juiz pode exigir fumus robusto e as vezes ouvir o ente antes (CPC 300 §2). Tutela nao e garantida — depende da forca da tese.
- **Reversibilidade** e o ponto que a Fazenda ataca; enderecar de frente (a medida nao esvazia o processo administrativo, so o suspende).
- **No MS**, a liminar segue o art. 7, III da Lei 12.016/09 (nao o CPC 300 diretamente) — nome e base corretos; efeito pratico equivalente.

## Entrega obrigatoria final
Topico de tutela pronto para colar na inicial (fumus + periculum ancorados no caso + reversibilidade + pedido inaudita altera parte com astreinte/oficio) + indicacao dos documentos que provam o periculum.

## Guard
Nenhum dispositivo/sumula/resolucao sem `validador-transito`. Sempre casar o periculum com PROVA no caso concreto (nao alegar perigo generico). No MS, citar art. 7, III Lei 12.016/09, nao CPC 300. Entrega pela `suprema-corte-transito` (R1-R4). Cross-link, nao duplicar: a acao que recebe a tutela vem de `acao-anulatoria-multa-infracao` / `mandado-de-seguranca-transito` / `anulatoria-suspensao-cassacao` / `acao-reparatoria-transito`.
