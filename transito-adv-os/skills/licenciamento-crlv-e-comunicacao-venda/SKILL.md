---
name: licenciamento-crlv-e-comunicacao-venda
description: Trata licenciamento anual atrasado (art. 230), CRLV/CRLV-e digital (Res. CONTRAN 809/2020) e o campo minado da comunicação de venda — art. 134 CTB (o vendedor responde solidariamente por MULTAS do comprador até comunicar) com a Súmula 585 STJ (exclui IPVA pós-venda, salvo lei estadual — Tema 1.118). Use quando o cliente está com licenciamento vencido, foi multado por não licenciar, tem CRLV digital e foi autuado por "falta de documento", vendeu o carro e continua recebendo multas/pontos do comprador, ou pergunta "vendi e não passei o carro, e agora?", "recebo multa de carro que não é mais meu", "posso ser cobrado de IPVA depois que vendi?".
---

# Licenciamento, CRLV-e & Comunicação de Venda — art. 230, 232 e 134 CTB

## 1. Quando ativa / trilha
Dois eixos frequentes: (a) **licenciamento/CRLV** — condutor com licenciamento vencido, autuado, ou penalizado por "falta de documento" mesmo tendo CRLV-e; (b) **comunicação de venda** — vendedor que não comunicou a transferência e segue recebendo multas/pontos (ou cobrança de IPVA) do comprador. Triar qual eixo e a fase (NA/NP) → `triagem-transito`.

## 2. Licenciamento e CRLV-e (base ancorada ✅)
- **CRLV/CRLV-e** — o Certificado de Registro e Licenciamento de Veículo tem versão **digital com fé pública** (Res. CONTRAN **809/2020**), hospedada na **Carteira Digital de Trânsito (CDT)**.
- **Art. 230 CTB** — conduzir veículo **não licenciado / registro vencido**: **gravíssima**, multa + medidas administrativas.
- **Art. 232** — conduzir **sem o documento de porte obrigatório**: **leve**, multa + retenção até apresentar.
- 🟡 **Tese anti-defasagem (Lei 15.428/2026):** CNH e CRLV **digitais** têm **fé pública** e equivalem a documento de identidade (art. 159 caput, redação Lei 15.428/2026). **Tese contra autuação por art. 232** ("falta de porte") quando o condutor **tinha o documento digital** no app. Confirmar a redação vigente via `validador-transito` antes de citar a Lei 15.428.

## 3. Comunicação de venda — art. 134 CTB + Súmula 585 STJ ✅
- **Art. 134 CTB** (vigente, **não** revogado pela Lei 14.071/2020): o antigo proprietário deve **comunicar a transferência** ao órgão de trânsito. Sem comunicar, responde **solidariamente pelas PENALIDADES (multas/infrações)** impostas **até a data da comunicação**. Natureza **administrativa** — **não** é responsabilidade tributária.
- **Súmula 585 STJ** ✅ (DJe 01/02/2017, vigente): "A responsabilidade solidária do ex-proprietário, prevista no art. 134 do CTB, **não abrange o IPVA** incidente sobre o veículo no período **posterior** à alienação." → sem comunicar, o vendedor responde por **multas**, mas **NÃO** pelo IPVA posterior à venda.
- **Exceção — Tema 1.118 STJ / Jur. em Teses ed. 112, tese 6** ✅: **havendo previsão em lei estadual**, admite-se a solidariedade do ex-proprietário pelo **IPVA**, excepcionando a Súmula 585. → **checar a lei estadual do IPVA** (ex.: SP) antes de garantir isenção.

## 4. O que produzir
- **Licenciamento:** defesa/recurso da autuação (rito `defesa-da-autuacao`→`recurso-jari`→`recurso-cetran`); tese do CRLV-e/fé pública quando cabível; regularização do licenciamento.
- **Comunicação de venda:** **anulatória de multas** e/ou **declaratória de inexistência de relação jurídica** para as infrações posteriores à venda; contra IPVA, discussão à luz da Súmula 585 + lei estadual.
- **Provas da data real da tradição:** recibo/**ATPV-e** com reconhecimento de firma, contrato, comprovantes de pagamento, e-mails, testemunhas.

## 5. Postura honesta
- Administrativamente, o DETRAN tende a usar a **data da comunicação no sistema** como marco objetivo do art. 134 (não a data real da venda). 🟡 Judicialmente há **mitigação** (ex.: TJDFT) quando comprovada a alienação anterior à infração e a ausência de posse — a responsabilidade do art. 134 **não é absoluta**, mas não é vitória garantida.
- **IPVA:** a Súmula 585 exclui o IPVA pós-venda, **salvo lei estadual** (Tema 1.118) → nunca prometer isenção sem checar a lei do estado.
- **Prevenção que a skill martela:** comunicar a venda **imediatamente** (idealmente o comprador registra a ATPV-e/transferência) — é o que corta a solidariedade na origem.

## 6. Cross-link (soft)
`defesa-da-autuacao`/`recurso-jari`/`recurso-cetran` (rito administrativo) · `acao-anulatoria-multa-infracao` (multas do comprador) · `mandado-de-seguranca-transito` (recusa de licenciar por multa não notificada — Súmula 127) · `remocao-apreensao-e-leilao` (veículo recolhido por licenciamento). IPVA/lei estadual → `tributario` (fora do escopo do plugin).

## 7. Fechamento obrigatório
Toda peça **fecha por `suprema-corte-transito`** (R1 fatos/data da tradição · R2 fundamentação — art. 134, Súmula 585, Tema 1.118; CRLV-e/Lei 15.428 · R3 prazos · R4 via/competência) **+ `validador-transito`** (trava a Súmula 585, o Tema 1.118, a Lei 15.428 e a lei estadual do IPVA). Nenhuma súmula entra sem WebFetch real.
