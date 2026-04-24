# Estrutura básica do VHDL (introdução)

## O que é VHDL?

**VHDL** é uma HDL usada para descrever circuitos digitais.

Ela permite:

- definir a interface do circuito (entradas e saídas),
- descrever o comportamento e/ou a estrutura,
- simular,
- e, em muitos casos, sintetizar para FPGA/CPLD.

## Conceitos básicos

### `entity` (entidade)

A `entity` define **a interface** do circuito:

- quais são as entradas,
- quais são as saídas,
- quais tipos de sinais entram e saem.

### `architecture` (arquitetura)

A `architecture` define **como o circuito funciona**:

- o comportamento,
- as conexões internas,
- os sinais internos.

### `port` (portas)

As `ports` são as entradas/saídas do circuito:

- `in` (entrada)
- `out` (saída)

### `signal` (sinais internos)

Sinais internos são “fios” dentro do circuito, usados para conectar partes internas.

### Tipos básicos: `bit` e `bit_vector`

Para começar:

- `bit` representa 0 ou 1.
- `bit_vector` representa um conjunto de bits (um “vetor” de bits).

> Observação: em projetos reais, é comum usar `std_logic` e `std_logic_vector`. Aqui vamos manter o básico com `bit`/`bit_vector` para focar no conceito.

## Exemplo VHDL (circuito combinacional simples)

```vhdl
entity exemplo_comb is
port (
    c, h, p : in bit;
    f       : out bit
);
end exemplo_comb;

architecture comportamento of exemplo_comb is
begin
    f <= (not c) and (h or p);
end comportamento;
```

## Explicação linha por linha

### 1) `entity exemplo_comb is`

Define o nome da entidade (o “módulo” do circuito): `exemplo_comb`.

### 2) `port ( ... )`

Define as portas (entradas e saídas):

- `c, h, p : in bit;` → três entradas de 1 bit cada.
- `f : out bit` → uma saída de 1 bit.

### 3) `end exemplo_comb;`

Finaliza a definição da entidade.

### 4) `architecture comportamento of exemplo_comb is`

Define uma arquitetura chamada `comportamento` para a entidade `exemplo_comb`.

### 5) `begin ... end comportamento;`

Dentro do `begin/end` fica a descrição do circuito.

### 6) `f <= (not c) and (h or p);`

Essa linha descreve a lógica:

- `not c` inverte a entrada `c`.
- `h or p` é 1 se `h` ou `p` for 1.
- `and` exige as duas condições.

Ou seja:

> `f` será 1 quando `c` for 0 e pelo menos uma das entradas `h` ou `p` for 1.

> Importante: isso descreve um circuito lógico. Não é “um programa que roda em sequência”; é uma relação entre sinais.

Na próxima página, vamos falar especificamente de **circuitos combinacionais** e tabela-verdade.

