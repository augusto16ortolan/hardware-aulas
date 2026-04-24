# Tecnologia LUT

## O que é LUT?

**LUT** significa *Look-Up Table* (tabela de consulta).

Em um FPGA, uma LUT pode ser entendida como:

- uma **pequena memória**;
- que armazena a saída de uma função lógica;
- para todas as combinações possíveis das entradas.

## Relação com tabela verdade

Se você tem uma função lógica com N entradas:

- existem `2^N` combinações possíveis de entradas;
- a LUT armazena a saída para cada combinação.

Exemplos:

- LUT de 2 entradas → 4 combinações
- LUT de 4 entradas → 16 combinações
- LUT de 5 entradas → 32 combinações

## Como a LUT funciona (ideia de endereço)

Pense assim:

- as entradas da LUT são como um **endereço**;
- o valor armazenado naquele endereço é a **saída**.

## Exemplo simples: função AND

Função AND com duas entradas `A` e `B`:

| A | B | Saída AND |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

Em uma LUT de 2 entradas:

- cada combinação (A,B) aponta para uma posição;
- a posição guarda o valor da saída.

## Por que LUTs são importantes?

Porque elas permitem implementar:

- portas lógicas simples (AND, OR, NOT, XOR);
- funções lógicas mais complexas;
- sem precisar de um conjunto fixo de portas internas.

## Comparação (bem introdutória)

| Porta lógica tradicional | LUT em FPGA |
|---|---|
| Implementada por transistores dedicados para aquela porta | Implementada como uma pequena memória configurada |
| Função fixa | Função configurável |
| Normalmente não muda | Pode mudar ao reprogramar o FPGA |

