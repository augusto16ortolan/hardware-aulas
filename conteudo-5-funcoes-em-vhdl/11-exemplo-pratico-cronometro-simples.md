# Exemplo prático: cronômetro simples (0 a 9)

Agora vamos juntar:

- um circuito **sequencial** (contador que muda no clock),
- com um circuito **combinacional** (conversão do número para o display).

O objetivo:

- contar de 0 a 9,
- mostrar o valor em um display de 7 segmentos.

> Observação: este exemplo é didático. Em um projeto real, você normalmente precisaria dividir o clock (para a contagem ficar visível), mas isso foge do escopo aqui.

## Exemplo completo (didático)

```vhdl
library ieee;
use ieee.std_logic_1164.all;

entity cronometro is
port (
    clk     : in std_logic;
    reset   : in std_logic;
    display : out std_logic_vector(6 downto 0)
);
end cronometro;

architecture behavioral of cronometro is

    signal contador : integer range 0 to 9 := 0;

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

    process(clk, reset)
    begin
        if reset = '1' then
            contador <= 0;
        elsif rising_edge(clk) then
            if contador = 9 then
                contador <= 0;
            else
                contador <= contador + 1;
            end if;
        end if;
    end process;

    display <= converte_display(contador);

end behavioral;
```

## Explicando o que acontece

### Parte sequencial: contador

- `process(clk, reset)` descreve um bloco que reage ao clock e ao reset.
- se `reset = '1'`, o contador volta para 0.
- na borda de subida (`rising_edge(clk)`), o contador soma 1.
- quando chega em 9, volta para 0.

Isso descreve um circuito com memória (estado): **sequencial**.

### Parte combinacional: conversão para display

```vhdl
display <= converte_display(contador);
```

A saída `display` depende apenas do valor atual do contador:

- isso é lógica combinacional (conversão).

## Por que usar função aqui ajuda?

- a lógica do display fica toda em um lugar só,
- se você quiser mudar o padrão, muda apenas na função,
- o código do contador fica mais fácil de ler.

Na próxima página, vamos resumir os conceitos principais do conteúdo.

