---
name: anulatoria-suspensao-cassacao
description: "Redige acao anulatoria do processo de suspensao (art. 261 CTB) ou cassacao (art. 263 CTB) do direito de dirigir, atacando cerceamento de defesa, lancamento de pontos de infracao ainda NAO definitiva (art. 18 Res. 918/2022), instauracao baseada em multa prescrita/anulada e erro na contagem dos 12 meses. Use quando o operador disser anular a suspensao da CNH, processo de suspensao/cassacao viciado, derrubar a cassacao na justica, contestar a suspensao do direito de dirigir, os pontos que geraram a suspensao nao eram definitivos, ou a multa-base da suspensao foi anulada."
---

# ANULATORIA-SUSPENSAO-CASSACAO — anular o processo punitivo da CNH

> Camada 6 (Judicial · standalone). Ataca o PROCESSO de suspensao/cassacao (rito proprio, diferente do processo de multa). Passa por `peticao-inicial-transito`. Fecha por `suprema-corte-transito`.

## Anexos obrigatorios (context/)
- `context/ctb-9503-97.md` (arts. **261** suspensao, **263** cassacao/reabilitacao — grep) + `context/resolucoes-contran-mapa.md` (rito da Res. 723/2018 alterada pela **844/2021**).
- `context/processo-adm-fluxo-prazos.md` (art. 18 Res.918 — pontos so apos esgotados recursos) + `context/jurisprudencia-transito.md` (so ✅).

## Objetivo
Anular judicialmente a suspensao/cassacao (ou o processo que a gerou) por vicio processual ou por queda da base (pontos/multa), com **restituicao do direito de dirigir** e tutela para o cliente voltar a dirigir enquanto discute.

## Quando ativar
- Instaurado (ou concluido) processo de **suspensao por pontos** (art. 261, I), **suspensao autossuspensiva** (art. 261, II) ou **cassacao** (art. 263), com vicio.
- Cliente ja teve a CNH recolhida/bloqueada ou foi notificado da instauracao.

## Teses de nulidade (o merito — ranquear as FORTES)
**FORTES:**
- **Pontos lancados de infracao ainda NAO definitiva** — viola **art. 18 Res. 918/2022** (os pontos so vao ao RENACH apos esgotados os recursos JARI + CETRAN). Se uma das multas-base ainda estava em recurso/sub judice, ela nao podia compor a contagem → suspensao prematura. **Trunfo estrutural.**
- **Multa-base anulada ou prescrita** — cai a infracao que fundou a contagem, cai a suspensao (efeito cascata). Prescricao por analogia a Lei 9.873/99 (🟡 nº de anos ao `validador-transito`).
- **Cerceamento de defesa** — decisao-padrao no processo de suspensao; ausencia de notificacao regular da instauracao (aplicacao da logica da Sumula 312 ao sancionador); indeferimento de prova.
- **Erro na contagem dos 12 meses / dos pontos** — janela movel mal computada; dupla contagem; pontos ja zerados por reciclagem.

**Especificas da cassacao (art. 263):**
- Enquadramento indevido nas 3 hipoteses (I dirigir com direito suspenso; II reincidencia 12 meses nos arts. 162 III/163/164/165/173/174/175; III condenacao judicial por delito) — se nao se subsome, a cassacao e nula.
- Reabilitacao (art. 263 §2): apos 2 anos, refaz TODOS os exames — orientar, nao e "volta automatica".

## Estrutura da peca
1. **Cabeca** (de `peticao-inicial-transito`): vara/competencia (esfera do orgao do prontuario — em regra DETRAN estadual → Justica Estadual); reu (o ente); valor (proveito economico/estimado).
2. **Fatos:** cronologia do processo de suspensao/cassacao (instauracao, notificacao, defesa, JARI, CETRAN) + a fragilidade (qual multa nao era definitiva, onde faltou defesa, erro de contagem).
3. **Direito:** as teses FORTES com art. 261/263 + art. 18 Res.918; efeito cascata da queda da multa-base.
4. **Tutela de urgencia (quase sempre):** **suspender a suspensao** / devolver a CNH enquanto discute — cross-link `tutela-urgencia-transito` (CPC 300); periculum obvio (perda do direito de locomocao/trabalho).
5. **Pedidos:** anular o processo/penalidade de suspensao ou cassacao; restituir o direito de dirigir e a CNH; baixar a restricao no RENACH; honorarios; gratuidade se cabivel.

## Postura honesta
- **Rito proprio:** o processo de suspensao/cassacao NAO e o mesmo da multa (Res. 844/2021, nao a 918). Nao transplantar prazos da multa. 🟡 prazos exatos de defesa/recurso da 844/2021 ao `validador-transito`.
- **Anular a suspensao nao apaga as infracoes** — se os pontos eram legitimos e definitivos, a suspensao pode ser legal; a tese vive de vicio real (nao-definitividade, prescricao, cerceamento).
- **Cassacao por condenacao criminal** (art. 263, III) tem base judicial — atacar exige mexer no titulo penal (fora do escopo v0.1; GAP criminal).

## Entrega obrigatoria final
Anulatoria redigida (cabeca + fatos com a cronologia do processo punitivo + teses FORTES fundamentadas + tutela para devolver a CNH + pedidos) + checklist (portaria de instauracao, notificacoes, extrato de pontos com status de cada multa, decisoes JARI/CETRAN).

## Guard
Nenhum dispositivo/resolucao/prazo sem `validador-transito`. Confirmar o **status de cada multa-base** (definitiva x sub judice) antes de alegar art. 18 Res.918. Nao confundir rito da suspensao (844/2021) com o da multa (918/2022). Entrega pela `suprema-corte-transito` (R1-R4). Cross-link, nao duplicar: vicio de multa isolada → `acao-anulatoria-multa-infracao`; direito liquido e certo (bloqueio sem processo) → `mandado-de-seguranca-transito`.
