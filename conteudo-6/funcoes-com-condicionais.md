---
description: >-
  Nesta página do Conteúdo 6, você vai entender funções com condicionais de forma
  progressiva, com foco no essencial para iniciantes.
---

# Funções com condicionais

Funções podem conter `if`, `elsif`, `else` e decidir qual valor retornar.

## Por que toda condição precisa levar a um `return`?

Porque a função prometeu devolver um valor do tipo declarado. Se existir um caminho que “não retorna”, o compilador pode acusar erro (e, conceitualmente, ficaria indefinido).

## Exemplo: verificar se um número é zero

```vhdl
function eh_zero (valor : integer) return boolean is
begin
    if valor = 0 then
        return true;
    else
        return false;
    end if;
end function;
```

### Usando o resultado da função

```vhdl
saida <= '1' when eh_zero(contador) else '0';
```

Explicação:

- a função retorna `true` ou `false`,
- a atribuição usa esse resultado para decidir a saída,
- fica mais legível, porque `eh_zero(...)` já explica a intenção.

## Exemplo: limitar um valor entre 0 e 9

```vhdl
function limita_0_9 (valor : integer) return integer is
begin
    if valor < 0 then
        return 0;
    elsif valor > 9 then
        return 9;
    else
        return valor;
    end if;
end function;
```

Explicação:

- se `valor < 0`, retorna 0,
- se `valor > 9`, retorna 9,
- caso contrário, retorna o próprio valor.

## O que isso “vira” em hardware?

Conceitualmente:

- uma função com `if/else` descreve uma lógica de seleção (como multiplexadores).

Você não ganha “um bloco mágico”; você descreve uma decisão lógica que o sintetizador (quando for o caso) transforma em hardware.

Na próxima página, vamos trabalhar com funções que recebem vetores (`bit_vector`) e usar `'length` e `for`.

