---
description: >-
  Roteiro completo (2 horas) para ministrar o Conteúdo 1 — Processadores RISC e
  CISC, com agenda por tempo, perguntas, checkpoints e sugestões didáticas.
---

# Roteiro de Aula (2h) — Conteúdo 1: Processadores RISC e CISC

## Objetivo da aula (para você, professor)

Ao final da aula, os alunos devem conseguir:

- explicar o que é uma CPU e o que são instruções (em linguagem simples);
- descrever a ideia geral de **RISC** e **CISC**;
- comparar RISC e CISC em termos de filosofia e trade-offs (sem “melhor absoluto”);
- relacionar x86/x86-64 e ARM com usos reais (PC, celular, Raspberry Pi).

## Pré-aula (checklist de 5 minutos)

- Abra no GitBook:
  - `hardware-aulas/conteudo-1/introducao-aos-processadores-risc-e-cisc.md`
  - `hardware-aulas/conteudo-1/arquitetura-cisc.md`
  - `hardware-aulas/conteudo-1/arquitetura-risc.md`
  - `hardware-aulas/conteudo-1/comparacao-risc-cisc.md`
  - `hardware-aulas/conteudo-1/resumo.md`
  - `hardware-aulas/conteudo-1/atividades.md`
- Separe 1 exemplo cotidiano para “ancorar”:
  - notebook (PC), smartphone e (se possível) Raspberry Pi.
- Prepare o quadro (ou um slide simples):
  - “CPU = executa instruções” + “ISA = vocabulário” + “trade-off = depende do objetivo”.

## Estrutura (2 horas)

### 0–10 min — Abertura e contexto

- Pergunta de aquecimento:
  - “Por que um celular aguenta o dia todo de bateria e um PC gamer não?”
  - “Por que a maioria dos PCs é Intel/AMD e a maioria dos celulares é ARM?”
- Enquadre a ideia central:
  - “Hoje vamos entender **duas filosofias de CPU** e como elas aparecem no mundo real.”

**Checkpoint (pergunta rápida):**
“O que uma CPU faz, em uma frase?”

### 10–25 min — O que é uma CPU e o que é uma instrução

Use `hardware-aulas/conteudo-1/o-que-e-um-processador.md`.

- Explique “CPU executa instruções”:
  - instrução = “comando básico” (mover, somar, comparar, desviar).
- Diferencie com exemplos:
  - “somar dois números”, “ler memória”, “pular para outro trecho”.

**Mini-atividade (2 min, oral):**
Peça 3 exemplos de “ações mínimas” que um computador precisa fazer para rodar um programa.

### 25–45 min — CISC (visão didática)

Use `hardware-aulas/conteudo-1/arquitetura-cisc.md`.

- Mensagens-chave:
  - histórico/legado e compatibilidade;
  - instruções mais “ricas” (conceitualmente);
  - trade-off: complexidade do hardware vs simplicidade de algumas instruções.
- Amarre no mundo real:
  - x86/x86-64 em PCs e servidores.

**Perguntas para a turma:**
- “Qual é a vantagem de manter compatibilidade com muito software antigo?”
- “Em que tipo de mercado isso vale muito?”

### 45–65 min — RISC (visão didática)

Use `hardware-aulas/conteudo-1/arquitetura-risc.md`.

- Mensagens-chave:
  - foco em eficiência e instruções mais simples (conceitualmente);
  - facilidade de pipeline/execução eficiente (sem aprofundar);
  - trade-off: mais trabalho no compilador/organização do software.
- Amarre no mundo real:
  - ARM em móveis/embarcados e Raspberry Pi.

**Perguntas para a turma:**
- “Por que eficiência energética é tão importante em móveis/embarcados?”
- “Que tipos de aplicações se beneficiam disso?”

### 65–85 min — Comparação RISC vs CISC (sem absolutismos)

Use `hardware-aulas/conteudo-1/comparacao-risc-cisc.md`.

- Faça a turma construir a comparação:
  - peça para eles sugerirem 2 pontos “RISC tende a…” e 2 pontos “CISC tende a…”.
- Conclusão:
  - “depende do objetivo (energia, custo, compatibilidade, desempenho, ecossistema)”.

**Armadilhas para evitar (diga explicitamente):**
- “x86 não é ‘CISC puro’ na prática moderna” (sem entrar em microarquitetura).
- “ARM não é um ‘padrão único’: existem variações e gerações”.

### 85–100 min — Ponte para o Conteúdo 2

- Conecte com o próximo tema:
  - “RISC e CISC influenciam o ‘vocabulário’ de instruções (ISA).”
  - “No próximo conteúdo, vamos ver como esse vocabulário aparece como instruções de máquina.”

### 100–110 min — Resumo guiado

Use `hardware-aulas/conteudo-1/resumo.md`.

- Faça um “resumo em 3 frases” com a turma:
  1) CPU executa instruções.
  2) RISC e CISC são filosofias de projeto com trade-offs.
  3) A escolha aparece no mundo real (ARM vs x86) e depende do objetivo.

### 110–120 min — Atividades (fechamento)

Use `hardware-aulas/conteudo-1/atividades.md`.

- Se der tempo: faça 2–3 questões em sala (oral) e deixe o restante como tarefa.
- Dê o “critério de resposta”:
  - “responda com ideia e exemplo real, não só definição”.

## Plano de quadro (sugestão)

- CPU → executa instruções
- ISA → “vocabulário”
- RISC → eficiência/ideia de simplicidade
- CISC → compatibilidade/ideia de instruções ricas
- Mundo real → ARM (móveis/embarcados) vs x86 (PC/servidor)
- Frase final → “não existe melhor absoluto”

## Dúvidas comuns (como responder)

- “Então ARM é sempre melhor?”
  - Não. Depende: objetivo, software, custo, desempenho, energia.
- “RISC é sempre mais rápido?”
  - Não. Existem muitas técnicas de otimização. A aula é visão introdutória.

