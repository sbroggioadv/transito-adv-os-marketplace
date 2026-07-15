# Processo Administrativo de Trânsito — fluxo, prazos e armadilhas

> Anexo de referência do plugin **transito-adv-os**. O coração operacional do produto: em que fase o cliente está, qual o prazo, qual peça. Base: **Res. 918/2022** (multa) + CTB arts. 280–290 + Lei 9.873/99 (prescrição).
> **Legenda:** ✅ confirmado em fonte primária · 🟡 a confirmar no validador antes de citar · 🔴 mito/pegadinha a desmentir.
> **Regra de triagem crítica:** o plugin **sempre** pergunta em qual fase o cliente está (recebeu **NA** ou **NP**? aderiu ao **SNE**?) **antes** de escolher a peça. NA e NP são notificações **distintas**.

---

## 1. O FLUXO (mapa de prazos)

```
INFRAÇÃO  (AIT lavrado no ato — art. 280 CTB; sem prazo p/ lavrar)
   │
   ▼
[1] NOTIFICAÇÃO DA AUTUAÇÃO (NA) ── órgão tem ATÉ 30 DIAS CORRIDOS da infração
   │   ↳ estourou 30 dias? → ARQUIVAMENTO do AIT (art. 4º §1º Res.918 / 281 p.ú. II CTB) ✅ TESE FORTE
   ▼
[2] DEFESA DA AUTUAÇÃO (= "defesa prévia") ── condutor: prazo NÃO INFERIOR A 30 DIAS da NA (art. 4º §2º)
   │   ↳ no MESMO prazo: INDICAÇÃO do real condutor (art. 5º Res.918) ✅
   ▼
[3] JULGAMENTO da defesa pela autoridade autuadora (art. 9º Res.918)
   │   ↳ acolhida → AIT cancelado e arquivado (§1º) ✅
   │   ↳ indeferida/não apresentada → aplica penalidade + expede NP:
   │        • ATÉ 180 DIAS da infração (sem defesa prévia)  — §2º ✅
   │        • ATÉ 360 DIAS da infração (COM defesa prévia)  — §3º ✅
   ▼
[4] NOTIFICAÇÃO DA PENALIDADE (NP) de multa (art. 12 Res.918 / art. 282 CTB)
   │   ↳ traz valor, desconto (art. 284) e DATA DE VENCIMENTO = mesma data-limite do recurso
   ▼
[5] RECURSO À JARI (1ª instância) ── prazo até o VENCIMENTO da NP (mín. 30 dias) — art. 285 CTB ✅
   │   ↳ efeito suspensivo: enquanto pende, sem restrição/pontos (arts. 13 e 18 Res.918) ✅
   ▼
[6] RECURSO ao CETRAN / CONTRANDIFE (2ª instância) ── 30 dias da decisão da JARI — arts. 288/289 CTB 🟡
   │   ↳ SEM depósito prévio (SV 21 STF) ✅
   ▼
ESGOTADA a via administrativa → só então pontos vão ao RENACH (art. 18 Res.918) ✅
   → resta a via JUDICIAL (anulatória / mandado de segurança)
```

### Tabela de prazos — fonte por linha

| Etapa | Prazo | Fundamento | Âncora |
|---|---|---|---|
| Lavratura do AIT | no ato; **sem prazo legal** | art. 280 CTB · art. 3º Res.918 | ✅ |
| Órgão expedir a **NA** | **até 30 dias corridos** da infração | art. 4º caput Res.918 · art. 281 p.ú. II CTB | ✅ |
| Estouro do prazo da NA | **arquivamento** do AIT (cancelamento por perda de prazo, não "prescrição") | art. 4º §1º Res.918 | ✅ |
| **Defesa da autuação** + **indicação** | **não inferior a 30 dias** da NA | art. 4º §2º + art. 5º Res.918 | ✅ |
| NA anterior a 12/04/2021 | não inferior a **15 dias** | art. 4º §6º Res.918 | ✅ |
| Expedir **NP** — sem defesa prévia | **até 180 dias** da infração | art. 9º §2º Res.918 | ✅ |
| Expedir **NP** — com defesa prévia | **até 360 dias** da infração | art. 9º §3º Res.918 | ✅ |
| Recurso à **JARI** | até o **vencimento da NP** (mín. 30 dias) | art. 285 CTB · art. 15 Res.918 | ✅ |
| Recurso à **2ª instância (CETRAN)** | **30 dias** da ciência da decisão JARI | arts. 288/289 CTB · art. 16 Res.918 | 🟡 confirmar nº na 900/2022 |
| Prescrição da ação punitiva | **Lei 9.873/1999** (5 anos; 3 anos intercorrente) | art. 36 Res.918 | ✅ (remete) / 🟡 (anos) |

---

## 2. AS TRÊS ARMADILHAS DE PRAZO (perda de direito por desatenção)

### 🪤 Armadilha nº 1 — dias CORRIDOS, não úteis 🔴
**Art. 29 Res. 918/2022:** a contagem (condutor, defesa da autuação, recursos) é em **"dias consecutivos" (= corridos)** — exclui o dia da notificação, inclui o do vencimento, prorroga ao 1º dia útil se cair em fim de semana/feriado. Material de internet que fala "dias úteis" está **ERRADO** para a 918/2022. **Contar sempre dias corridos** por padrão; só "úteis" se a norma específica daquele ato disser expressamente. Fonte real de perda de prazo.

