# Flip-flop e clock (introdução)

## O que é clock?

O **clock** é um sinal que “marca o ritmo” do circuito sequencial.

Pense nele como um metrônomo:

- a cada batida, o circuito pode atualizar seu estado.

## O que é borda de subida?

O clock fica alternando entre 0 e 1.

- **Borda de subida** é o momento em que o clock muda de 0 para 1.

Muitos circuitos sequenciais atualizam o estado **na borda de subida**.

## O que é flip-flop tipo D?

Um **flip-flop D** guarda 1 bit.

Ideia simplificada:

- ele tem uma entrada `d` (o valor a ser armazenado),
- e uma saída `q` (o valor armazenado),
- na borda do clock, ele “captura” `d` e coloca em `q`.

É como tirar uma “foto” do valor `d` no instante do clock.

## Entradas e saídas comuns

- `clk`: clock
- `d`: dado de entrada
- `q`: saída armazenada
- `qn`: saída invertida (às vezes usada, às vezes não)

## Exemplo em VHDL (registrador de 1 bit)

```vhdl
entity registrador is
port (
    clk : in bit;
    d   : in bit;
    q   : out bit;
    qn  : out bit
);
end registrador;

architecture comportamento of registrador is
begin
    process(clk)
    begin
        if clk'event and clk = '1' then
            q  <= d;
            qn <= not d;
        end if;
    end process;
end comportamento;
```

## Explicação linha por linha

### 1) `entity registrador is ...`

Define a interface:

- `clk` e `d` são entradas.
- `q` e `qn` são saídas.

### 2) `process(clk)`

Indica que este bloco “reage” a mudanças no sinal `clk`.

### 3) `if clk'event and clk = '1' then`

Isso identifica a **borda de subida**:

- `clk'event` indica que houve um evento (mudança) no clock.
- `clk = '1'` indica que o clock agora está em 1.

### 4) `q <= d;`

Na borda de subida, `q` recebe o valor de `d`.

### 5) `qn <= not d;`

Na borda de subida, `qn` recebe o inverso de `d`.

## O que esse código representa?

Ele representa **armazenamento de informação**:

- entre uma borda e outra do clock, o valor fica “guardado”.

Na próxima página, vamos ver o conceito de máquina de estados finitos (FSM), muito usado em controle de hardware.

