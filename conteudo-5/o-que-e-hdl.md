---
description: >-
  Explicação introdutória de "O que é HDL?", definindo o conceito e mostrando por
  que ele é importante neste conteúdo.
---

# O que é HDL?

## O que significa HDL?

**HDL** vem de **Hardware Description Language**.

Tradução: **Linguagem de Descrição de Hardware**.

## Objetivo de uma HDL

Uma HDL serve para **descrever circuitos digitais** de forma:

- organizada,
- testável (simulação),
- reutilizável,
- e, em muitos casos, implementável em dispositivos programáveis.

Ela pode descrever:

- a **estrutura** (quais componentes existem e como se conectam),
- e/ou o **comportamento** (o que o circuito deve fazer).

## Diferença entre descrever software e descrever hardware

Uma forma simples de comparar:

- Em uma linguagem de programação, normalmente descrevemos uma **sequência de instruções** para a CPU executar (passo a passo).
- Em uma HDL, descrevemos **circuitos**, com sinais que existem “ao mesmo tempo” e reagem às entradas e ao clock.

Isso muda a forma de pensar:

- hardware não é “uma lista de comandos”;
- hardware é “um conjunto de blocos conectados”, onde sinais mudam e afetam outros sinais.

## Descrever comportamento e estrutura

### Descrição estrutural

Você diz:

- quais portas/blocos existem,
- como elas se conectam.

### Descrição comportamental

Você diz:

- a regra do que deve acontecer,
- sem necessariamente listar cada porta.

Por exemplo, em vez de desenhar as portas, você pode escrever uma expressão lógica que representa a saída.

## Como HDL ajuda no projeto (do começo ao fim)

Uma HDL é útil para:

- **projeto:** organizar o circuito em módulos.
- **documentação:** o código vira uma documentação do circuito.
- **simulação:** testar se o circuito se comporta como esperado.
- **síntese:** transformar a descrição em uma implementação (por exemplo, em FPGA).
- **implementação:** carregar o circuito no dispositivo (FPGA/CPLD) e testar.

> Importante: nem todo código HDL é automaticamente sintetizável. Algumas construções servem para simulação, outras para síntese. Aqui, o foco é introdutório.

## Exemplos de HDLs

Algumas linguagens famosas:

- **VHDL** (muito usada em ensino e indústria)
- **Verilog**
- **SystemVerilog**
- **SystemC** (mais próxima de C++, usada em modelagem em níveis mais altos)

Neste conteúdo, o foco introdutório será em **VHDL**, mas sem aprofundar demais.

