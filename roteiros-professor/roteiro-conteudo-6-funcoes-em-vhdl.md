---
description: >-
  Roteiro completo (2 horas) para ministrar o Conteúdo 6 — Funções em VHDL, com
  sequência por tempo, exemplos práticos e checkpoints para iniciantes.
---

# Roteiro de Aula (2h) — Conteúdo 6: Funções em VHDL

## Objetivo da aula (para você, professor)

Ao final da aula, os alunos devem conseguir:

- explicar o que é uma função em VHDL e por que ela ajuda a organizar o projeto;
- reconhecer parâmetros, retorno e variáveis locais;
- entender onde declarar funções (na architecture e em packages, conceitualmente);
- relacionar funções com reuso (ex.: conversões e cálculos repetidos).

## Pré-aula (checklist de 5 minutos)

- Abra:
  - `hardware-aulas/conteudo-6/introducao-a-funcoes-em-vhdl.md`
  - `hardware-aulas/conteudo-6/o-que-sao-funcoes-em-vhdl.md`
  - `hardware-aulas/conteudo-6/sintaxe-basica-de-funcoes.md`
  - `hardware-aulas/conteudo-6/parametros-retorno-e-variaveis.md`
  - `hardware-aulas/conteudo-6/funcoes-em-packages.md`
  - `hardware-aulas/conteudo-6/funcoes-e-sintese.md`
  - `hardware-aulas/conteudo-6/exemplo-pratico-display-7-segmentos.md`
  - `hardware-aulas/conteudo-6/exemplo-pratico-cronometro-simples.md`
  - `hardware-aulas/conteudo-6/atividades.md`
- Prepare um exemplo conceitual no quadro:
  - “entradas → função → saída” (conversão ou comparação).

## Estrutura (2 horas)

### 0–10 min — Abertura: por que funções existem em VHDL?

- Pergunta:
  - “Qual problema acontece quando copiamos e colamos lógica várias vezes?”
- Mensagem-chave:
  - função = reuso + legibilidade + manutenção.

### 10–25 min — O que é uma função (conceito)

Use `hardware-aulas/conteudo-6/o-que-sao-funcoes-em-vhdl.md`.

- Características:
  - recebe 0+ parâmetros;
  - retorna 1 valor;
  - tem lógica interna (sequencial).

**Checkpoint:**
“Uma função retorna quantos valores?”

### 25–45 min — Sintaxe e parâmetros/retorno

Use:
- `hardware-aulas/conteudo-6/sintaxe-basica-de-funcoes.md`
- `hardware-aulas/conteudo-6/parametros-retorno-e-variaveis.md`

- Foco didático:
  - tipos e retorno;
  - variáveis locais;
  - exemplo simples (soma/comparação).

### 45–60 min — Funções com condicionais e vetores

Use:
- `hardware-aulas/conteudo-6/funcoes-com-condicionais.md`
- `hardware-aulas/conteudo-6/funcoes-com-vetores.md`

Mensagem-chave:
- funções ajudam muito em lógica repetitiva (comparar vetores, conversões).

### 60–75 min — Funções em packages (reuso)

Use `hardware-aulas/conteudo-6/funcoes-em-packages.md`.

- Explique como ideia:
  - “biblioteca” de funções do projeto.

### 75–90 min — Funções e síntese (o que vira hardware)

Use `hardware-aulas/conteudo-6/funcoes-e-sintese.md`.

- Mensagem-chave:
  - função não “roda” como software; ela descreve lógica que será implementada.
- Evite aprofundar em temporização/pipeline.

### 90–110 min — Exemplos práticos guiados

Use:
- `hardware-aulas/conteudo-6/exemplo-pratico-display-7-segmentos.md`
- `hardware-aulas/conteudo-6/exemplo-pratico-cronometro-simples.md`

Sugestão de condução:
- peça para a turma identificar:
  - entrada(s)
  - saída
  - “qual parte vira função?”

### 110–120 min — Resumo + atividades

- Use `hardware-aulas/conteudo-6/resumo.md`.
- Resolva 2–3 questões do `hardware-aulas/conteudo-6/atividades.md` em sala e deixe o restante como tarefa.

## Plano de quadro (sugestão)

- Função: entradas → cálculo → 1 saída
- Benefícios: reuso, clareza, manutenção
- Onde: architecture / package
- Cuidado: VHDL descreve hardware (não “executa programa”)

