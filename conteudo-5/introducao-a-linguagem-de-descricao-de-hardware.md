---
description: >-
  Introdução e visão geral do Conteúdo 5, com objetivos de aprendizagem e a
  sequência do que será estudado.
---

# CONTEÚDO 4 - Linguagem de descrição de hardware

Até agora, você estudou que computadores executam instruções e que existe uma grande variedade de arquiteturas. Agora vamos mudar um pouco o foco:

> “E se eu quiser **criar hardware digital** em vez de apenas programar software?”

Quando falamos em circuitos digitais (portas lógicas, somadores, registradores, controladores), existe um desafio: **como projetar algo grande e complexo de forma organizada**, testável e reaproveitável?

É aqui que entram as **HDLs** (Hardware Description Languages), as **linguagens de descrição de hardware**.

## Objetivos de aprendizagem

Ao final deste conteúdo, você deve ser capaz de:

- Explicar o que é uma **HDL** e por que ela não é “uma linguagem de programação comum”.
- Entender como uma HDL é usada para **descrever**, **simular** e (em alguns casos) **implementar** circuitos digitais.
- Reconhecer onde HDLs aparecem: **FPGA**, **CPLD**, **ASIC** e simulação.
- Identificar os elementos básicos do **VHDL**: `entity`, `architecture`, `port`, `signal`, `bit` e `bit_vector`.
- Diferenciar **circuitos combinacionais** e **sequenciais** e ver exemplos introdutórios.
- Entender o papel de **clock**, **flip-flops** e o conceito de **FSM** (máquina de estados finitos) de forma inicial.

## O que será estudado (sequência)

1. Por que descrever hardware (em vez de “desenhar tudo”)
2. O que é HDL e para que serve
3. Aplicações de HDL (FPGA, CPLD, ASIC, simulação)
4. Estrutura básica do VHDL (entity/architecture/ports/sinais)
5. Circuitos combinacionais em VHDL
6. Descrição estrutural vs. comportamental
7. Estruturas condicionais em VHDL (introdução)
8. Circuitos sequenciais (ideia de memória/estado)
9. Flip-flop e clock (exemplo simples)
10. Máquinas de estados finitos (FSM) (exemplo conceitual)
11. Ferramentas e fluxo de trabalho (simular vs sintetizar)
12. Resumo
13. Atividades com gabarito

## Por que HDL é importante?

Em circuitos pequenos, dá para desenhar tudo em um diagrama. Mas conforme o circuito cresce:

- aumenta o número de portas e conexões,
- fica mais difícil testar,
- fica mais difícil corrigir e manter,
- fica mais difícil garantir que está “certo” antes de montar o hardware.

Com uma HDL, você consegue:

- **descrever** o circuito de forma organizada,
- **simular** para ver se a lógica funciona,
- **sintetizar** (transformar a descrição em uma implementação) para FPGA/CPLD,
- documentar e comunicar melhor o projeto.

## Relação com circuitos digitais, FPGA, CPLD, ASIC e simulação

- **Circuitos digitais** são feitos de portas lógicas e blocos (somadores, registradores, multiplexadores).
- **FPGA** e **CPLD** são dispositivos que permitem “colocar” um circuito lá dentro sem fabricar um chip do zero.
- **ASIC** é um chip feito sob medida para uma aplicação (alto custo inicial, mas ótimo para grande escala).
- **Simulação** permite testar o comportamento antes de implementar fisicamente.

## HDL não é “programação comum”

Uma linguagem de programação comum (como C/Python) descreve uma **sequência de passos** que a CPU executa.

Uma HDL descreve **hardware**:

- sinais,
- entradas e saídas,
- componentes e conexões,
- comportamento lógico do circuito.

Algumas partes parecem “sequenciais” (como `process` em VHDL), mas representam hardware reagindo a sinais, especialmente ao **clock**.

