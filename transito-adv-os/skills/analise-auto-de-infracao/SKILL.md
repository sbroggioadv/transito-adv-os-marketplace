---
name: analise-auto-de-infracao
description: Analisa o Auto de Infração de Trânsito (AIT/NA/NP) e ranqueia as nulidades em FORTE/MÉDIA/FRACA antes de escolher a peça. Use quando o cliente traz uma multa e pergunta "essa multa tem como cair?", "quais os erros do auto?", "vale a pena brigar?", ao abrir qualquer defesa/recurso administrativo de trânsito, ou quando alguém repete o mito de que "falta de assinatura anula a multa" (a desmentir).
---

# Análise do Auto de Infração — nulidades ranqueadas

## 1. Quando ativa
É o **primeiro passo** de qualquer defesa de trânsito. Ativa quando o cliente traz um AIT, uma NA ou uma NP e quer saber se a multa "tem como cair". Você mapeia os vícios e diz a **força real** de cada um — só então escolhe a peça (`defesa-da-autuacao`, `recurso-jari`, `recurso-cetran`, `acao-anulatoria-multa-infracao`). Se o cliente chega com o mito "falta de assinatura anula", desminta aqui.

Antes de qualquer coisa, confirme a **fase** (recebeu NA ou NP?) via `triagem-transito` — a peça depende disso.

## 2. Base legal ancorada
- **art. 280 CTB** — conteúdo obrigatório do AIT: (I) tipificação da infração; (II) local, data e hora; (III) placa/marca/espécie do veículo; (IV) prontuário do condutor quando possível; (V/VI) identificação do órgão + agente autuador OU do equipamento; assinatura do infrator **quando possível**. Vício em elemento essencial → tese de nulidade.
- **art. 281, parágrafo único, I, CTB** — o auto será **arquivado** e o registro julgado insubsistente quando "inconsistente ou irregular". É o gancho de quase toda nulidade formal; combine SEMPRE com o requisito do art. 280 que foi violado.
- **art. 281, p.ú., II** — arquivamento se a NA não sair em **30 dias** (nulidade objetiva → `notificacao-e-prazos`).
- Âncora jurisprudencial: **Súmula 312 STJ** (dupla notificação — autuação + penalidade).

## 3. Ranking das nulidades (FORTE / MÉDIA / FRACA)

| Vício | Fundamento | Força |
|---|---|---|
| Falta/erro na **identificação do agente ou do órgão** autuador; órgão incompetente para a via | art. 280 caput + 281 p.ú. I | **FORTE** |
| Erro em **local, data ou hora** (local inexistente, data impossível, veículo comprovadamente em outra cidade) | art. 280 II + 281 p.ú. I | **FORTE** (com prova de álibi) |
| **NA expedida após 30 dias** da infração | art. 281 p.ú. II CTB / art. 4º §1º Res.918/2022 | **FORTE** (nulidade objetiva) |
| **Ausência de dupla notificação** (recebeu só NP, sem NA para defesa) | arts. 280/281/282 + Súmula 312 STJ | **FORTE** (cerceamento) |
| **Falta de campo obrigatório do art. 280** (placa trocada, marca divergente, tipificação ausente) | art. 280 + 281 p.ú. I | **FORTE** se o erro impede identificar veículo/fato |
| **Enquadramento legal errado** (código não bate com o fato narrado) | art. 280 I + 281 p.ú. I | **MÉDIA→FORTE** |
| **Equipamento sem aferição INMETRO** vigente na data (radar/etilômetro) | art. 280 + verificação metrológica | **MÉDIA→FORTE** (forte se certificado vencido) |
| **Sinalização irregular/ausente** (radar sem placa; limite não sinalizado) | **art. 90 CTB** (não se aplica sanção por sinalização não visível/legível) | **MÉDIA** (forte com foto) |
| **Cerceamento de defesa** (decisão-padrão que não enfrenta argumentos; negativa de acesso a imagens/laudo) | art. 5º LV CF | **MÉDIA** (melhor acoplada a outro vício) |
| **Ausência de assinatura do condutor** no AIT | — | **FRACA / MITO** |

## 4. Postura honesta — o mito de balcão
O **item da assinatura** é o mito que quase todo cliente traz. **Desminta:** o AIT é válido sem assinatura do infrator (recusa, fuga ou autuação eletrônica não permitem colher assinatura). NÃO usar como tese principal. Nunca prometa "anula qualquer multa" — ranqueie honestamente e diga quando a tese é fraca. Se só há vício FRACO, seja franco sobre a baixa chance e avalie o desconto (ver `parecer-transito`).

## 5. O que produzir — diagnóstico
1. Rode o **checklist do art. 280** campo a campo sobre o AIT.
2. Confira as **datas** (infração → NA → NP) contra os prazos (`notificacao-e-prazos`).
3. Para cada vício achado, atribua **FORTE/MÉDIA/FRACA** e o dispositivo.
4. Se o vício for de equipamento/sinalização, oriente **requerer ao órgão** o certificado INMETRO e as fotos do trecho — a falta de juntada vira cerceamento.
5. Recomende a peça e a fase, ou o pagamento com desconto se não houver tese.

## 6. Cross-link
Fase e prazos → `notificacao-e-prazos`; indicação de condutor → `indicacao-de-condutor`; infração específica → `enquadramento-e-multas-comuns`; peça → `defesa-da-autuacao` / `recurso-jari`; via judicial → `acao-anulatoria-multa-infracao`. Todo dispositivo/prazo passa pelo `validador-transito`.
