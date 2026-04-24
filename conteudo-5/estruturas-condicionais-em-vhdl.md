---
description: >-
  Nesta página do Conteúdo 5, você vai entender estruturas condicionais em vhdl
  (introdução) de forma progressiva, com foco no essencial para iniciantes.
---

# Estruturas condicionais em VHDL (introdução)

Em VHDL, existem formas diferentes de descrever lógica combinacional por “regras”.

Aqui vamos ver, de forma introdutória:

- `when/else`
- `with/select`

E vamos comentar rapidamente:

- `if/elsif/else`
- `case/when` (geralmente dentro de `process`)

## Preparando: um vetor com 3 bits

Imagine que juntamos as entradas `c`, `h`, `p` em um vetor de 3 bits chamado `chp`:

- `chp(2)` representa `c`
- `chp(1)` representa `h`
- `chp(0)` representa `p`

E que valores como `"001"` representam combinações:

- `"001"` → c=0, h=0, p=1
- `"010"` → c=0, h=1, p=0
- `"011"` → c=0, h=1, p=1

> Atenção: isso é uma convenção do exemplo.

## Exemplo com `when/else`

```vhdl
f <= '1' when chp = "001" else
     '1' when chp = "010" else
     '1' when chp = "011" else
     '0';
```

Como ler:

- se `chp` for `"001"`, `f` vale 1
- senão, se for `"010"`, `f` vale 1
- senão, se for `"011"`, `f` vale 1
- senão, `f` vale 0

Isso casa com a ideia de `f = not c and (h or p)`:

- `f` é 1 apenas quando c=0 e pelo menos uma das outras entradas é 1.

## Exemplo com `with/select`

```vhdl
with chp select
    f <= '1' when "001",
         '1' when "010",
         '1' when "011",
         '0' when others;
```

Explicação:

- `with chp select` significa “escolha o valor de `f` com base em `chp`”.
- `others` representa qualquer outra combinação.

## E o `if/elsif/else` e `case/when`?

Eles são muito comuns, mas geralmente aparecem dentro de um bloco `process`.

Por enquanto, guarde a ideia:

- `when/else` e `with/select` são formas legais de descrever combinacional.
- `if` e `case` costumam aparecer quando você organiza lógica em um `process`.

Na próxima página, vamos entrar no conceito de **circuitos sequenciais** (onde existe memória/estado).

