# Metodologia do plugin transito-adv-os

> Anexo mestre do plugin **transito-adv-os**. O "como pensar" antes do "o que escrever": pilares, fluxo triagem→peça, as 7 verdades duras que o plugin vende (contra o folclore de balcão), as correções travadas e a lista 🟡 proibida.
> É o arquivo que o `transito-master`, o `anti-alucinacao-transito` e a `suprema-corte-transito` consultam para não escorregar.

---

## 1. OS PILARES (herança da família Adv-OS)

1. **Porta única** — todo caso entra pelo `transito-master`, que triara e roteia. Toda peça fecha pela `suprema-corte-transito` (R1–R4) + `validador-transito`.
2. **Standalone-first** — recursos e peças judiciais modelados internamente (espinha do civel); zero dependência de API em runtime.
3. **Anti-alucinação por design** — nenhuma súmula/tema/dispositivo/prazo/resolução com selo ✅ entra em peça sem verificação; itens 🟡 entram **sempre** como "a confirmar", nunca como fato.
4. **Lei VIGENTE 2026** — inclui a **Lei 15.428/2026** (pós-corte de treino). Captura de fonte oficial supera o treino do modelo.
5. **Postura honesta** — nulidades ranqueadas FORTE/MÉDIA/FRACA; rachas e pendências declarados; nunca prometer "anula qualquer multa".
6. **Despersonalizado** — autoria IA Combativa; o advogado-cliente configura o próprio escritório via `/start-transito`.

---

## 2. O FLUXO TRIAGEM → PEÇA

```
CASO
  │
  ▼
[TRIAGEM CRÍTICA]  (transito-master / triagem-transito)
  │  1. Em que FASE está?  ── recebeu NA (autuação) ou NP (penalidade)?  ⇦ decide a peça
  │  2. Aderiu ao SNE?     ── ajusta o dies a quo (ciência presumida 30 dias)
  │  3. Qual o EIXO?       ── multa/defesa · CNH (suspensão/cassação/bloqueio) · bafômetro
  │                            · pedágio/consumo · veículo (remoção/leilão) · judicial
  │  4. Data da infração?  ── antes ou depois de 12/04/2021 (regime da Lei 14.071)?
  ▼
[TRILHA]
  • Recebeu NA  → defesa-da-autuacao  (ou indicacao-de-condutor)
  • Recebeu NP  → recurso-jari → recurso-cetran
  • CNH em risco → sistema-de-pontuacao / processo-suspensao / cassacao / bloqueio
  • Bafômetro   → bafometro-e-recusa-administrativa
  • Pedágio/tag → infracao-de-pedagio-e-free-flow / tag-e-cobranca-indevida / concessionaria
  • Veículo     → remocao-apreensao-e-leilao / licenciamento-crlv-e-comunicacao-venda
  • Esgotou adm → judicial (anulatoria / mandado-de-seguranca / tutela / reparatoria)
  ▼
[ANÁLISE DO AIT]  (analise-auto-de-infracao)
  • pente fino art. 280 · confronto de prazos · confronto de notificações · prova de álibi
  • teses ranqueadas FORTE > MÉDIA > FRACA (desmentir o mito da assinatura)
  ▼
[PEÇA]  (skill da trilha)
  ▼
[FECHAMENTO]  suprema-corte-transito (R1–R4) + validador-transito
  • R1 fatos/fase/prazos · R2 fundamentação vigente · R3 prazos corridos + dies a quo · R4 forma/competência/via
```

---

## 3. AS 7 VERDADES DURAS (o plugin vende a verdade vigente)

1. **NÃO é "20 pontos e perde a CNH".** Desde 12/04/2021 (Lei 14.071/2020) é **escalonado 20/30/40** conforme nº de gravíssimas em 12 meses (art. 261). EAR = 40 fixo.
2. **Resoluções CONTRAN foram CONSOLIDADAS em 2022.** Usar **918/2022** (notificação/multas), **900/2022** (defesa+recurso), **931/2022** (SNE), **901/2022** (CETRAN). **NUNCA** as revogadas (619/2016, 299/2008, 692/2017, 622/2016). Suspensão/cassação = **723/2018 alterada pela 844/2021**.
3. **art. 262 CTB está REVOGADO** (Lei 13.281/2016). Remoção ao depósito = **art. 271**; leilão = **art. 328** (Lei 13.160/15). Não existe mais "penalidade de apreensão".
4. **Lei 15.428/2026 (05/06/2026, pós-corte de treino):** CNH em meio físico OU digital com **fé pública** (art. 159 reescrito) + **renovação automática via RNPC** (art. 268-A §7º). Reforça a tese contra autuação por "falta de porte" (art. 232) quando havia CNH-e.
5. **Prazos em dias CORRIDOS** (não úteis — art. 29 Res.918; "dias úteis" é erro de internet que faz perder prazo) · **NA ≠ NP** (duas fases distintas — triar em qual o cliente está) · **SNE presume ciência 30 dias** após inclusão, mesmo sem abrir.
6. **TRUNFO (art. 18 Res.918):** os pontos só vão ao RENACH **após esgotados os recursos** → **recorrer SEGURA os pontos** (ouro para quem está perto do limite de suspensão).
7. **Postura honesta:** nulidades do AIT ranqueadas FORTE/MÉDIA/FRACA; o **"falta de assinatura anula" é MITO** (tese fraca — desmentir); nunca prometer "anula qualquer multa".

