# Parâmetros, retorno e variáveis (e `signal` vs `variable`)

## O que são parâmetros?

Parâmetros são os valores que a função recebe para trabalhar.

Exemplos:

- um número (`integer`),
- um bit (`bit`),
- um vetor (`bit_vector`),
- etc.

## Como declarar parâmetros

Você declara cada parâmetro com:

- nome,
- tipo.

Exemplo:

```vhdl
function dobro (valor : integer) return integer is
    variable resultado : integer;
begin
    resultado := valor * 2;
    return resultado;
end function;
```

Explicação:

- `valor` é o parâmetro de entrada.
- `integer` após o `return` é o tipo do valor retornado.
- `resultado` é uma variável local usada no cálculo.

## Mais de um parâmetro

Você pode ter vários parâmetros separados por `;`.

Exemplo (retorna o maior):

```vhdl
function maior (a : integer; b : integer) return integer is
begin
    if a > b then
        return a;
    else
        return b;
    end if;
end function;
```

Repare que:

- todos os caminhos do `if` retornam um valor.

## Tipo de retorno

O tipo de retorno diz qual tipo o `return` deve devolver.

Se a função declara `return integer`, então o `return` precisa devolver algo compatível com `integer`.

## Variáveis locais

Variáveis locais são declaradas dentro da função e existem apenas ali.

Elas são úteis para:

- guardar resultados intermediários,
- organizar cálculos,
- deixar o código mais claro.

## Diferença básica: `signal` vs `variable`

Para iniciantes, dá para pensar assim:

- **`signal`** representa um sinal/conexão de hardware (um “fio”), muito usado em `architecture` e entre processos.
- **`variable`** é usada para cálculos temporários em contextos sequenciais (como funções e processos).

### Um resumo prático

- Em funções, é comum usar `variable` para organizar a conta.
- Para “aparecer” fora da função, a função retorna um valor que depois é usado em uma atribuição (`<=` ou `:=`, dependendo do contexto).

> Observação: existem regras importantes sobre quando um `signal` “atualiza” e quando uma `variable` “atualiza”. Para este conteúdo, o essencial é: variável é local e ajuda em cálculos sequenciais.

Na próxima página, vamos ver funções usando `if/elsif/else` e por que é importante sempre retornar um valor.

