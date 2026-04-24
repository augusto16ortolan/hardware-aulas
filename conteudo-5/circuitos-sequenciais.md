---
description: >-
  Nesta página do Conteúdo 5, você vai entender circuitos sequenciais de forma
  progressiva, com foco no essencial para iniciantes.
---

# Circuitos sequenciais

Até agora falamos de combinacional: saída depende apenas das entradas atuais.

Agora vem uma ideia fundamental para hardware digital:

> circuitos sequenciais têm **memória** (estado).

## O que são circuitos sequenciais?

Um **circuito sequencial** é aquele em que:

- a saída pode depender das entradas atuais **e**
- do que aconteceu antes (estado anterior).

Isso é possível porque o circuito possui elementos de memória, como flip-flops.

## Exemplos

- latches
- flip-flops
- registradores
- contadores
- máquinas de estados (FSM)

## Por que isso é importante?

Porque é assim que hardware “lembra” coisas:

- armazenar um bit,
- contar eventos,
- manter estados (ex.: “verde”, “amarelo”, “vermelho” em um semáforo).

## Tabela comparativa

| Característica | Circuito combinacional | Circuito sequencial |
|---|---|---|
| Memória/estado | Não | Sim |
| Saída depende do passado? | Não | Sim |
| Depende de clock? | Normalmente não | Normalmente sim |
| Exemplos | portas, somador, mux | registrador, contador, FSM |

> Observação: existem detalhes e exceções, mas esta visão é suficiente para uma introdução.

Na próxima página, vamos entender clock e um flip-flop tipo D com um exemplo VHDL simples.