---

## 4. AS CORREÇÕES TRAVADAS (o que a pesquisa desmentiu)

- **Súmula 434 STJ ≠ "defesa prévia".** Ela diz que o **pagamento NÃO inibe** a discussão judicial. Defesa prévia = **Súmula 312 STJ + CTB art. 281 p.ú.** (+ CF art. 5º LV).
- **Tema 1.293 STJ é ADUANEIRO, não trânsito.** Nunca citar como prescrição intercorrente de trânsito. Prescrição de trânsito = **Lei 9.873/99 por analogia** (sem súmula/tema de trânsito).
- **"CNH sem autoescola" (2025) = PROPOSTA, não vigente.** A Res. 1020/2025 não é isso; curso em CFC segue obrigatório.
- **Tema 1.122 STJ só cobre animais DOMÉSTICOS** — não estender a silvestres (aí é responsabilidade do Estado).
- **"Apreensão" no texto de alguns tipos (162 I, 230, 173–175)** — resíduo legislativo; **não pode ser aplicada** (art. 262 revogado).

---

## 5. LISTA 🟡 PROIBIDA (nunca afirmar sem verificação — o guard bloqueia, roteia ao validador)

Estes itens **NÃO entram em peça como fato**. Entram como "a confirmar" e são roteados ao `validador-transito`:
- **Multiplicadores exatos** de gravíssima (NIC 2× do art. 257 §8º; toxicológico 5× do art. 165-B; dobro na reincidência do 165).
- **Número da portaria INMETRO** do etilômetro e periodicidade da verificação metrológica.
- **Prazos exatos da Res. 900/2022** (2ª instância — nº de dias) e da **Res. 844/2021** (suspensão/cassação — defesa/recurso).
- **Número de anos da prescrição** aplicado ao trânsito (5 / 3 por analogia à Lei 9.873/99) — citar como analogia, não como prazo do CTB.
- **Número da resolução CONTRAN/ANTT do free flow** e o prazo da janela de regularização.
- **Rol fechado das infrações autossuspensivas** (art. 165, 165-A, 173–175, 218 III etc. — confirmar cada uma).
- **Faixa exata do prazo de suspensão** (meses) do art. 261 e a regra EAR de reciclagem preventiva.
- **Valor final de multa** — sempre conferir o multiplicador no tipo antes de dar número.
- **Números de REsp/EAREsp** marcados 🟡 (Tema 1.122 = REsp 1.908.738/SP; repetição em dobro = EAREsp 676.608/RS) — exigem **WebFetch real** antes de entrar em peça.
- **Composição do CONTRAN (art. 10)** — mexida por 14.071/2020 e 14.599/2023; conferir antes de afirmar quem preside.

---

## 6. MAPA DOS ANEXOS context/

| Tema | Arquivo |
|---|---|
| Dispositivos nucleares do CTB | `ctb-9503-97.md` |
| Reformas (14.071 / 14.599 / 15.428) | `leis-14071-14599-15428.md` |
| Processo de multa verbatim (o fosso) | `resolucao-918-2022.md` |
| Resoluções vigentes × revogadas | `resolucoes-contran-mapa.md` |
| Fluxo, prazos e armadilhas | `processo-adm-fluxo-prazos.md` |
| Nulidades do AIT ranqueadas | `nulidades-do-ait.md` |
| Súmulas/temas + rachas + correções | `jurisprudencia-transito.md` |
| Pedágio, free flow e consumo | `pedagio-e-consumo.md` |
| Veículo: remoção, leilão, venda | `veiculo-remocao-leilao.md` |
| Metodologia (este arquivo) | `metodologia-transito.md` |
