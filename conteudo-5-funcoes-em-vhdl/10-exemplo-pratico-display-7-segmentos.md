# Exemplo prático: função para display de 7 segmentos

Um display de 7 segmentos tem 7 “barrinhas” (segmentos) que podem ser ligadas/desligadas para formar números.

Vamos chamar os segmentos de:

- `a, b, c, d, e, f, g`

E vamos representar o estado desses segmentos com um vetor de 7 bits:

- `display(6)` … `display(0)` (ordem didática definida pelo projeto)

> Observação: o padrão exato depende do display (ânodo/cátodo comum) e do mapeamento físico. Aqui vamos usar um mapeamento didático fixo só para estudar funções.

## Ideia da função

Queremos uma função que:

- recebe um número de 0 a 9,
- retorna um `std_logic_vector(6 downto 0)` com o padrão dos segmentos.

## Exemplo completo (didático)

```vhdl
library ieee;
use ieee.std_logic_1164.all;

entity conversor_display is
port (
    numero  : in integer range 0 to 9;
    display : out std_logic_vector(6 downto 0)
);
end conversor_display;

architecture behavioral of conversor_display is

    function converte_display(valor : integer) return std_logic_vector(6 downto 0) is
    begin
        case valor is
            when 0 => return "1111110";
            when 1 => return "0110000";
            when 2 => return "1101101";
            when 3 => return "1111001";
            when 4 => return "0110011";
            when 5 => return "1011011";
            when 6 => return "1011111";
            when 7 => return "1110000";
            when 8 => return "1111111";
            when 9 => return "1111011";
            when others => return "0000000";
        end case;
    end function;

begin

    display <= converte_display(numero);

end behavioral;
```

## Explicação por blocos

### `entity`

- `numero` é a entrada (0 a 9).
- `display` é a saída (7 bits).

### Função `converte_display`

- recebe `valor` (inteiro),
- usa `case` para escolher qual padrão retornar,
- cada `when` retorna um vetor de 7 bits.

### Uso da função

```vhdl
display <= converte_display(numero);
```

O corpo principal fica simples:

- a conversão está encapsulada na função,
- a `architecture` só conecta entrada e saída.

## Por que isso é um bom exemplo de função?

- É uma lógica que se repete em muitos projetos (display).
- É fácil de dar um nome claro (`converte_display`).
- Retorna um único valor (o padrão do display).
- Ajuda a manter o código principal limpo.

Na próxima página, vamos usar a mesma função em um exemplo sequencial: um cronômetro simples que conta de 0 a 9.

