# Pedágio, Free Flow e Relação de Consumo

> Anexo de referência do plugin **transito-adv-os**. A camada onde trânsito encontra o CDC: infração de pedágio/free flow (arts. 209/209-A), tag eletrônica (relação de consumo), e responsabilidade da concessionária de rodovia.
> Fontes: Planalto (CTB), STJ, Senado, doutrina consumerista. Captura 2026-07-15.
> **Legenda:** ✅ confirmado · 🟡 a confirmar (nº de processo / regulação) antes de citar em peça · 🔴 revogado/pegadinha.
> **Guard:** números de REsp/EAREsp marcados 🟡 **exigem WebFetch real antes de entrar em qualquer peça** (anti-alucinação da família).

---

## 1. INFRAÇÃO DE PEDÁGIO / BLOQUEIO VIÁRIO — arts. 209 e 209-A ✅

A **Lei 14.157/2021 desmembrou** o antigo art. 209. Citar os dois corretamente:

### Art. 209 (redação Lei 14.157/2021) ✅ — bloqueio viário / pesagem
> "Transpor, sem autorização, bloqueio viário com ou sem sinalização ou dispositivos auxiliares, ou deixar de adentrar às áreas destinadas à pesagem de veículos."
- **Infração:** GRAVE · **Penalidade:** multa (R$ 195,23) + **5 pontos**.
- Cobre: furar barreira policial/fiscalização, cancela de balança, bloqueio de posto de pesagem. **Não** é o artigo da evasão de pedágio.

### Art. 209-A (incluído pela Lei 14.157/2021) ✅ — **o "artigo do pedágio" e do free flow**
> "Evadir-se da cobrança pelo uso de rodovias e vias urbanas para não efetuar o seu pagamento, ou deixar de efetuá-lo na forma estabelecida."
- **Infração:** GRAVE · **Penalidade:** multa (R$ 195,23) + **5 pontos**.
- Base legal do **pedágio eletrônico sem cancela (free flow)**: quem passa pelo pórtico e **não regulariza no prazo** comete a 209-A.

---

## 2. A DISTINÇÃO QUE DECIDE A DEFESA — evasão DOLOSA × falha do sistema ✅

O tipo do art. 209-A exige **"evadir-se… para não efetuar o pagamento"** — pressupõe **intenção de não pagar** (elemento subjetivo):
- **Evasão dolosa** (passou de propósito, sem tag, sem pagar) → infração legítima.
- **Falha do sistema** (tag ativa + saldo, mas a cancela não abriu ou a antena não debitou; ou, no free flow, o cliente **tentou/quis pagar** e o sistema não processou) → **não há "evasão"**, o elemento subjetivo não se configura → **auto NULO**.
- **Prova-rainha:** o **extrato da tag** na data/hora exata da passagem (comprova saldo/limite ativo → afasta o dolo de evasão).

🟡 **Free flow (pórtico de livre passagem):** existe **janela de regularização** (o usuário recebe a cobrança e tem prazo para pagar antes de virar infração). **Confirmar o número e o prazo da Resolução CONTRAN/ANTT** que regula o free flow antes de citar — a regra existe, o número exato não foi capturado.

---

## 3. TAG ELETRÔNICA (Sem Parar / ConectCar / Veloe / Move Mais) — CONSUMO ✅

Há **relação de consumo** entre motorista e operadora da tag (art. 2º CDC = destinatário final; art. 3º = fornecedor de serviço de pagamento). **CDC aplica-se integralmente.** Na verdade há **duas relações de consumo simultâneas** a explorar:
1. Motorista **×** operadora da tag (serviço de pagamento eletrônico).
2. Motorista **×** concessionária de rodovia (serviço público tarifado — pedágio é **tarifa/preço público**, não tributo).

### Teses de defesa consumerista ✅

| Tese | Base legal | Como usar |
|---|---|---|
| **Falha na prestação — responsabilidade objetiva** | CDC **art. 14** | Tag ativa + saldo, mas sem débito/leitura = defeito do serviço. Independe de culpa; basta dano + nexo. O risco do negócio é da operadora/concessionária. |
| **Inversão do ônus da prova** | CDC **art. 6º VIII** | Logs de passagem e leitura da antena estão sob controle da empresa (hipossuficiência técnica do usuário). Requerer que a empresa prove que o sistema funcionava e que não havia saldo. |
| **Repetição do indébito em dobro** | CDC **art. 42 §ú** | Cobrança em duplicidade, pedágio não devido, tarifa sem prestação → devolução **em dobro**, salvo engano justificável. |
| **Dano moral** | CDC art. 6º VI + art. 14 | Autuação/negativação indevida, pontos por erro de sistema, risco de suspensão → dano moral (mais sólido com **inscrição indevida** ou efeito concreto na CNH; sem isso, risco de "mero aborrecimento"). |

