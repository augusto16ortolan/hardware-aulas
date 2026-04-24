---
description: >-
  Nesta página do Conteúdo 4, você vai entender critérios de escolha: quando fpga
  com dsp faz sentido? de forma progressiva, com foco no essencial para
  iniciantes.
---

# Critérios de escolha: quando FPGA com DSP faz sentido?

FPGA é poderoso, mas não é a escolha certa para tudo.

Ele costuma fazer sentido quando há:

- muita operação repetitiva (multiplicar e somar);
- necessidade de tempo real/baixa latência;
- possibilidade de paralelizar o algoritmo;
- necessidade de flexibilidade de hardware (reconfiguração).

## Perguntas orientadoras

- O projeto precisa processar muitos dados em tempo real?
- Há muitas multiplicações e somas?
- Existe necessidade de baixa latência?
- O algoritmo pode ser paralelizado?
- O custo e o consumo são aceitáveis?
- A flexibilidade de reconfiguração é importante?
- Um microcontrolador ou CPU seria suficiente?
- O projeto precisa de interfaces específicas?

## Tabela (necessidade e justificativa)

| Necessidade do projeto | FPGA com DSP faz sentido? | Justificativa |
|---|---|---|
| Filtro de áudio simples | Depende | Pode ser feito em CPU/MCU; FPGA vale se houver baixa latência e muita taxa |
| Controle de LED | Não | Problema simples; MCU/CPLD geralmente basta |
| Processamento de vídeo em tempo real | Sim | Alto throughput e paralelismo |
| Rede neural embarcada (conceitual) | Depende | Se houver muitas MACs e paralelismo necessário, pode fazer sentido |
| Leitura simples de botão | Não | Não exige DSP nem paralelismo |
| Comunicação de alta velocidade | Sim | DSP e baixa latência são comuns |
| Sistema de radar (conceitual) | Sim | Processamento em tempo real e repetitivo |
| Automação simples | Depende | Se for controle básico, MCU; se houver muita lógica paralela, avaliar |

## Mensagem final

- FPGA não é sempre melhor que CPU/GPU.
- FPGA aumenta complexidade de desenvolvimento.
- Para tarefas simples, microcontroladores costumam ser mais adequados.
- Para DSP pesado e paralelo, FPGAs podem ser muito vantajosos.

