# Resumo

## Recapitulação dos principais pontos

- PLDs permitem **configurar hardware** depois da fabricação.
- ASIC é **fixo e otimizado**, mas tem alto custo inicial e pouca flexibilidade.
- CPLD e FPGA são programáveis; CPLD tende a ser melhor para **controle**, FPGA para **complexidade e paralelismo**.
- Um FPGA é **hardware reconfigurável**: ele é configurado para virar um circuito.
- LUTs implementam lógica como pequenas tabelas de consulta (tabela verdade).
- FPGAs modernos podem ter memória interna e **blocos DSP**.
- Blocos DSP aceleram operações matemáticas comuns (multiplicar, somar, acumular).
- Paralelismo é uma grande vantagem de FPGAs em DSP.
- FPGA não é a melhor escolha para tudo: depende do requisito do projeto.

## Tabela de conceitos (para revisar)

| Conceito | O que é (em uma frase) |
|---|---|
| PLD | Dispositivo lógico programável (hardware configurável) |
| ASIC | Chip fixo para uma aplicação específica |
| CPLD | PLD complexo, bom para controle e projetos menores |
| FPGA | PLD com muitos blocos e alta flexibilidade |
| CLB | Bloco lógico configurável |
| IOB | Bloco de entrada/saída |
| Switch Matrix | Matriz que conecta blocos (roteamento) |
| LUT | Tabela de consulta que implementa funções lógicas |
| Flip-flop | Armazenamento de estado (1 bit) |
| Memória interna | Memória no chip para dados/apoio |
| Bloco DSP | Unidade matemática otimizada (MAC e afins) |
| DSP | Processamento Digital de Sinais |
| MAC | Multiplica e acumula (resultado = resultado + a*b) |
| Paralelismo | Várias operações ao mesmo tempo |
| Síntese | Transformar descrição de hardware em mapeamento no FPGA |
| Bitstream | Arquivo de configuração do FPGA |

## Frases‑chave para memorização

- Um FPGA é um hardware reconfigurável.
- FPGAs permitem implementar circuitos digitais personalizados sem fabricar um ASIC.
- LUTs implementam funções lógicas por meio de pequenas tabelas verdade.
- Blocos DSP aceleram operações matemáticas comuns em processamento de sinais.
- O paralelismo é uma das grandes vantagens dos FPGAs.
- FPGA não é sempre a melhor escolha; a decisão depende dos requisitos do projeto.
- Em DSP, multiplicação e acumulação aparecem com muita frequência.
- Blocos DSP ajudam a melhorar desempenho e economizar recursos lógicos.