### 🪤 Armadilha nº 2 — NA ≠ NP (duas notificações distintas)
"Defesa prévia" (defesa da autuação, contra a **NA**) é fase **diferente** do "recurso" (contra a **NP**). Erro comum: achar que só existe "recurso da multa". Perder a defesa da autuação (30 dias da NA) **não impede** o recurso à JARI, mas queima a 1ª janela — a mais barata e a mais fácil de anular por vício da NA. **Triar a fase antes de escolher a peça.**

### 🪤 Armadilha nº 3 — SNE presume ciência em 30 dias
Na notificação eletrônica (SNE/CDT), o autuado é considerado **notificado 30 dias após a inclusão no sistema, mesmo sem abrir** (art. 10 §6º Res.918, por analogia — 🟡). Quem aderiu ao SNE e não acompanha o app vê o prazo correr sem saber. **Perguntar sempre "você aderiu ao SNE?"** e ajustar o dies a quo.

---

## 3. INDICAÇÃO DO REAL CONDUTOR — prazo e requisitos (art. 257 §7º CTB + art. 5º Res.918)

- **Prazo:** o **mesmo da defesa da autuação** — não inferior a **30 dias** da NA (art. 4º §2º + art. 5º). Os "15 dias" só valem para NA anteriores a 12/04/2021 (art. 4º §6º).
- **Requisitos formais (art. 5º):** formulário corretamente preenchido, **sem rasuras**, com **assinaturas ORIGINAIS** do proprietário (inciso III) **e** do condutor indicado (inciso IV); dados completos do indicado (nome, CNH, identidade, CPF); placa + nº do AIT.
- **Não indicou / indicou em desacordo (art. 6º):** o **proprietário** responde (multa + pontos dele).
- **PJ que não indica (art. 7º + art. 257 §8º):** **NIC** — multa autônoma além da originária (PJ não recebe pontos). 🟡 multiplicador exato (2×?) a confirmar.
- 🪤 **art. 5º §2º:** indicar condutor que se enquadra no art. 162 (sem habilitação) → lavra-se AIT ao proprietário por **art. 163** (entregar direção a não habilitado). Indicação errada gera multa nova.
- **Posse (art. 8º):** locação/leasing/comodato só transfere a notificação se o contrato tiver **≥ 180 dias**.

---

## 4. EFEITO SUSPENSIVO E O TRUNFO DOS PONTOS (arts. 13 e 18 Res.918) ✅

- **Art. 13** — até o vencimento da NP ou enquanto houver efeito suspensivo, **sem restrição** no veículo (licenciamento/transferência liberados).
- **Art. 18** — pontos só vão ao RENACH **depois de esgotados os recursos**. ⇒ **recorrer SEGURA os pontos**: enquanto o processo corre, os pontos não entram no prontuário. Argumento de ouro para quem está perto do limite de suspensão (20/30/40).

---

## 5. DESCONTOS — o trade-off (arts. 20 e 21 Res.918) ✅

- **20% (paga 80%)** — pagamento até o vencimento, sem SNE (art. 20).
- **40% (paga 60%)** — recebeu a NP **pelo SNE** e **renuncia** a defesa/recurso (art. 21 c/c art. 284 §1º CTB).
- ⚠️ O desconto de 40% **exige renúncia ao recurso**. Multa com tese de nulidade → recorrer (segura pontos + pode anular) tende a valer mais. Decisão informada pelo `parecer-transito`.

---

## 6. PRESCRIÇÃO — Lei 9.873/1999 (art. 36 Res.918) ✅ / 🟡

- **Pretensão punitiva (multa, suspensão, cassação):** prescreve em **5 anos** por **aplicação analógica da Lei 9.873/1999, art. 1º** (contados do cometimento da infração). 🟡 **sem súmula nem tema repetitivo específico de trânsito** — citar como "jurisprudência consolidada por analogia à Lei 9.873/99", nunca como súmula.
- **Prescrição intercorrente:** processo parado **> 3 anos** (Lei 9.873/99, art. 1º §1º). 🟡 aplicação ao trânsito **em construção** — bom argumento, campo em disputa, retroatividade controvertida.
- 🔴 **NUNCA** citar o **Tema 1.293 STJ** como prescrição intercorrente de trânsito — ele é **ADUANEIRO** (armadilha de URL). Ver `jurisprudencia-transito.md`.

---

## 7. CHECKLIST DE DOCUMENTOS (o fosso na prática)

1. **AIT** — conferir campos do art. 280.
2. **NA** — conferir **data de expedição** vs 30 dias.
3. **NP** — conferir data de vencimento (= prazo do recurso).
4. **Formulário de indicação** (se houver) — assinaturas originais + CNH do indicado.
5. **Certificado de aferição INMETRO** do equipamento (radar/etilômetro) — **requerer ao órgão** se não veio.
6. **Fotos/imagens** da infração e do local (sinalização — art. 90).
7. **Extrato do prontuário/RENACH** (pontos, processos de suspensão/cassação em curso).
8. **Comprovante de adesão ao SNE** (define o dies a quo).
9. **Provas de álibi** (nota fiscal, pedágio/tag, GPS) para erro de local/data.
