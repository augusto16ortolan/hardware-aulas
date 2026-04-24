---
description: >-
  Roteiro completo (2 horas) para ministrar o Conteúdo 3 — PC vs Raspberry Pi,
  com agenda por tempo, comparações-chave, estudos de caso e perguntas para a
  turma.
---

# Roteiro de Aula (2h) — Conteúdo 3: PC vs Raspberry Pi

## Objetivo da aula (para você, professor)

Ao final da aula, os alunos devem conseguir:

- explicar por que PC e Raspberry Pi são computadores com propostas diferentes;
- comparar CPU/arquitetura, RAM/armazenamento, expansão/conectividade, GPU e energia;
- escolher a plataforma adequada para cenários típicos (com justificativa).

## Pré-aula (checklist de 5 minutos)

- Abra:
  - `hardware-aulas/conteudo-3/introducao-comparacao-entre-hardware-de-pc-e-raspberry-pi.md`
  - `hardware-aulas/conteudo-3/visao-geral-pc-e-raspberry-pi.md`
  - `hardware-aulas/conteudo-3/arquitetura-do-processador.md`
  - `hardware-aulas/conteudo-3/memoria-e-armazenamento.md`
  - `hardware-aulas/conteudo-3/conectividade-e-expansao.md`
  - `hardware-aulas/conteudo-3/aplicacoes-praticas.md`
  - `hardware-aulas/conteudo-3/pc-ou-raspberry-pi-como-escolher.md`
  - `hardware-aulas/conteudo-3/estudo-de-caso.md`
  - `hardware-aulas/conteudo-3/atividades.md`
- Se possível, leve:
  - um Raspberry Pi (ou foto) e um notebook/desktop (ou foto).

## Estrutura (2 horas)

### 0–10 min — Abertura e enquadramento

- Perguntas rápidas:
  - “Raspberry Pi é ‘um PC pequeno’?”
  - “Se ambos rodam Linux, então são iguais?”
- Mensagem-chave:
  - “Ambos são computadores, mas com objetivos diferentes.”

### 10–25 min — Visão geral (tabela inicial)

Use `hardware-aulas/conteudo-3/visao-geral-pc-e-raspberry-pi.md`.

- Passe pelos itens da tabela e peça exemplos reais:
  - custo, energia, tamanho, expansão, prototipagem.

**Checkpoint:**
“Diga 2 motivos para usar Raspberry Pi e 2 para usar PC.”

### 25–45 min — Arquitetura do processador (x86/x86-64 vs ARM)

Use `hardware-aulas/conteudo-3/arquitetura-do-processador.md`.

- Mensagens-chave:
  - PC tende a x86/x86-64 (compatibilidade/ecossistema).
  - Pi tende a ARM (eficiência).
  - Conexão com Conteúdo 1: RISC/CISC como ideias (sem absolutismo).
  - Conexão com Conteúdo 2: ISA diferente afeta software.

**Pergunta:**
“O que pode acontecer se eu tentar rodar um programa compilado para x86 em um ARM?”

### 45–60 min — Memória e armazenamento (RAM vs disco/microSD)

Use `hardware-aulas/conteudo-3/memoria-e-armazenamento.md`.

- Mensagens-chave:
  - RAM ≠ armazenamento;
  - PC: upgrades e SSD/HD;
  - Pi: microSD e expansão via USB (dependendo do projeto).

**Exemplo que cola bem:**
- PC: IDE + navegador + banco local
- Pi: servidor simples/automação

### 60–75 min — Conectividade e expansão (PCIe vs GPIO)

Use `hardware-aulas/conteudo-3/conectividade-e-expansao.md`.

- Mensagens-chave:
  - PC expande com placas/portas;
  - Pi brilha com GPIO (sensores/atuadores).

**Mini-atividade (2–3 min):**
Peça para a turma citar 3 componentes “do mundo físico” que poderiam ser ligados ao GPIO.

### 75–85 min — Gráficos e energia (quando importa)

Use:
- `hardware-aulas/conteudo-3/desempenho-grafico.md`
- `hardware-aulas/conteudo-3/consumo-de-energia-e-aquecimento.md`

Mensagens-chave:
- PC com GPU dedicada → jogos/edição;
- Pi → gráficos modestos, baixo consumo, bom 24/7.

### 85–105 min — Aplicações práticas (decisão por cenário)

Use `hardware-aulas/conteudo-3/aplicacoes-praticas.md` e `hardware-aulas/conteudo-3/pc-ou-raspberry-pi-como-escolher.md`.

- Faça a turma justificar 5 cenários (em duplas, 5 min):
  - 2 cenários “PC”
  - 2 cenários “Pi”
  - 1 cenário “depende”

### 105–115 min — Estudos de caso (discussão guiada)

Use `hardware-aulas/conteudo-3/estudo-de-caso.md`.

- Escolha 2 casos para discutir (sem ler tudo):
  - laboratório educacional
  - automação com sensor/relé

### 115–120 min — Fechamento e atividade

- Use `hardware-aulas/conteudo-3/resumo.md`.
- Deixe 5 itens do `hardware-aulas/conteudo-3/atividades.md` como tarefa.

## Plano de quadro (sugestão)

- “Objetivo do projeto” no topo
- PC: desempenho/expansão/compatibilidade
- Pi: custo/energia/GPIO/prototipagem
- 3 perguntas de decisão:
  1) preciso de GPU?
  2) preciso de GPIO/sensores?
  3) preciso ficar 24/7 e gastar pouco?

