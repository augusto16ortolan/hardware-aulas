# Função dentro da `architecture`

## Onde uma função pode ser declarada?

De forma comum e didática, você pode declarar uma função:

- no preâmbulo da `architecture` (antes do `begin`),
- dentro de um `package` (para reutilizar em vários arquivos/projetos).

Neste momento, vamos focar na `architecture`.

## Declarar vs chamar a função

- **Declarar** é escrever a função (definir o nome, parâmetros, retorno e corpo).
- **Chamar** é usar a função para obter um valor (ex.: `soma(a_1, b_1)`).

## Regra importante de posição

Quando a função é declarada na `architecture`, ela fica:

- **antes** do `begin` (no “preâmbulo”),
- e pode ser usada **depois** do `begin`.

## Exemplo completo (simples)

```vhdl
library ieee;
use ieee.std_logic_1164.all;

entity exefun is
port (
    a_1, b_1 : in integer range 0 to 15;
    s_1      : out integer range 0 to 15
);
end exefun;

architecture hard of exefun is

    function soma (a : integer; b : integer) return integer is
        variable s : integer;
    begin
        s := a + b;
        return s;
    end soma;

begin

    s_1 <= soma(a_1, b_1);

end hard;
```

## Explicando por partes

### `library` e `use`

- `library ieee;` e `use ieee.std_logic_1164.all;` importam tipos e funções comuns para sinais digitais.
  - Neste exemplo, não estamos usando `std_logic` diretamente nas portas, mas manter esse padrão ajuda em projetos reais.

### `entity exefun`

Define a interface:

- entradas: `a_1` e `b_1` (inteiros de 0 a 15),
- saída: `s_1` (inteiro de 0 a 15).

### `architecture hard`

Define como o circuito funciona.

### Declaração da função (antes do `begin`)

```vhdl
function soma (a : integer; b : integer) return integer is
    variable s : integer;
begin
    s := a + b;
    return s;
end soma;
```

- `a` e `b` são parâmetros.
- `s` é uma variável local (só existe dentro da função).
- `s := a + b;` calcula a soma.
- `return s;` retorna o resultado.

### Uso da função (depois do `begin`)

```vhdl
s_1 <= soma(a_1, b_1);
```

- chama a função com as entradas,
- recebe um valor,
- atribui esse valor à saída.

## Por que isso é útil?

- A lógica da soma fica “escondida” dentro da função.
- O corpo principal da `architecture` fica mais simples e legível.
- A função retorna um único valor e pode ser reaproveitada.

Na próxima página, vamos falar de parâmetros, retorno e variáveis locais, e também da diferença entre `signal` e `variable`.

