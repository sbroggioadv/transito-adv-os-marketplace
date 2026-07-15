---
name: infracao-de-pedagio-e-free-flow
description: Defende autuação por evasão de pedágio, free flow (pórtico sem cancela) e bloqueio viário/pesagem — art. 209 e 209-A CTB. A tese-mãe é que o tipo do 209-A exige DOLO de evasão (tag ativa + saldo, cancela que não abriu, ou tentativa de pagar = SEM evasão → auto nulo). Use quando o cliente foi multado por passar por pedágio sem pagar, por não regularizar o free flow, por "furar" barreira de fiscalização, cancela de balança ou posto de pesagem; quando a antena não debitou a tag; ou quando ele pergunta "pode multar por não pagar pedágio?", "furei o pórtico sem querer", "recebi multa do sem parar".
---

# Infração de Pedágio & Free Flow — art. 209 e 209-A CTB

## 1. Quando ativa / trilha
Cliente autuado em pedágio, pórtico de livre passagem (**free flow**), barreira de fiscalização, cancela de balança ou posto de pesagem. Triar **primeiro a fase** (recebeu NA ou NP? → `triagem-transito`) e a causa: passou de propósito × falha do sistema. Se houver cobrança indevida da operadora da tag ou dano, cruza com `tag-e-cobranca-indevida`.

## 2. Base legal ancorada (verificada ✅)
Os dois artigos foram **desmembrados pela Lei 14.157/2021** — citar corretamente:

- **Art. 209 CTB** (redação Lei 14.157/2021): "Transpor, sem autorização, bloqueio viário com ou sem sinalização ou dispositivos auxiliares, ou deixar de adentrar às áreas destinadas à pesagem de veículos" — **GRAVE**, multa (R$ 195,23) + **5 pontos**. É o artigo de **barreira/balança**, NÃO o do pedágio.
- **Art. 209-A CTB** (INCLUÍDO pela Lei 14.157/2021) — **este é o "artigo do pedágio":** "Evadir-se da cobrança pelo uso de rodovias e vias urbanas para não efetuar o seu pagamento, ou deixar de efetuá-lo na forma estabelecida" — **GRAVE**, multa (R$ 195,23) + **5 pontos**. É a base legal do **free flow** (pórtico sem cancela).

Ancoragem verbatim em `context/ctb-9503-97.md` §9 e `context/pedagio-e-consumo.md`. Valores: art. 258 (grave R$ 195,23) + art. 259 (grave 5 pontos).

## 3. Tese-mãe: o tipo exige DOLO de evasão
O art. 209-A pune quem se **"evadir-se… PARA não efetuar o pagamento"** — o núcleo do tipo é a **intenção de não pagar**. Sem o elemento subjetivo, o auto não se sustenta:

| Situação | Enquadramento |
|----------|---------------|
| Passou de propósito, sem tag, sem pagar | Evasão dolosa → infração legítima |
| Tag ativa + saldo, mas a antena não debitou / cancela não abriu | Falha do serviço → **NÃO há evasão** → auto nulo |
| Free flow: o cliente tentou/quis pagar dentro do prazo, mas o sistema não processou | Sem dolo → auto insubsistente |

**Argumento central da defesa:** demonstrar boa-fé e capacidade de pagamento na data/hora exata → afasta o dolo → descaracteriza o tipo do 209-A.

## 4. Provas para derrubar a autuação (em ordem de força)
1. **Extrato de saldo e movimentação da tag** na **data e horário exatos** da passagem (prova saldo/limite ativo).
2. **Contrato / termo de adesão** da tag (obrigação da operadora de garantir leitura e débito).
3. **Comprovante de recarga/pagamento** de mensalidade anterior à viagem.
4. **Histórico de passagens** anteriores e posteriores na mesma praça (usuário regular → falha pontual, não hábito de evasão).
5. **Protocolos de reclamação** (SAC/ouvidoria da operadora e da concessionária; Consumidor.gov.br — canal indicado pela ANTT para pedágio eletrônico).
6. No **free flow**: comprovante de que **tentou pagar dentro do prazo** de regularização.

## 5. Estratégia de dois planos
- **Plano administrativo (trânsito):** defesa prévia contra a NA → recurso `recurso-jari` → `recurso-cetran`. O CDC não rege a multa em si, mas é a arma para **atacar a CAUSA** (provar a falha do serviço → não houve evasão).
- **Plano civil/consumo:** ação contra operadora/concessionária (cancelamento da cobrança, repetição em dobro, dano) → `tag-e-cobranca-indevida` + `acao-reparatoria-transito`.

## 6. Postura honesta (não prometer o que não se prova)
- **Free flow tem janela de regularização** — o usuário recebe a cobrança e tem prazo para pagar **antes** de virar infração. 🟡 **PROIBIDO citar o número/prazo exato da Resolução CONTRAN/ANTT do free flow sem verificação** — a regra existe, o número não foi capturado. Rotear a `validador-transito` antes de a peça sair.
- Se o cliente **passou mesmo sem tag e sem pagar**, a infração é legítima — a tese cai; oriente pelo desconto (art. 284) ou por atenuar, não por anular.
- Evasão de pedágio **não vira** crime automático; enquadrar só no administrativo (209-A). Não inventar desdobramento penal.

## 7. Cross-link (soft)
`tag-e-cobranca-indevida` (CDC contra operadora) · `responsabilidade-concessionaria` (defeito da via) · `defesa-da-autuacao`/`recurso-jari`/`recurso-cetran` (rito) · `acao-reparatoria-transito` (dano). Cálculo de dano → `calculosjudiciais-adv-os`; cobrança indevida → `bancario`/consumo.

## 8. Fechamento obrigatório
Toda peça (defesa/recurso/anulatória) **fecha por `suprema-corte-transito`** (R1 fatos/fase · R2 fundamentação vigente — 209-A, nunca só 209 · R3 prazos corridos · R4 forma/via) **+ `validador-transito`** (confirma o 209-A, os valores e o 🟡 do free flow). Zero citação de número de resolução não verificado.
