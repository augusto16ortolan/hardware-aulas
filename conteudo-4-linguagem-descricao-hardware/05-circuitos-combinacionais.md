# Circuitos combinacionais

## O que são circuitos combinacionais?

Um **circuito combinacional** é aquele em que:

> a saída depende apenas das entradas atuais.

Ou seja: não existe “memória” do que aconteceu antes.

## Exemplos comuns

- portas lógicas (AND, OR, NOT…)
- somadores
- multiplexadores
- comparadores

## Descrevendo combinacional em VHDL

Em VHDL, circuitos combinacionais podem ser descritos:

- de forma **comportamental** (com uma expressão ou regras),
- ou de forma **estrutural** (conectando portas/blocos).

Neste início, vamos usar a forma comportamental por ser mais direta.

## Exemplo: três entradas e uma saída

Vamos usar:

- entradas: `c`, `h`, `p`
- saída: `f`

Expressão lógica:

> **f = not c and (h or p)**

### O que isso significa?

`f` será 1 apenas quando:

- `c = 0`
- e pelo menos uma das entradas `h` ou `p` for 1.

## Tabela-verdade

| c | h | p | f |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 0 |

### Interpretando

Repare que `f = 1` apenas quando:

- `c` é 0 (por causa do `not c`),
- e `h or p` é 1 (ou seja, `h = 1` ou `p = 1`).

## Estrutural vs. comportamental (introdução)

- **Comportamental:** “f é igual a esta expressão”.
- **Estrutural:** “f vem de uma porta AND conectada a uma porta NOT e a uma porta OR…”.

Na próxima página, vamos comparar essas duas formas com mais calma.

