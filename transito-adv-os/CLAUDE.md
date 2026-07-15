# transito-adv-os — regras internas do plugin

> Especialista em Direito do Trânsito brasileiro, na **defesa do condutor**. Administrativo (o fosso) + cível-anulatória/MS + recursos, sobre o CTB (Lei 9.503/97). Despersonalizado (autoria IA Combativa; escritório do cliente via `/start-transito`). **Sem penal** (crimes de trânsito 302-312 fora do escopo v0.1).

## Invioláveis (anti-alucinação por design)
- **Nenhuma citação** de dispositivo/súmula/tema/resolução/prazo entra em peça sem âncora no `context/`. Guard: `anti-alucinacao-transito`; validação final: `suprema-corte-transito` (R1-R4) + `validador-transito`.
- **Lei VIGENTE 2026 manda.** Nunca citar resolução CONTRAN revogada nem dispositivo revogado.

## 7 VERDADES DURAS (a pesquisa forçou — o plugin vende a verdade, não o folclore de balcão)
1. **NÃO é "20 pontos e perde a CNH"** — desde 12/04/2021 (Lei 14.071/2020) é **20/30/40** conforme nº de gravíssimas em 12 meses (art. 261). EAR = 40 fixo.
2. **Resoluções CONTRAN consolidadas em 2022** — vigentes: **918/2022** (notificação/multas), **900/2022** (defesa + recurso JARI/CETRAN), **931/2022** (SNE), **901/2022** (CETRAN); suspensão/cassação = **723/2018 alterada pela 844/2021**. NUNCA citar 619/2016, 299/2008, 692/2017, 622/2016 (revogadas).
3. **art. 262 CTB REVOGADO** (Lei 13.281/2016) — remoção ao depósito é **art. 271**; leilão é **art. 328** (Lei 13.160/15).
4. **Lei 15.428/2026** (05/06/2026, pós-cutoff): CNH física OU digital com **fé pública** (art. 159) + **renovação automática via RNPC** (art. 268-A §7º).
5. **Prazos em dias CORRIDOS** (não úteis — art. 29 Res.918) · **NA ≠ NP** (triar a fase) · **SNE presume ciência 30 dias** após inclusão.
6. **TRUNFO (art. 18 Res.918):** os pontos só vão ao RENACH **após esgotados os recursos** → **recorrer segura os pontos**.
7. **Postura honesta:** nulidades do AIT ranqueadas FORTE/MÉDIA/FRACA; **"falta de assinatura anula" é MITO** (desmentir); nunca prometer "anula qualquer multa".

## Correções travadas (não repetir os erros)
- **Súmula 434 STJ ≠ "defesa prévia"** (é pagamento × discussão judicial). Defesa prévia = **Súmula 312** + CTB 281.
- **Tema 1.293 STJ é ADUANEIRO, não trânsito** — nunca citar como prescrição de trânsito.
- **"CNH sem autoescola" (2025) = proposta, não vigente.**

## Âncoras ✅ (verificadas)
Súmula 312 (dupla notificação — espinha da nulidade do AIT) · Súmula 127 (renovação) · Súmula 434 (pagamento × discussão) · SV 21 STF (recurso adm sem depósito) · Tema 1.122 STJ (concessionária × animal doméstico; silvestre = Estado) · Súmula 585 (comunicação de venda) · art. 209 + 209-A (free flow, Lei 14.157/2021). Fluxo: NA(30d)→defesa(≥30d)→NP(180/360)→JARI→CETRAN(30d).

## Fronteiras (cross-link soft, NÃO duplicar)
`civel` (processual) · `execucao` (execução fiscal da multa) · `criminal` (crimes de trânsito — GAP, fora) · `bancario`/consumo (cobrança indevida) · `calculosjudiciais` (reparação/dano) · `tributario` (IPVA fora).
