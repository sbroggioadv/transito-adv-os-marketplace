---
name: tag-e-cobranca-indevida
description: Aciona a operadora de tag (Sem Parar, ConectCar, Veloe, Move Mais) por falha do serviço e cobrança indevida — CDC art. 14 (responsabilidade objetiva), art. 6º VIII (inversão do ônus), art. 42 §ú (repetição em dobro) e dano moral por negativação. É a frente CÍVEL/CONSUMO que complementa o cancelamento da autuação de pedágio. Use quando a tag não debitou mas veio multa, quando a operadora cobrou pedágio já pago, tarifa/mensalidade sem prestação, cobrança em duplicidade, negativou o cliente ou gerou pontos na CNH por erro de sistema; ou quando pergunta "o sem parar me cobrou errado", "fui negativado por pedágio que paguei".
---

# Tag & Cobrança Indevida — CDC contra a operadora

## 1. Quando ativa / trilha
Cliente lesado pela **operadora da tag** (Sem Parar, ConectCar, Veloe, Move Mais) ou pela concessionária: tag não debitou e gerou multa, cobrança em duplicidade, pedágio já pago cobrado de novo, tarifa/mensalidade sem prestação, negativação indevida, pontos na CNH por erro do sistema. É a frente **cível/consumo** — anda em paralelo com `infracao-de-pedagio-e-free-flow` (frente administrativa, que ataca a multa em si).

## 2. Há relação de consumo — CDC integral ✅
Há **duas relações de consumo simultâneas** a explorar (`context/pedagio-e-consumo.md`):
1. Motorista **×** operadora da tag (serviço de pagamento eletrônico — art. 2º e 3º CDC).
2. Motorista **×** concessionária da rodovia (serviço público tarifado; pedágio é **tarifa/preço público**, não tributo).

O CDC aplica-se **integralmente** à falha do serviço e às consequências civis.

## 3. Teses de defesa/pedido (base ancorada ✅)

| Tese | Base legal | Como usar |
|------|-----------|-----------|
| **Falha na prestação — responsabilidade objetiva** | CDC **art. 14** | Tag ativa + saldo, mas sem débito/leitura = defeito do serviço. Independe de culpa; basta dano + nexo. O risco do negócio é da operadora. |
| **Inversão do ônus da prova** | CDC **art. 6º, VIII** | Logs de passagem e de leitura da antena estão sob controle da empresa (hipossuficiência técnica do usuário). Requerer que a operadora prove que o sistema funcionou e que não havia saldo. |
| **Repetição do indébito em dobro** | CDC **art. 42, § único** | Cobrança em duplicidade, pedágio não devido, tarifa/mensalidade sem prestação → devolução **em dobro**, salvo engano justificável. |
| **Dano moral** | CDC art. 6º VI + art. 14 | Negativação indevida, pontos na CNH por erro, risco de suspensão do direito de dirigir → dano moral (mais sólido com inscrição indevida ou efeito concreto na CNH). |

## 4. O que produzir
- **Reclamação administrativa/extrajudicial** primeiro (SAC/ouvidoria, Consumidor.gov.br) — gera prova e, muitas vezes, resolve.
- **Ação cível** (reparatória/declaratória): pedir cancelamento da cobrança + repetição em dobro (art. 42 §ú) + dano moral + inversão do ônus (art. 6º VIII) + tutela de urgência para baixar negativação/segurar os pontos. Fecha em `acao-reparatoria-transito` / `tutela-urgencia-transito`.
- **Provas:** extrato da tag na data/hora, contrato/termo de adesão, comprovantes de recarga, histórico de passagens, protocolos de reclamação.

## 5. Postura honesta
- **Repetição em dobro (art. 42 §ú):** o STJ firmou que **independe de prova de má-fé** do fornecedor, com **modulação temporal**. 🟡 **PROIBIDO citar número/relator/data do leading case (EAREsp 676.608/RS) sem verificação** — anchor a confirmar via `validador-transito`/`juris-adv-os` antes de a peça sair. A tese é sólida; o número não foi verificado nesta base.
- **Dano moral não é automático:** sem inscrição indevida ou efeito concreto na CNH, o pedágio cobrado errado tende a ser tratado como **mero aborrecimento**. Calibrar a expectativa do cliente.
- Cancelar a cobrança no cível **não cancela a multa** de trânsito automaticamente — precisa da defesa administrativa em paralelo (`infracao-de-pedagio-e-free-flow`).

## 6. Cross-link (soft)
`infracao-de-pedagio-e-free-flow` (frente administrativa gêmea) · `acao-reparatoria-transito` · `tutela-urgencia-transito` · `protocolo-p4-transito` (cruza administrativo × cível × consumo). Cobrança indevida/negativação → `bancario`/consumo; liquidação do dano → `calculosjudiciais-adv-os`.

## 7. Fechamento obrigatório
A peça cível **fecha por `suprema-corte-transito`** (R1 fatos · R2 fundamentação CDC vigente · R3 prazos · R4 competência/valor da causa) **+ `validador-transito`** (confere os artigos do CDC e trava o 🟡 do EAREsp). Nenhuma citação de jurisprudência entra sem WebFetch real.
