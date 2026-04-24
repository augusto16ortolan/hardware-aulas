---
description: >-
  Nesta página do Conteúdo 4, você vai entender arquitetura básica de um fpga de
  forma progressiva, com foco no essencial para iniciantes.
---

# Arquitetura básica de um FPGA

Para entender por que FPGAs são tão flexíveis, precisamos olhar para a arquitetura típica deles.

Em nível introdutório, um FPGA pode ser visto como:

- muitos blocos de lógica;
- muitos caminhos de conexão entre esses blocos;
- blocos de entrada e saída;
- recursos especializados (memória e DSP).

## Componentes principais (explicação curta)

### CLB (Configurable Logic Block)

Blocos lógicos configuráveis, usados para implementar funções lógicas e pequenos circuitos.

Eles normalmente incluem:

- **LUTs** (para lógica combinacional)
- **flip-flops** (para armazenamento/estado)

### IOB (Input/Output Block)

Blocos de entrada e saída que fazem a interface entre:

- pinos físicos do chip
- e a lógica interna do FPGA

### Switch Matrix (matriz de interconexão)

É a estrutura que permite **rotear** sinais, conectando:

- CLBs entre si
- CLBs com IOBs
- CLBs com memória e DSP

Isso é essencial para o FPGA “virar” o circuito desejado.

### Interconexões programáveis

São caminhos que podem ser configurados para ligar blocos diferentes, formando o circuito final.

### LUT (Look-Up Table)

Uma LUT é uma pequena tabela (como uma memória pequena) que implementa funções lógicas.

Você vai ver isso com mais detalhes na próxima página.

### Flip-flops

Guardam 1 bit de estado e permitem circuitos sequenciais (com clock).

### Memórias internas

FPGAs modernos podem ter memórias internas para:

- guardar dados temporários;
- implementar buffers;
- apoiar algoritmos.

### Blocos DSP

São unidades especializadas para operações matemáticas comuns em DSP:

- multiplicação
- soma
- acumulação

Eles ajudam a acelerar cálculos e economizar recursos lógicos (LUTs).

## Tabela (componente, função e exemplo)

| Componente | Função no FPGA | Exemplo de uso |
|---|---|---|
| CLB | Implementar lógica e pequenos circuitos | Contadores, decodificadores |
| IOB | Interface com pinos externos | Ler botão, gerar sinal para LED |
| Switch Matrix | Conectar/rotear sinais | Montar caminhos entre blocos |
| LUT | Implementar lógica combinacional | AND/OR e funções maiores |
| Flip-flops | Guardar estado | Registradores, FSMs |
| Memória interna | Armazenar dados | Buffer de amostras, filas |
| Bloco DSP | Operações matemáticas eficientes | MAC em filtros e IA |

Sugestão de imagem: diagrama simples mostrando CLBs, IOBs, Switch Matrix, LUTs e blocos DSP dentro de um FPGA.

