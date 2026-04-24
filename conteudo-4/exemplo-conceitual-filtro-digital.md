# Exemplo conceitual: filtro digital

Aqui vamos ver um padrão clássico de DSP sem entrar em VHDL avançado.

## Ideia geral

Um filtro digital:

- recebe amostras de entrada;
- multiplica cada amostra por um coeficiente;
- soma os resultados;
- gera a saída.

## Fórmula conceitual

```text
saida = (x0 * c0) + (x1 * c1) + (x2 * c2) + (x3 * c3)
```

Onde:

- `x0, x1, x2, x3` são amostras do sinal
- `c0, c1, c2, c3` são coeficientes do filtro

## O padrão de operações

```text
x0 * c0
x1 * c1
x2 * c2
x3 * c3
somar resultados
gerar saída
```

## Onde entram os blocos DSP?

Cada multiplicação `xi * ci` pode, conceitualmente, ser feita por um bloco DSP.

E as somas podem ser organizadas em hardware para:

- formar uma árvore de soma;
- manter uma boa taxa de processamento.

## CPU vs FPGA (entendimento didático)

- Em uma CPU, isso é calculado por instruções (multiplica, soma, repete).
- Em um FPGA, isso pode ser implementado como um circuito dedicado.
- Blocos DSP tornam esse circuito mais eficiente para multiplicar e acumular.

## Observação importante

Esse exemplo é propositalmente simples. Em projetos reais, existem detalhes como:

- número maior de coeficientes;
- controle de precisão (ponto fixo, etc.);
- pipeline e temporização.

Mas para um primeiro contato, o foco é reconhecer o padrão: **muitas multiplicações + muitas somas**.

