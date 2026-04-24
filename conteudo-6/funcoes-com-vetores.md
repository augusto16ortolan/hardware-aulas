---
description: >-
  Nesta página do Conteúdo 6, você vai entender funções com vetores (`bit_vector`)
  de forma progressiva, com foco no essencial para iniciantes.
---

# Funções com vetores (`bit_vector`)

Funções podem receber vetores e retornar valores baseados nesses vetores.

## O que é `bit_vector`?

`bit_vector` é um vetor de bits (0 ou 1). Por exemplo:

```vhdl
signal a : bit_vector(0 to 3);
signal b : bit_vector(0 to 3);
```

Aqui, `a` e `b` têm 4 bits (índices 0,1,2,3).

## Atributo `'length`

O atributo `'length` retorna quantos elementos o vetor tem.

Exemplo: se `a` é `bit_vector(0 to 3)`, então `a'length = 4`.

## Exemplo: função que compara dois vetores

A função abaixo compara `a` e `b` bit a bit e retorna `true` se forem iguais.

> Observação didática: para simplificar o índice, vamos assumir vetores no formato `(0 to N)` (como nos sinais acima).

```vhdl
function equal(a, b : bit_vector) return boolean is
begin
    if a'length = b'length then
        for idx in 0 to a'length - 1 loop
            if a(idx) /= b(idx) then
                return false;
            end if;
        end loop;

        return true;
    else
        report "Tamanhos diferentes." severity note;
        return false;
    end if;
end function;
```

## Explicando a função

- `a` e `b` são vetores de bits.
- `a'length` retorna o tamanho do vetor `a`.
- primeiro a função verifica se os tamanhos são iguais.
- o `for` percorre os índices.
- se encontrar um bit diferente, retorna `false`.
- se terminar o laço sem diferenças, retorna `true`.
- se os tamanhos forem diferentes, retorna `false` e emite um `report` (útil na simulação).

## Usando a função

```vhdl
c <= '1' when equal(bva, bvb) else '0';
```

Como ler:

- se `bva` e `bvb` forem iguais, `c` recebe `'1'`,
- caso contrário, `c` recebe `'0'`.

> Lembrete: `report` é uma mensagem para simulação. Em síntese, muitas ferramentas ignoram ou restringem esse tipo de recurso.

Na próxima página, vamos aprender a colocar funções em `packages` para reutilizar em vários circuitos.

