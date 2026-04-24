---
description: >-
  Roteiro completo (2 horas) para ministrar o Conteúdo 5 — HDL/VHDL (base), com
  sequência didática, checkpoints e foco em iniciantes.
---

# Roteiro de Aula (2h) — Conteúdo 5: HDL e base de VHDL

## Objetivo da aula (para você, professor)

Ao final da aula, os alunos devem conseguir:

- explicar o que é uma HDL e por que ela difere de uma linguagem de programação comum;
- reconhecer onde HDLs são usadas (FPGA/CPLD/ASIC/simulação);
- entender `entity` e `architecture` em VHDL (nível inicial);
- diferenciar combinacional vs sequencial (noção);
- entender por que clock/flip-flop importam (conceitual).

## Pré-aula (checklist de 5 minutos)

- Abra:
  - `hardware-aulas/conteudo-5/introducao-a-linguagem-de-descricao-de-hardware.md`
  - `hardware-aulas/conteudo-5/o-que-e-hdl.md`
  - `hardware-aulas/conteudo-5/vhdl-estrutura-basica.md`
  - `hardware-aulas/conteudo-5/circuitos-combinacionais.md`
  - `hardware-aulas/conteudo-5/circuitos-sequenciais.md`
  - `hardware-aulas/conteudo-5/flip-flop-e-clock.md`
  - `hardware-aulas/conteudo-5/maquinas-de-estados-finitos.md`
  - `hardware-aulas/conteudo-5/vamos-para-a-pratica.md`
  - `hardware-aulas/conteudo-5/atividades.md`
- Prepare o quadro com 2 frases:
  - “Software → sequência de passos”
  - “HDL → descrição de circuito”

## Estrutura (2 horas)

### 0–10 min — Abertura: “não é programação comum”

- Pergunte:
  - “Se eu escrevo VHDL, eu estou criando um programa ou um circuito?”
- Mensagem-chave:
  - HDL descreve hardware.

### 10–25 min — O que é HDL e onde aparece

Use `hardware-aulas/conteudo-5/o-que-e-hdl.md` e `hardware-aulas/conteudo-5/aplicacoes-de-hdl.md`.

- Foco em:
  - simular, testar, sintetizar;
  - FPGA/CPLD.

### 25–45 min — Estrutura básica do VHDL (visão inicial)

Use `hardware-aulas/conteudo-5/vhdl-estrutura-basica.md`.

- Conceitos:
  - `entity` = interface (entradas/saídas)
  - `architecture` = implementação
  - `signal` = fio/conexão

**Checkpoint:**
“O que fica na entity e o que fica na architecture?”

### 45–60 min — Combinacional

Use `hardware-aulas/conteudo-5/circuitos-combinacionais.md`.

- Ideia:
  - saída depende só das entradas atuais.
- Exemplos conceituais:
  - AND, OR, multiplexador.

### 60–75 min — Sequencial (memória/estado)

Use `hardware-aulas/conteudo-5/circuitos-sequenciais.md` e `hardware-aulas/conteudo-5/flip-flop-e-clock.md`.

- Ideia:
  - saída depende de entradas + estado anterior.
- Explique clock:
  - “batida” que sincroniza mudanças.

### 75–90 min — FSM (máquina de estados) em nível conceitual

Use `hardware-aulas/conteudo-5/maquinas-de-estados-finitos.md`.

- Mostre um exemplo cotidiano:
  - semáforo (estados e transições).

### 90–105 min — “Vamos para a prática?” (guiado)

Use `hardware-aulas/conteudo-5/vamos-para-a-pratica.md`.

- Se for sala prática:
  - foque em um AND simples + testbench conceitual.
- Se for sala teórica:
  - faça como exercício mental: entradas → saída.

### 105–120 min — Resumo + atividades

- Use `hardware-aulas/conteudo-5/resumo.md` e 3–5 questões do `hardware-aulas/conteudo-5/atividades.md`.

## Plano de quadro (sugestão)

- HDL ≠ software
- VHDL: entity (I/O) + architecture (lógica)
- Combinacional vs sequencial
- Clock + flip-flop
- FSM = estados + transições

