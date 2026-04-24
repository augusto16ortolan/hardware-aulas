---
description: >-
  Roteiro completo (2 horas) para ministrar o Conteúdo 4 — Arquitetura DSP em
  FPGAs, com agenda por tempo, analogias, exemplos MAC e checkpoints para
  iniciantes.
---

# Roteiro de Aula (2h) — Conteúdo 4: Arquitetura DSP em FPGAs

## Objetivo da aula (para você, professor)

Ao final da aula, os alunos devem conseguir:

- explicar o que é um PLD e diferenciar ASIC, CPLD e FPGA;
- explicar o que significa FPGA ser “programável em campo”;
- descrever a arquitetura básica de um FPGA (CLB/IOB/Switch Matrix/LUT/memória/DSP);
- explicar o que é DSP e por que MAC aparece tanto;
- justificar quando FPGA com DSP faz sentido (e quando não).

## Pré-aula (checklist de 5 minutos)

- Abra:
  - `hardware-aulas/conteudo-4/introducao-arquitetura-dsp-em-fpgas.md`
  - `hardware-aulas/conteudo-4/dispositivos-logicos-programaveis.md`
  - `hardware-aulas/conteudo-4/asic-pld-cpld-e-fpga.md`
  - `hardware-aulas/conteudo-4/o-que-e-fpga.md`
  - `hardware-aulas/conteudo-4/arquitetura-basica-de-um-fpga.md`
  - `hardware-aulas/conteudo-4/tecnologia-lut.md`
  - `hardware-aulas/conteudo-4/o-que-e-dsp.md`
  - `hardware-aulas/conteudo-4/blocos-dsp-em-fpgas.md`
  - `hardware-aulas/conteudo-4/paralelismo-em-fpga-para-dsp.md`
  - `hardware-aulas/conteudo-4/exemplo-conceitual-filtro-digital.md`
  - `hardware-aulas/conteudo-4/criterios-de-escolha.md`
  - `hardware-aulas/conteudo-4/atividades.md`
- Quadro pronto:
  - “CPU executa instruções” vs “FPGA vira circuito”
  - MAC: `resultado = resultado + (a*b)`

## Estrutura (2 horas)

### 0–10 min — Abertura: CPU vs FPGA (sem confusão)

- Mensagem-chave (diga explicitamente):
  - CPU: executa instruções
  - FPGA: é configurado para virar circuito
- Pergunta:
  - “Quando você gostaria de ‘virar circuito’ em vez de executar instruções?”

### 10–25 min — PLDs: por que existem?

Use `hardware-aulas/conteudo-4/dispositivos-logicos-programaveis.md`.

- Analogia:
  - ferramenta fixa vs ferramenta reconfigurável.
- Aplicações:
  - prototipagem, controle, integração.

### 25–40 min — ASIC vs CPLD vs FPGA (trade-offs)

Use `hardware-aulas/conteudo-4/asic-pld-cpld-e-fpga.md` e `hardware-aulas/conteudo-4/cpld-vs-fpga.md`.

- Faça a turma “escolher” em 3 cenários:
  1) produto em massa
  2) lógica de controle simples
  3) processamento de sinais com paralelismo

### 40–55 min — O que é FPGA?

Use `hardware-aulas/conteudo-4/o-que-e-fpga.md`.

- Mensagens-chave:
  - programável em campo;
  - hardware reconfigurável;
  - VHDL/Verilog descrevem circuitos (nível introdutório).

**Checkpoint:**
“FPGA ‘roda programa’ como CPU? Por quê?”

### 55–75 min — Arquitetura básica do FPGA (blocos)

Use `hardware-aulas/conteudo-4/arquitetura-basica-de-um-fpga.md` e `hardware-aulas/conteudo-4/tecnologia-lut.md`.

- Blocos:
  - CLB/IOB/Switch Matrix/LUT/flip-flop/memória/bloco DSP.
- LUT:
  - tabela verdade como memória pequena.

**Mini-atividade (3 min):**
Monte a tabela AND (2 entradas) e diga “isso cabe numa LUT”.

### 75–90 min — O que é DSP? (sem matemática pesada)

Use `hardware-aulas/conteudo-4/o-que-e-dsp.md`.

- Sinal: áudio, imagem, sensores.
- Operações: soma, multiplicação, média, filtragem.

### 90–105 min — Blocos DSP e MAC

Use `hardware-aulas/conteudo-4/blocos-dsp-em-fpgas.md`.

- Mensagem-chave:
  - multiplicação e acumulação repetem muito;
  - bloco DSP economiza LUTs e aumenta desempenho.
- Faça o MAC virar “mantra”:
  - `resultado = resultado + (a*b)`

### 105–115 min — Paralelismo (por que FPGA brilha)

Use `hardware-aulas/conteudo-4/paralelismo-em-fpga-para-dsp.md`.

- Mostre no quadro:
  - 4 multiplicações em paralelo + soma.

### 115–120 min — Critérios de escolha + fechamento

Use `hardware-aulas/conteudo-4/criterios-de-escolha.md` e `hardware-aulas/conteudo-4/resumo.md`.

- Faça 2 decisões rápidas em sala:
  - “LED com botão” → não precisa FPGA DSP
  - “vídeo em tempo real” → possivelmente sim

Deixe `hardware-aulas/conteudo-4/atividades.md` como tarefa (ou faça 2 questões ao vivo).

## Plano de quadro (sugestão)

- CPU vs FPGA (frase curta)
- ASIC / CPLD / FPGA (tabela rápida: flexível vs otimizado)
- FPGA: CLB + IOB + Switch + LUT + Mem + DSP
- DSP: sinais → “muito multiplica + soma”
- MAC: `res = res + (a*b)`
- “Quando usar?” (3 bullets: paralelismo, baixa latência, contas repetitivas)

