---
name: cnh-bloqueio-renovacao-reabilitacao
description: Destrava a CNH bloqueada e organiza renovação/desbloqueio — distingue BLOQUEIO (estado processual do prontuário) de SUSPENSÃO (penalidade). Cobre PPD/permissão no 1º ano (art. 148 §2º), validade por idade (art. 147 §2º: 10/5/3 anos), a RENOVAÇÃO AUTOMÁTICA via RNPC (Lei 15.428/2026, art. 268-A §7º), curso de reciclagem + prova para desbloqueio pós-suspensão, e a Súmula 127 STJ (renovação não pode ser condicionada a multa não notificada). Use quando o cliente falar em "CNH bloqueada", "não consigo renovar", "2ª via travada", "permissão/PPD 1º ano", "reabilitar a carteira", "CNH vencida", ou "desbloquear".
---

# CNH-BLOQUEIO-RENOVACAO-REABILITACAO

> Camada 3 (CNH). Separa três coisas que o cliente confunde: **bloqueio** (não é penalidade), **renovação** (validade/idade + RNPC automático 2026) e **desbloqueio/reabilitação** (o caminho de volta). Lei VIGENTE inclui a 15.428/2026 (pós-cutoff).

## Anexos obrigatórios (context/)
- `context/ctb-9503-97.md` — **grep art. 148 §2º** (PPD 1º ano), **art. 147 §2º** (validade 10/5/3), art. 162 V (CNH vencida +30 dias).
- `context/leis-14071-14599-15428.md` — **Lei 15.428/2026**: art. 159 caput reescrito (CNH física OU digital, **fé pública**) + **art. 268-A §7º (renovação automática via RNPC)**. Pós-corte de treino — só existe porque foi capturada do Planalto; conferir antes de citar em peça.
- `context/jurisprudencia-transito.md` — **Súmula 127 STJ** (renovação/licença não condicionada a multa não notificada) ✅.

## Quando ativa
- "Minha CNH está **bloqueada**"; "não consigo **renovar/tirar 2ª via/mudar categoria**".
- **PPD** (permissão) no 1º ano com infração impeditiva.
- CNH **vencida** (renovação + validade por idade).
- Voltar a dirigir **após suspensão** (reciclagem + desbloqueio).
- Detran exige **pagar multa não notificada** para renovar/licenciar.

## Base legal ancorada
### Bloqueio ≠ suspensão 🟡
**Bloqueio** = restrição sistêmica no prontuário/RENACH (ex.: processo de suspensão instaurado) que **impede renovação, 2ª via, mudança de categoria**. É **estado processual**, não a penalidade. **Suspensão** = a penalidade do art. 261. Desbloqueio só depois de concluído o processo + cumprido o prazo + reciclagem — **não há atalho administrativo**; atalho real é **anular** o processo-base (→ `processo-suspensao-direito-dirigir`).

### PPD — permissão no 1º ano — art. 148 §2º/§3º ✅
No 1º ano (permissão), quem comete infração **grave/gravíssima** ou é **reincidente em média** **NÃO obtém a CNH definitiva** e **reinicia todo o processo de habilitação**. **Defesa:** anular a infração impeditiva (defesa → JARI → 2ª instância) — cai a infração, cai o impedimento e obtém a definitiva.

### Validade por idade — art. 147 §2º (Lei 14.071/2020) ✅
< 50 anos → **10 anos** · ≥ 50 e < 70 → **5 anos** · ≥ 70 → **3 anos** (perito pode reduzir por saúde). **CNH vencida há +30 dias = art. 162, V**: gravíssima + retenção do veículo até apresentar condutor habilitado.

### 🔴 Renovação automática — RNPC — Lei 15.428/2026, art. 268-A §7º ✅
Condutor cadastrado no **RNPC (Registro Nacional Positivo de Condutores)** tem a **habilitação renovada AUTOMATICAMENTE** ao fim da validade, **dispensado dos procedimentos do art. 147, EXCETO os exames de aptidão física e mental**. E o art. 159 (caput reescrito) dá **fé pública** à CNH física ou digital → reforça tese contra autuação por "falta de porte" (art. 232) quando havia **CNH-e**. Novidade de **jun/2026** — nenhum modelo de jan/2026 tem; citar da fonte.

### Súmula 127 STJ ✅
É ilegal **condicionar a renovação da CNH/licenciamento ao pagamento de multa da qual o condutor não foi notificado**. Ferramenta direta contra a exigência abusiva do Detran → cabe **MS** (`mandado-de-seguranca-transito`).

## Reabilitação / desbloqueio pós-suspensão ✅
Após a suspensão: cumprir **integralmente o prazo** + **curso de reciclagem** (aula + prova teórica) → o Detran **desbloqueia** e a **pontuação zera**. O prazo de suspensão **só começa a correr com a entrega da CNH**. (Reabilitação **após CASSAÇÃO** é outra coisa — 2 anos + todos os exames, art. 263 §2º → `cassacao-da-cnh`.)

## Passo a passo — o que produzir
1. **Diagnosticar a trava**: bloqueio (processo?), vencimento (idade?), PPD (infração impeditiva?), exigência de multa não notificada?
2. **Rota administrativa**: renovação normal / RNPC automático (se cadastrado) / desbloqueio via reciclagem.
3. **Rota de defesa**: exigência ilegal de multa não notificada → **MS + Súmula 127**; infração impeditiva de PPD → anular a base.
4. **Saída**: parecer com a causa da trava + o caminho (administrativo × judicial) + peça cabível.

## Postura honesta
- Bloqueio por processo de suspensão **legítimo** não se "destrava" por petição — só concluindo o rito ou **anulando** o processo-base. Dizer isso claramente.
- RNPC/renovação automática é **novo (2026)** e depende de cadastro/regulamentação — confirmar disponibilidade no órgão antes de prometer.

## Cross-link (soft)
Processo-base → `processo-suspensao-direito-dirigir` / `cassacao-da-cnh`. Exigência de multa p/ renovar → `mandado-de-seguranca-transito` (Súmula 127). Toxicológico na renovação C/D/E → `exame-toxicologico`. Autuação por porte (232) com CNH-e → `enquadramento-e-multas-comuns`.

## Guard
Validade 10/5/3, PPD (148 §2º) e **RNPC (Lei 15.428/2026, 268-A §7º)** saem **do `context/` via grep** — a Lei 15.428 é pós-cutoff, jamais citar de memória. Bloqueio×suspensão = 🟡 (conceito operacional, confirmar no `validador-transito`). Peça fecha por `suprema-corte-transito`.

cnh-bloqueio-renovacao-reabilitacao -> arts.: CTB 148 §2º/§3º (PPD ✅), 147 §2º (validade 10/5/3 ✅), 162 V (vencida +30d ✅), 232 (porte ✅); Lei 15.428/2026 art. 159 caput (fé pública ✅) + 268-A §7º (RNPC automático ✅); Súmula 127 STJ (✅).
