---
name: apelacao-transito
description: "Redige apelacao (CPC 1.009-1.014) contra sentenca em acao anulatoria de multa/infracao, mandado de seguranca ou acao reparatoria de transito — prazo de 15 dias UTEIS (nao os dias corridos do administrativo), preparo/desercao (1.007), efeito suspensivo como regra (1.012) com a peculiaridade do MS, causa madura (1.013 §3), sem honorarios em MS (Sumula 105 STJ/512 STF). Use quando disser apelar, apelacao, recorrer da sentenca, sentenca improcedente na anulatoria/MS, perdi a anulatoria de multa, efeito suspensivo da apelacao."
---

# APELACAO-TRANSITO — CPC 1.009-1.014

> Camada 7 (recursos). Recurso contra a **sentenca** nas acoes judiciais de transito. STANDALONE — carrega o espinhaco do CPC aqui, nao depende do plugin civel.

## Anexos / skills-fonte
- `context/metodologia-transito.md` (estilo e regras de ouro).
- `base-processual-judicial-transito` (espinha CPC filtrada + MS Lei 12.016/09) — cross-link.
- `jurisprudencia-transito` para toda tese de merito (Sumula 312/127/434/585, SV 21, Tema 1.122).

## Quando ativar
- Houve **sentenca** (485 terminativa ou 487 definitiva) em `acao-anulatoria-multa-infracao`, `mandado-de-seguranca-transito`, `anulatoria-suspensao-cassacao` ou `acao-reparatoria-transito` e a parte quer recorrer.
- Gatilhos: "apelar", "recorrer da sentenca", "perdi a anulatoria/MS", "improcedente", "efeito suspensivo", "causa madura".

## 🔴 Prazo — a pegadinha nº1 do transito
Recurso **judicial** conta em **dias UTEIS** (CPC 219). Isso **contradiz** o administrativo (dias corridos, art. 29 Res. 918/2022). Ao migrar da esfera adm para a judicial, **trocar o regime de contagem** — errar aqui perde o recurso. Sempre declarar qual esfera.

## Metodologia
1. **Cabimento (1.009):** da sentenca. Interlocutorias **nao agravaveis** nao precluem e vao em **preliminar de apelacao ou contrarrazoes** (§1) — levantar as pertinentes (ex.: indeferimento de prova pericial do radar).
2. **Tempestividade:** **15 dias uteis** (1.003 §5); dobro para a Fazenda (30) quando ela apela — comum no polo passivo (DETRAN/DER/Municipio). Regime judicial, nao administrativo.
3. **Preparo (1.007):** comprovar preparo + porte no ato, sob pena de **desercao**; insuficiencia -> 5 dias para suprir (§2); ausencia -> dobro (§4). **Gratuidade** afasta (requerer se cabivel). **Atencao MS:** custas incidem, mas so ha condenacao em honorarios fora dele.
4. **Efeito suspensivo (1.012):** regra geral. **MS:** a sentenca concessiva pode ser **executada provisoriamente** (art. 14 §3 Lei 12.016/09, salvo vedacoes) — a apelacao da autoridade nao segura sozinha a liberacao da CNH/licenciamento ja deferida; sustentar isso.
5. **Error in procedendo x in judicando:** preliminares de nulidade (procedendo — ex.: cerceamento por indeferir pericia do etilometro/radar) + merito (judicando — atacar cada fundamento da sentenca).
6. **Causa madura (1.013 §3):** requerer julgamento imediato do merito quando o tribunal reformar sentenca 485 ou suprir omissao — util para nao voltar a estaca zero na anulatoria.
7. **Honorarios recursais (85 §11):** o tribunal majora — **MAS em mandado de seguranca NAO ha condenacao em honorarios** (Sumula 105 STJ / 512 STF, confirmar no validador). Nao pedir majoracao em MS.

## Entrega obrigatoria final
- Peticao de interposicao + razoes combatendo cada fundamento (preliminares + merito) + pedido de efeito adequado.
- Comprovacao/calculo de preparo (ou gratuidade) + parecer de tempestividade em **dias uteis** + nota sobre causa madura e ausencia de honorarios se MS.

## Postura honesta
Anulatoria/MS de transito frequentemente esbarra em **materia de fato** (havia sinalizacao? o radar era aferido?) — se a sentenca julgou prova, avisar que a via excepcional depois sera estreita (Sumula 7 STJ) e que a apelacao e a ultima instancia ampla. Nao prometer reforma.

## Cross-link (soft, nao duplicar)
`base-processual-judicial-transito` (CPC) · `recursos-excepcionais` (proxima instancia) · `contrarrazoes-e-agravos-excepcionais` (se o outro polo apelar) · `acao-reparatoria-transito`/`calculosjudiciais` (quantum).

## Guard
Toda sumula/tese so via `validador-transito`. Preparo ausente = risco de desercao — calcular e avisar. **Entrega final fecha pela `suprema-corte-transito` (R1-R4).**
