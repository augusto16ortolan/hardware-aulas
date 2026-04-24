---
description: >-
  Explicação introdutória de "O que é FPGA?", definindo o conceito e mostrando por
  que ele é importante neste conteúdo.
---

# O que é FPGA?

## Significado

**FPGA** significa *Field Programmable Gate Array*.

Uma tradução comum é:

- **Arranjo de Portas Programáveis em Campo**

## O que significa “programável em campo”?

Significa que o dispositivo pode ser configurado **pelo usuário**, fora da fábrica (no “campo”), para implementar um circuito.

Isso é diferente de um chip com função fixa, que sai pronto da fabricação sem possibilidade de mudança.

## FPGA é hardware reconfigurável

Um FPGA é considerado **hardware reconfigurável** porque:

- você pode programar uma configuração hoje e outra amanhã;
- o mesmo chip pode virar circuitos diferentes em projetos diferentes.

## FPGA não é “software rodando”

Esse ponto é muito importante:

- um FPGA **não** executa uma sequência de comandos como uma CPU.
- em vez disso, ele é configurado para **se comportar como um circuito digital**.

## Como descrevemos o circuito?

Para descrever a lógica que vai para o FPGA, usamos linguagens de descrição de hardware, como:

- **VHDL**
- **Verilog**

Você descreve o comportamento/estrutura do circuito, e a ferramenta transforma isso em uma configuração para o chip.

## Analogia (bem didática)

- Um processador comum executa **instruções**.
- Um FPGA é configurado para virar um **circuito específico**.

## Exemplos de uso (visão geral)

- Prototipagem de hardware
- Processamento de sinais (áudio, imagem, vídeo)
- Controle industrial
- Telecomunicações
- Aceleração de algoritmos
- Sistemas embarcados
- Inteligência artificial (em alguns cenários)
- Comunicação de alta velocidade (ex.: aplicações em redes modernas)

