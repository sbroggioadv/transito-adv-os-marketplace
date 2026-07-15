---
name: memoria-de-caso-transito
description: "Mantem o estado append-only de um caso de transito — condutor/proprietario, veiculo (placa), AIT (nº, orgao autuador, enquadramento), FASE (recebeu NA ou NP? datas de cada uma), pontos no prontuario, adesao ao SNE, processos de suspensao/cassacao em curso, prazos e proximo passo. Use quando o operador retomar um caso, perguntar onde paramos, pedir o status, a cronologia ou os prazos, ou quando o transito-master precisar carregar/atualizar o estado. Tambem ao iniciar caso novo."
---

# MEMORIA-DE-CASO-TRANSITO

> Camada 0. Registro append-only do caso. O `transito-master` le no inicio e atualiza no fim de cada ato.

## Anexos obrigatorios (context/)
- `context/metodologia-transito.md` — fluxo da porta unica e fases — **grep + ler a faixa**.

## Objetivo
Nunca perder o fio do caso: quem e o condutor/proprietario, o veiculo, o AIT e seus dados, **em que FASE esta** (NA x NP) e as datas de cada notificacao, os pontos, se aderiu ao SNE, os processos em curso, os prazos que vencem e o proximo passo.

## Quando ativar
Retomar caso, "onde paramos", "status", "cronologia", "quais prazos"; ou quando o `transito-master` precisa carregar/atualizar o estado; ou ao iniciar caso novo.

## Onde grava
`transito/casos/<slug-do-caso>.md` no diretorio de trabalho. **Append-only:** cada ato vira nova linha; nunca apaga o anterior.

## Estrutura do arquivo de caso
```markdown
# Caso: <titulo>
## Partes e veiculo
- Condutor: <nome> | Proprietario: <nome/PJ> | e o mesmo? <sim/nao>
- Veiculo: <placa / marca / especie> | categoria da CNH: <A-E> | EAR? <sim/nao>
## AIT (auto de infracao)
- Nº do AIT: <...> | orgao autuador: <DETRAN/PRF/DNIT/municipio> | via: <estadual/federal>
- Enquadramento: <artigo/codigo> | natureza: <leve/media/grave/gravissima> | data/hora/local: <...>
- Equipamento (radar/etilometro): <sim/nao> | aferido INMETRO? <a confirmar>
## FASE e notificacoes (o campo mais critico)
- Recebeu NA? <sim/nao> | data de expedicao da NA: <...> | dentro dos 30 dias da infracao? <sim/nao>
- Recebeu NP? <sim/nao> | data da NP: <...> | vencimento/prazo do recurso: <...>
- Aderiu ao SNE? <sim/nao> (se sim, ciencia presumida 30 dias apos inclusao)
- Fase atual: <defesa da autuacao / recurso JARI / recurso CETRAN / judicial>
## CNH / pontuacao
- Pontos no prontuario (12 meses): <...> | nº de gravissimas: <...> | teto aplicavel: <20/30/40>
- Processo de suspensao/cassacao em curso? <sim/nao> | fase: <...>
## Prazos
- <data fatal> | <ato> | <fonte: NA/NP/intimacao/publicacao> | <dias corridos [adm] / uteis [judicial]>
## Historico (append-only)
- <data> | <ato praticado> | <skill> | <resultado>
## Proximo passo
- <acao> ate <data>
```

## Metodologia
1. Ao iniciar: criar o arquivo com partes/veiculo + AIT + FASE/notificacoes + pontuacao.
2. A cada ato: **acrescentar** linha no Historico + atualizar Fase/Prazos/Proximo passo.
3. Nunca sobrescrever historico (auditabilidade).

## Entrega obrigatoria final
- Arquivo de caso criado/atualizado + resumo do estado (fase, proximo prazo, pontos, pendencias).

## Guard
Estado e fato, nao opiniao. Registrar numeros/datas exatamente como constam na fonte (AIT/NA/NP/prontuario). **A FASE (NA x NP) e as datas de expedicao/vencimento sao fatos-chave** — sustentam ou afastam a nulidade (Sumula 312; 30 dias da NA) e definem qual peca cabe. Prazo administrativo em **dias corridos**; nao estimar data sem o marco (expedicao da NA / vencimento da NP / inclusao no SNE).
