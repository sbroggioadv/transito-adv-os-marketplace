---
description: Inicia o wizard de configuracao do plugin transito — cria a pasta transito/ com identidade do escritorio, orgaos-alvo (DETRAN/DER/DNIT/PRF), UF, perfil (condutor/frota) e modo de fluxo.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
argument-hint: [--update para reconfigurar]
---

Voce foi acionado pelo comando `/start-transito` do plugin transito-adv-os (Direito do Transito — defesa do condutor).

Argumento recebido: `$ARGUMENTS`

**Objetivo:** configurar o plugin ao perfil do escritorio.

## PROTOCOLO
1. **Acionar a skill `transito-onboarding`** (wizard com botoes via AskUserQuestion nas escolhas de lista fechada).
2. Cria `<cwd>/transito/perfil.md` (identidade, orgaos-alvo, UF, perfil condutor/frota, modo).
3. Se ja existir, oferecer continuar / atualizar / recriar.

**Skill a acionar:** `transito-onboarding`.
