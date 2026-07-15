# Resoluções CONTRAN — mapa vigentes × revogadas (anti-armadilha)

> Anexo de referência do plugin **transito-adv-os**. A "grande consolidação" de 2022 reorganizou o processo administrativo de trânsito e revogou dezenas de resoluções antigas. **Citar a consolidadora, nunca a revogada** é um dos maiores diferenciais anti-defasagem do plugin.
> Captura oficial (gov.br/transportes + PDFs DOU) 2026-07-15.
> **Legenda:** ✅ vigente/confirmado · 🟡 vigente mas conferir (não consolidada em 2022, citada em normas recentes) · 🔴 REVOGADA — nunca citar como norma vigente.

---

## 1. TABELA MESTRA — o que citar por tema

| Tema | ✅ VIGENTE (citar esta) | Data | 🔴 REVOGADAS (NUNCA citar) |
|---|---|---|---|
| Procedimentos de multas / **notificação NA e NP** / arrecadação | **918/2022** | 28/03/2022 | 156/04, 424/12, 442/13, 574/15, **619/16**, 697/17, 736/18, 845/21 |
| **Defesa prévia + recurso** (1ª e 2ª instâncias) contra advertência e multa | **900/2022** | 09/03/2022 | **299/08**, **692/17** |
| **SNE — Sistema de Notificação Eletrônica** (base art. 282-A) | **931/2022** | 28/03/2022 | **622/16**, 636/16 |
| Regimento Interno / gestão dos **CETRAN e CONTRANDIFE** (2ª instância) | **901/2022** | 28/03/2022 | 688/17, 732/18, 779/19 |
| **Suspensão do direito de dirigir e cassação** — procedimento | **723/2018** (alterada pela **844/2021**) | 06/02/2018 | — 🟡 não consolidada em 2022; segue vigente e citada por DETRANs |
| **JARI** — Regimento Interno / composição mínima | **357/2010** | 02/08/2010 | — 🟡 anterior à onda 2022; conferir vigência |
| **MBFT — Manual Brasileiro de Fiscalização de Trânsito** | **985/2022** | 2022 | **925/2022** (que já revogara 371/10, 389/11, 401/12, 428/12, 480/14, 497/14, 561/15, 858/21, 880/21) |
| **CNH — especificações, produção e expedição** (base CNH-e/digital) | **886/2021** | 13/12/2021 | 133/02, 598/16, 650/17, 668/17, 679/17, 684/17, 718/17, 747/18, 775/19, 850/21 |
| **CRV/CRLV digital** (documentos digitais de veículo) | **809/2020** | 15/12/2020 | — ✅ |
| **Etilômetro / bafômetro** — requisitos e fiscalização | **432/2013** | 2013 | — 🟡 base do art. 277; conferir alterações recentes |
| Habilitação / formação de condutor / expedição de documentos | **1020/2025** | 01/12/2025 | 🟡 conferir o que revoga; **NÃO é a "CNH sem autoescola"** |

---

## 2. AS QUATRO REVOGADAS QUE MAIS APARECEM POR ENGANO 🔴

| 🔴 Resolução | Tema que tinha | Substituta vigente |
|---|---|---|
| **619/2016** | notificação de autuação e penalidade | **918/2022** |
| **299/2008** | defesa prévia e recurso | **900/2022** |
| **692/2017** | recursos (JARI/CETRAN) | **900/2022** |
| **622/2016** | notificação eletrônica | **931/2022** |

Citar qualquer uma delas como norma vigente = **erro grave** (a defesa fica ancorada em base revogada e pode ser desqualificada). O `validador-transito` bloqueia.

---

## 3. NOTAS DE ESCOPO E ARMADILHAS

- **Suspensão/cassação NÃO foi consolidada em 2022.** O rito próprio segue na **723/2018 (alterada pela 844/2021)** — norma diferente da 918/2022 (que é só multa). Não misturar prazos dos dois processos. 🟡 confirmar vigência 2026 e prazos exatos no texto da 844/2021 antes de citar (o dossiê registrou menção a Deliberação CONTRAN 278/2026 — checar se há mudança recente).
- **CDT — Carteira Digital de Trânsito:** é o **aplicativo** oficial (SENATRAN/SERPRO) que agrega **CNH-e** (886/2021) e **CRLV-e** (809/2020). 🟡 **Não citar "uma resolução do CDT" isolada** — citar as normas dos documentos que ele hospeda + a Portaria SENATRAN de instituição do app (conferir número antes de citar).
- **1020/2025 ≠ "CNH sem autoescola".** É norma de habilitação/expedição; **não** extingue a autoescola. A "CNH mais barata / sem CFC" é **proposta**, não direito vigente. Ver `leis-14071-14599-15428.md` §4.
- **Free flow (pedágio sem cancela):** a janela de regularização existe (Resolução CONTRAN/ANTT), mas o **número exato não foi capturado** — 🟡, roteia ao validador. Ver `pedagio-e-consumo.md`.

---

### Fontes oficiais (validador confere ao vivo)
- Lista oficial com revogações: `https://www.gov.br/transportes/pt-br/assuntos/transito/conteudo-Senatran/resolucoes-contran`
- SNE — legislação: `https://centraldeajuda.serpro.gov.br/sne/legislacao/`
