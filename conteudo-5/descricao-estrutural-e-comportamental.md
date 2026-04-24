---
description: >-
  Nesta página do Conteúdo 5, você vai entender descrição estrutural e
  comportamental de forma progressiva, com foco no essencial para iniciantes.
---

# Descrição estrutural e comportamental

Ao descrever hardware, você pode explicar:

- **como** o circuito é montado (estrutura), ou
- **o que** o circuito deve fazer (comportamento).

As duas abordagens são úteis.

## Descrição estrutural

Na descrição estrutural, você escreve como se estivesse “montando” o circuito:

- lista de componentes (portas, blocos),
- sinais internos (fios),
- conexões entre eles.

### Pontos fortes

- Ajuda a entender a composição lógica/“física”.
- Fica bem próximo de um diagrama com portas.

### Ponto fraco

- Pode ficar muito extensa em circuitos grandes.

## Descrição comportamental

Na descrição comportamental, você descreve a regra do comportamento:

- expressões lógicas,
- condições,
- tabelas de seleção,
- processos para reagir a sinais (especialmente clock).

### Pontos fortes

- Mais legível quando o circuito cresce.
- Facilita mudanças e manutenção.

### Ponto fraco

- Você pode perder a visão “porta por porta” (o que nem sempre é um problema).

## Analogia (bem simples)

- **Estrutural:** explicar cada peça de uma máquina e como elas se encaixam.
- **Comportamental:** explicar o que a máquina deve fazer (o resultado esperado).

## Tabela comparativa

| Critério | Estrutural | Comportamental |
|---|---|---|
| Foco | Como é montado | O que deve fazer |
| Proximidade de portas | Alta | Variável |
| Legibilidade em circuitos grandes | Pode piorar muito | Geralmente melhor |
| Facilidade de manutenção | Pode ser difícil | Geralmente melhor |
| Uso típico | Didática/visualização, módulos pequenos | Descrição de lógica, controle, FSMs |

Na próxima página, vamos ver algumas estruturas condicionais em VHDL que ajudam na descrição comportamental.

