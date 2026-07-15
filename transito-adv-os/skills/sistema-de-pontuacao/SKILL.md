---
name: sistema-de-pontuacao
description: Calcula o teto de pontos VIGENTE (20/30/40 conforme nº de gravíssimas em 12 meses, Lei 14.071/2020) e a contagem no prontuário — NUNCA "20 pontos e perde a CNH". EAR (motorista profissional) = 40 fixo. Aplica o TRUNFO do art. 18 da Res. 918/2022 (pontos só vão ao RENACH após esgotados os recursos → recorrer SEGURA os pontos). Use quando o operador falar em "pontos na CNH", "quantos pontos", "vou ser suspenso por pontos", "atingi o limite", "EAR/motorista profissional", "contagem de 12 meses", ou cliente perto do limite de suspensão.
---

# SISTEMA-DE-PONTUACAO

> Camada 3 (CNH). O motor de contagem de pontos. Toda faixa vem do `context/` — zero número de cabeça. Verdade dura §1: desde 12/04/2021 NÃO é "20 pontos e perde"; é escalonado 20/30/40 conforme gravíssimas.

## Anexos obrigatórios (context/)
- `context/leis-14071-14599-15428.md` — **grep art. 261, §1º** (teto 20/30/40) e **art. 259** (7/5/4/3 pontos). A Lei 14.071/2020 vige desde **12/04/2021** — fatos anteriores seguem o regime antigo (20 pontos secos). Marco temporal decisivo.
- `context/ctb-9503-97.md` — art. 259 (pontuação por natureza) + art. 261 (portas da suspensão).
- `context/resolucao-918-2022.md` — **art. 18** (pontos só ao RENACH após esgotados os recursos) + art. 13 (efeito suspensivo).

## Quando ativa
- "Quantos pontos eu tenho / falta / posso ter?"; "vou perder a CNH por pontos?".
- Cliente **próximo do teto** querendo saber se ainda pode dirigir / o que fazer.
- Motorista com **EAR** (atividade remunerada) — regra própria de teto.
- Triagem que revela acúmulo de pontos → decidir entre recorrer (segurar pontos) ou reciclagem preventiva.

## Base legal ancorada
### Teto escalonado — art. 261, I CTB (Lei 14.071/2020) ✅
No período de **12 meses**, o limite de pontos que enseja suspensão **varia conforme o nº de infrações gravíssimas**:
- **20 pontos** → se houver **2 ou mais** gravíssimas;
- **30 pontos** → se houver **exatamente 1** gravíssima;
- **40 pontos** → se **nenhuma** gravíssima.

⚠️ Logo: dizer "juntou 20 pontos, perdeu a CNH" é **erro** (folclore do regime pré-2021). Sempre contar **quantas gravíssimas** o cliente tem antes de afirmar o teto.

### EAR — motorista profissional (art. 261, §1º) ✅
Condutor com **atividade remunerada (EAR na CNH)**: teto de **40 pontos**, independentemente do nº de gravíssimas. 🟡 Ao atingir **30 pontos**, há previsão de **curso preventivo de reciclagem** para não ser suspenso (art. 261 §§5º-7º — *a confirmar redação/condições no `validador-transito`*).

### Pontos por natureza — art. 259 CTB ✅
Gravíssima **7** · grave **5** · média **4** · leve **3**. (Multiplicador da gravíssima afeta o **valor da multa**, NÃO o nº de pontos — não confundir.)

### 🔑 TRUNFO — art. 18 da Res. 918/2022 ✅
Os pontos **só são lançados no RENACH/prontuário depois de ESGOTADOS os recursos** (defesa da autuação → JARI → 2ª instância). Enquanto o processo corre com efeito suspensivo (art. 13/18), **os pontos não entram** na contagem. ⇒ **Recorrer segura os pontos.** Para quem está a poucos pontos do teto, recorrer de cada autuação é a jogada que evita a suspensão — ouro comercial e jurídico.

## Passo a passo — o que produzir
1. **Reunir o prontuário/RENACH** (extrato do Detran): listar cada infração dos últimos **12 meses** com data, natureza, pontos e **status** (definitiva? em recurso? prescrita?).
2. **Excluir da contagem** o que ainda NÃO é definitivo (art. 18 Res.918) e o que está prescrito/anulado.
3. **Contar as gravíssimas definitivas** → definir o teto aplicável (20/30/40). EAR → 40 (checar reciclagem preventiva aos 30).
4. **Somar os pontos definitivos** e comparar com o teto → dizer, honestamente, se está ou não em zona de suspensão.
5. **Plano de contenção:** para cada autuação ainda viva, avaliar recurso (segura o ponto) — acionar `defesa-da-autuacao` / `recurso-jari` / `recurso-cetran`. Se já suspenso, `processo-suspensao-direito-dirigir`.
6. **Saída:** quadro de pontos (definitivos × pendentes), teto aplicável, distância do limite e recomendação (recorrer × reciclagem × aceitar).

## Postura honesta
- Nunca prometer que "recorrer apaga a multa" — o art. 18 **adia** o lançamento; se o recurso for negado e a infração virar definitiva, o ponto entra. O valor real é **ganhar tempo e chance de anulação**, não milagre.
- Reciclagem preventiva do EAR e faixa de suspensão são **🟡 a confirmar** — não afirmar prazo/condição sem validar.

## Cross-link (soft)
Cálculo de valor de multa → `enquadramento-e-multas-comuns` / `calculosjudiciais`. Já suspenso → `processo-suspensao-direito-dirigir`. Anular a base → `defesa-da-autuacao`.

## Guard
Faixa 20/30/40, EAR=40 e pontos 7/5/4/3 saem **do `context/` via grep**, nunca de memória; contagem cruzada pelo `validador-transito`. Fato anterior a 12/04/2021 = regime antigo (checar data). Peça derivada fecha por `suprema-corte-transito`.

sistema-de-pontuacao -> arts.: CTB 259 (7/5/4/3 ✅), 261 I + §1º (20/30/40 ✅; EAR 40 ✅; reciclagem §§5-7 🟡); Res. 918/2022 art. 18 (RENACH pós-recursos ✅) + art. 13 (efeito suspensivo ✅); Lei 14.071/2020 (vig. 12/04/2021 ✅).
