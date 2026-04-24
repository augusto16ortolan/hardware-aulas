---
description: >-
  Nesta página do Conteúdo 6, você vai entender sintaxe básica de funções de forma
  progressiva, com foco no essencial para iniciantes.
---

# Sintaxe básica de funções

## Estrutura geral

Uma função tem, em geral, este formato:

```vhdl
function Nome_Funcao (parametros) return Tipo_Retorno is
begin
    -- corpo da função (sequencial)
    return valor;
end function;
```

## Explicando cada parte

- `function`: indica que você está criando uma função.
- `Nome_Funcao`: nome escolhido para a função (de preferência, claro e descritivo).
- `(parametros)`: dados de entrada (pode ter zero, um ou vários).
- `return Tipo_Retorno`: tipo do valor que a função vai devolver.
- `begin/end`: delimitam o corpo da função.
- `return valor`: devolve o resultado.

## Exemplo simples: soma

```vhdl
function soma (a : integer; b : integer) return integer is
begin
    return a + b;
end function;
```

Como ler:

- recebe `a` e `b` (inteiros),
- retorna um inteiro (a soma).

## Usando a função (chamada)

Em um contexto sequencial (por exemplo, dentro de um `process`), você pode fazer:

```vhdl
resultado := soma(5, 3);
```

Explicação:

- `a` recebe 5,
- `b` recebe 3,
- a função retorna 8,
- o valor retornado é guardado em `resultado`.

> Importante: esse exemplo é didático. Para compilar de verdade, `resultado` precisa ser uma variável e o código precisa estar dentro de um contexto VHDL adequado (como uma `architecture` e um `process`).

Na próxima página, vamos ver um exemplo completo: função declarada dentro da `architecture` e usada em uma atribuição concorrente.

