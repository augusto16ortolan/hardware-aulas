---
description: >-
  Nesta página do Conteúdo 5, você vai entender máquinas de estados finitos (fsm)
  de forma progressiva, com foco no essencial para iniciantes.
---

# Máquinas de estados finitos (FSM)

## O que é uma FSM?

**FSM** vem de **Finite State Machine** (Máquina de Estados Finitos).

É um modelo muito usado em hardware para descrever controle, porque vários sistemas podem ser vistos como:

- um conjunto de **estados**,
- com **transições** entre estados,
- dependendo de entradas/condições,
- gerando saídas.

## Por que FSMs são importantes em hardware?

Porque muitos circuitos de controle funcionam assim:

- semáforo,
- controle de elevador,
- máquina de venda,
- controladores de comunicação,
- controle interno de um processador (por exemplo, a “sequência” do ciclo de instrução).

## Conceitos essenciais

- **Estado atual:** em que “modo” o sistema está agora.
- **Próximo estado:** para onde ele vai no próximo passo (geralmente no próximo clock).
- **Entradas/condições:** sinais que influenciam a transição.
- **Saídas:** o que o sistema produz em cada estado (ou transição).
- **Transição:** mudança de um estado para outro.

## Exemplo conceitual: semáforo

Vamos imaginar um semáforo simples com estados:

- **Verde**
- **Amarelo**
- **Vermelho**

Condição de transição (conceitual):

- “passou o tempo do estado atual”.

### Tabela de transição (conceitual)

| Estado atual | Entrada/condição | Próximo estado | Saída |
|---|---|---|---|
| Verde | tempo_acabou = 1 | Amarelo | verde=1, amarelo=0, vermelho=0 |
| Amarelo | tempo_acabou = 1 | Vermelho | verde=0, amarelo=1, vermelho=0 |
| Vermelho | tempo_acabou = 1 | Verde | verde=0, amarelo=0, vermelho=1 |

## Como isso aparece em VHDL (visão bem geral)

Uma FSM em VHDL normalmente pode ser dividida em:

1. **processo sequencial** (com clock): atualiza o estado atual.
2. **processo combinacional**: decide o próximo estado e as saídas com base no estado atual e entradas.

> Não vamos escrever uma FSM grande aqui. O objetivo é entender o conceito.

Na próxima página, vamos ver ferramentas e o fluxo básico de simulação e síntese.

