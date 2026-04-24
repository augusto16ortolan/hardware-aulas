---
description: >-
  Nesta página do Conteúdo 4, você vai entender fluxo de desenvolvimento em fpga
  (visão básica) de forma progressiva, com foco no essencial para iniciantes.
---

# Fluxo de desenvolvimento em FPGA (visão básica)

Projetar para FPGA envolve um fluxo de etapas. Você não “compila e roda” como um programa comum: você descreve hardware e gera uma configuração para o chip.

## Etapas do fluxo

### 1) Definição do problema

Entender o que o circuito deve fazer:

- entradas, saídas, taxa de dados, latência, consumo, etc.

### 2) Descrição do hardware (VHDL ou Verilog)

Você descreve a lógica digital:

- combinacional (LUTs)
- sequencial (flip-flops)
- estruturas maiores (máquinas de estado, pipelines, etc.)

### 3) Simulação

Antes de ir para o chip, você testa o comportamento:

- verifica se a lógica faz sentido;
- encontra erros cedo.

### 4) Síntese

A ferramenta transforma a descrição do hardware em:

- uma rede lógica interna (mapeada para recursos do FPGA).

### 5) Place and route (posicionamento e roteamento)

A ferramenta decide:

- onde cada bloco vai ficar no chip (place);
- como as conexões vão passar pelas interconexões (route).

### 6) Geração do bitstream

Gera um arquivo de configuração (muito conhecido como **bitstream**).

### 7) Programação do FPGA

Você grava essa configuração no dispositivo:

- o FPGA passa a se comportar como o circuito definido.

### 8) Testes no hardware

Com o FPGA programado, você testa:

- entradas/saídas reais;
- performance;
- estabilidade do projeto.

## Relação com DSP

Em uma aplicação DSP, você geralmente:

- define operações matemáticas (ex.: filtros, MAC);
- descreve o circuito;
- a ferramenta decide como usar LUTs, flip-flops, memória e **blocos DSP**;
- o bitstream final é carregado no FPGA.

## Ferramentas (exemplos)

Existem ferramentas específicas para trabalhar com FPGAs, por exemplo:

- Intel Quartus
- Xilinx Vivado

> Observação: aqui o objetivo é entender o fluxo, não dominar as ferramentas.

