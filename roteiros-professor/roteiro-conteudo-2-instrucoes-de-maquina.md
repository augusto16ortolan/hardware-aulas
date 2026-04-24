---
description: >-
  Roteiro completo (2 horas) para ministrar o Conteúdo 2 — Instruções de máquina,
  com agenda por tempo, exemplos, checkpoints e perguntas guiadas.
---

# Roteiro de Aula (2h) — Conteúdo 2: Instruções de máquina

## Objetivo da aula (para você, professor)

Ao final da aula, os alunos devem conseguir:

- explicar a diferença entre **alto nível**, **assembly** e **código de máquina**;
- identificar **opcode** e **operandos** em exemplos simples;
- reconhecer tipos de instruções (dados, aritmética, controle de fluxo);
- explicar modos de endereçamento em nível introdutório;
- descrever o **ciclo de instrução** (buscar → decodificar → executar → armazenar);
- entender que arquiteturas diferentes (x86 vs ARM) têm ISAs diferentes.

## Pré-aula (checklist de 5 minutos)

- Abra:
  - `hardware-aulas/conteudo-2/introducao-as-instrucoes-de-maquina.md`
  - `hardware-aulas/conteudo-2/do-codigo-ao-processador.md`
  - `hardware-aulas/conteudo-2/o-que-sao-instrucoes-de-maquina.md`
  - `hardware-aulas/conteudo-2/opcode-e-operandos.md`
  - `hardware-aulas/conteudo-2/modos-de-enderecamento.md`
  - `hardware-aulas/conteudo-2/ciclo-de-instrucao.md`
  - `hardware-aulas/conteudo-2/resumo.md`
  - `hardware-aulas/conteudo-2/atividades.md`
- Prepare um pseudo-exemplo de 4 instruções (no quadro):
  - `LOAD R1, [X]`
  - `ADD R1, R2`
  - `STORE [Y], R1`
  - `JMP L1`

## Estrutura (2 horas)

### 0–10 min — Revisão rápida + conexão com Conteúdo 1

- Relembre:
  - “CPU executa instruções” e “ISA = vocabulário da arquitetura”.
- Gancho:
  - “Hoje vamos ver como esse vocabulário aparece na prática.”

### 10–30 min — Do alto nível até a CPU

Use `hardware-aulas/conteudo-2/do-codigo-ao-processador.md`.

- Mensagens-chave:
  - alto nível → compilador/VM → assembly → assembler → código de máquina;
  - CPU executa o código de máquina, não `if/for/classes`.

**Checkpoint (pergunta):**
“Onde entra o assembly nesse caminho?”

### 30–50 min — O que é uma instrução de máquina

Use `hardware-aulas/conteudo-2/o-que-sao-instrucoes-de-maquina.md`.

- Mensagens-chave:
  - instruções são representadas em bits;
  - CPU lê da memória e executa.

**Exemplo didático:**
Descreva uma instrução como “verbo + complementos”:
- verbo = opcode
- complementos = operandos

### 50–65 min — Opcode e operandos

Use `hardware-aulas/conteudo-2/opcode-e-operandos.md`.

- Faça a turma “apontar” no pseudo-exemplo:
  - opcode = `LOAD/ADD/STORE/JMP`
  - operandos = registradores, endereços, imediatos.

**Mini-atividade (2–3 min):**
Escreva 3 instruções no quadro e peça para 2 alunos identificarem opcode/operandos.

### 65–80 min — Tipos de instruções (categorias)

Use `hardware-aulas/conteudo-2/tipos-de-instrucoes.md`.

- Categorias úteis para iniciantes:
  - movimentação de dados
  - aritmética e lógica
  - controle de fluxo
  - comparação

**Checkpoint:**
“Qual categoria ‘faz’ um `if` existir no nível de máquina?”

### 80–95 min — Modos de endereçamento

Use `hardware-aulas/conteudo-2/modos-de-enderecamento.md`.

- Mensagens-chave:
  - “onde está o dado?” (registrador, memória, imediato).
- Evite aprofundar em muitos modos: foque em 3–4 intuitivos.

**Pergunta para discussão:**
“Por que ‘imediato’ pode ser útil?”

### 95–105 min — Formato de instrução (visão simples)

Use `hardware-aulas/conteudo-2/formato-de-instrucao.md`.

- Mensagem-chave:
  - instrução tem campos (opcode, operandos, etc.).
- Evite entrar em tamanhos específicos e bits reais.

### 105–112 min — Ciclo de instrução

Use `hardware-aulas/conteudo-2/ciclo-de-instrucao.md`.

- Faça o ciclo “virar rotina” na cabeça deles:
  - buscar → decodificar → executar → armazenar.

### 112–118 min — Instruções em arquiteturas diferentes

Use `hardware-aulas/conteudo-2/instrucoes-em-arquiteturas-diferentes.md`.

- Mensagem-chave:
  - x86 e ARM possuem “vocabulários” diferentes;
  - binários não são automaticamente compatíveis.

### 118–120 min — Fechamento e tarefa

Use `hardware-aulas/conteudo-2/resumo.md`.

- Deixe 3 questões de `hardware-aulas/conteudo-2/atividades.md` para casa.

## Plano de quadro (sugestão)

- Caminho: alto nível → assembly → máquina → CPU
- Instrução = opcode + operandos
- Modos de endereçamento (3 exemplos)
- Ciclo: buscar → decodificar → executar → armazenar
- ISA depende da arquitetura (x86 vs ARM)

## Erros comuns (para prevenir)

- Confundir RAM com armazenamento.
- Achar que FPGA/CPU “funcionam do mesmo jeito” (você pode lembrar que FPGA é outro assunto).
- Achar que assembly é “linguagem universal”: não é (depende da ISA).