🟡 **Repetição em dobro — precedente-âncora a confirmar:** STJ **Corte Especial, EAREsp 676.608/RS** (a repetição em dobro do art. 42 §ú **independe de prova de má-fé**, com **modulação a partir de 30/03/2021**). É o leading case que blinda o pedido de dobro. **Confirmar número/relator/modulação por WebFetch antes de citar.**

### Provas para cancelar a autuação por falha da tag ✅ (ordem de utilidade)
1. **Extrato de saldo e movimentação** da tag na data/hora exata da passagem.
2. **Contrato / termo de adesão** da tag (obrigação de garantir leitura e débito).
3. **Comprovante de recarga/pagamento** anterior à viagem.
4. **Histórico de passagens** na mesma praça (usuário regular → falha pontual, não hábito de evasão).
5. **Protocolos de reclamação** (SAC/ouvidoria + **Consumidor.gov.br** — canal indicado pela ANTT p/ pedágio eletrônico).
6. No **free flow:** comprovante de que **tentou pagar dentro do prazo** de regularização.

### Estratégia de dois planos ✅
- **Administrativo (trânsito):** defesa prévia + recurso (JARI → CETRAN). O CDC não rege a multa em si, mas é a arma para **atacar a CAUSA** (provar a falha → não houve evasão → auto insubsistente).
- **Civil/consumo:** ação contra operadora/concessionária pedindo cancelamento da cobrança, **repetição em dobro** e **dano moral**, com inversão do ônus. Cross-link `bancario`/consumo. Cruzamento das duas frentes = `protocolo-p4-transito`.

---

## 4. RESPONSABILIDADE DA CONCESSIONÁRIA DE RODOVIA ✅

**Responsabilidade OBJETIVA.** Base: **CF art. 37 §6º** (PJ de direito privado prestadora de serviço público) + **CDC arts. 14 e 22** (usuário = consumidor). Usuário prova **dano + nexo + defeito**; não prova culpa.

### RESPONDE (defeito do serviço — risco interno da via) ✅
- **Buraco na pista**, **falta/insuficiência de sinalização**, **objeto estranho na via**, **animal doméstico na pista**.
- **Tema 1.122 STJ** (animais **domésticos**, independe de culpa, CDC + Lei 8.987/95) — ver `jurisprudencia-transito.md`. 🟡 confirmar nº do REsp 1.908.738/SP antes de citar.

### NÃO RESPONDE (fortuito externo / fato de terceiro) ✅ — LIMITE HONESTO
- **REsp 1.872.260/SP**, STJ 3ª Turma, Rel. Min. Marco Aurélio Bellizze, j. 04/10/2022, **Informativo 752**: concessionária **NÃO responde** por **roubo à mão armada** contra usuário no posto de pedágio — **fortuito externo** que rompe o nexo (CDC art. 14 §3º II). Segurança da concessionária "limita-se à estrada, não inclui segurança armada contra criminalidade".
- ⚠️ **Racha do Tema 1.122:** animal **SILVESTRE** (fauna nativa) **não** entra automaticamente — aí a discussão migra para o **Estado/órgão ambiental**. Não vender Tema 1.122 como "qualquer animal".

### Prescrição da reparação 🟡 (divergência real)
- **CDC art. 27 = 5 anos** (acidente = fato do serviço) — posição consumerista, a defender como principal.
- Há julgados aplicando **3 anos** (CC art. 206 §3º V — reparação civil). **Tratar como controvertido**, não pacificado.

---

### Fontes
- CTB arts. 209 / 209-A (Lei 14.157/2021) — Planalto / CTB Digital / parecer do Senado.
- CDC arts. 6º VIII, 14, 22, 27, 42 §ú — Planalto.
- STJ: Tema 1.122 (REsp 1.908.738/SP 🟡), REsp 1.872.260/SP (Info 752), EAREsp 676.608/RS (🟡).
