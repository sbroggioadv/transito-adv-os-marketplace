---
name: enquadramento-e-multas-comuns
description: Mapeia as infrações de trânsito mais comuns e a defesa típica de cada uma (velocidade, avanço de sinal, estacionamento, celular, cinto), com foco em aferição INMETRO e sinalização (art. 90). Use quando o cliente pergunta "levei multa por excesso de velocidade/avançar sinal/estacionar/celular/sem cinto, tem defesa?", "o radar estava aferido?", "a placa de limite não existia", ou para escolher a tese certa por tipo de infração.
---

# Enquadramento e Multas Comuns — teses por tipo

## 1. Quando ativa
Ativa quando o cliente identifica a **infração específica** e quer saber a defesa típica dela. Complementa `analise-auto-de-infracao` (que ranqueia os vícios formais): aqui você acrescenta a **tese de mérito** própria de cada tipo. Sempre confira antes a fase (`triagem-transito`) e os prazos (`notificacao-e-prazos`).

## 2. Âncoras transversais (valem para quase toda multa)
- **Valores (art. 258 CTB):** gravíssima **R$ 293,47** · grave **R$ 195,23** · média **R$ 130,16** · leve **R$ 88,38**. Gravíssimas específicas têm multiplicador no próprio tipo (🟡 confirmar o fator antes de calcular valor final).
- **Pontos (art. 259 CTB):** gravíssima **7** · grave **5** · média **4** · leve **3**.
- **Aferição INMETRO (art. 280 CTB):** toda infração por **equipamento** (radar, etilômetro, balança) exige verificação metrológica vigente na data. **Requerer ao órgão** o certificado — se não juntar, combine com cerceamento (`analise-auto-de-infracao`).
- **Sinalização (art. 90 CTB):** "não se aplicará a sanção quando a sinalização não estiver visível, correta e legível". Sem placa de limite, sem aviso de "fiscalização eletrônica", placa oculta → tese com prova fotográfica + croqui.
- **Enquadramento errado (art. 280 I + 281 p.ú. I):** o código do AIT não bate com o fato narrado → nulidade; não se "readequa" a tipificação no julgamento (viola contraditório).

## 3. As infrações comuns e a defesa típica

**Excesso de velocidade — art. 218 CTB** (✅ ancorado): natureza escalona pela faixa (até 20% / 20-50% / acima de 50%); **acima de 50% (inciso III) é gravíssima e autossuspensiva**. Defesa: (a) **aferição INMETRO** do radar vigente na data; (b) **sinalização** (art. 90 — placa de limite e de fiscalização); (c) margem de tolerância do próprio equipamento; (d) enquadramento na faixa correta.

**Avançar sinal vermelho / parada obrigatória — art. 208 CTB ✅** (conferido no Planalto): "Avançar o sinal vermelho do semáforo ou o de parada obrigatória, exceto onde houver sinalização que permita a livre conversão à direita prevista no art. 44-A" (redação Lei 14.071/2020) — **gravíssima**. Defesa: aferição do equipamento de foto-sensor; sinalização/temporização do semáforo; imagem que comprove o cruzamento sob amarelo; erro de horário.

**Estacionamento/parada irregular — arts. 181 (estacionar) e 182 (parar) CTB ✅** (conferido): a natureza **varia do leve ao gravíssimo** conforme o local (o art. 181 tem incisos de leve a gravíssima — ex.: vaga de PcD/idoso). Defesa: sinalização de proibição ausente/ilegível (art. 90); erro de local no AIT; foto que contrarie a narrativa.

**Dirigir manuseando celular — art. 252, parágrafo único (c/c inciso V) CTB ✅** (conferido): **segurar ou manusear** o celular ao dirigir = **gravíssima** ("A hipótese prevista no inciso V caracterizar-se-á como infração gravíssima no caso de o condutor estar segurando ou manuseando telefone celular" — Lei 13.281/2016). ⚠️ **Não confundir:** usar **fone de ouvido ou celular** sem segurar = **art. 252, VI = média**. Defesa: descrição genérica do agente ("usava o celular" sem detalhar se segurava/manuseava) = insuficiência probatória + risco de enquadramento errado (média × gravíssima); ausência de imagem.

**Sem cinto de segurança — art. 167 CTB ✅** (conferido): "Deixar o condutor ou passageiro de usar o cinto de segurança, conforme previsto no art. 65" — **grave** (retenção do veículo até colocação). Defesa: descrição genérica; erro de identificação do ocupante; foto.

> Para cada tipo, a **espinha** é a mesma: checar aferição do equipamento, sinalização (art. 90), enquadramento e a descrição do agente. O tipo muda a faixa e a natureza; a tese formal é transversal.

## 4. Postura honesta
Multa por **agente presencial** com descrição detalhada é mais difícil de derrubar que multa **eletrônica** com vício de aferição/sinalização. Nem toda multa comum tem tese — se só há o mito da assinatura, seja franco e avalie o **desconto de 40%** (SNE + renúncia, art. 21 Res.918) via `parecer-transito`. Não prometa cancelamento.

## 5. Regra dura anti-alucinação
**Só afirme número de artigo com âncora.** Estão **✅ conferidos no Planalto** e podem entrar direto: 208 (avançar sinal, gravíssima), 181/182 (estacionar/parar), 252 §único c/c V (manusear celular, gravíssima) e 252 VI (fone/celular, média), 167 (cinto, grave), 218 (velocidade), 90 (sinalização), 258 (valores), 259 (pontos), 280 (aferição). **Ao redigir peça, ainda passe pelo `validador-transito`** para checar o **enquadramento aplicado ao caso** (faixa/natureza/multiplicador) — o número do artigo está travado; o que muda por caso é a subsunção.

## 6. Cross-link e fechamento
Vícios formais → `analise-auto-de-infracao`; prazos → `notificacao-e-prazos`; peça por fase → `defesa-da-autuacao` / `recurso-jari`; velocidade acima de 50% (autossuspensiva) → `processo-suspensao-direito-dirigir`; álcool/recusa → `bafometro-e-recusa-administrativa`. Se produzir peça, **fecha pela `suprema-corte-transito` (R1-R4)** + `validador-transito`.
