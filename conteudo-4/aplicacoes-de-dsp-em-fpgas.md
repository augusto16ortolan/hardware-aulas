---
description: >-
  Nesta página do Conteúdo 4, você vai entender aplicações de dsp em fpgas de
  forma progressiva, com foco no essencial para iniciantes.
---

# Aplicações de DSP em FPGAs

FPGAs com blocos DSP aparecem quando precisamos processar sinais com:

- alta taxa de dados;
- baixa latência;
- paralelismo;
- operações repetitivas (multiplicar e somar).

Abaixo, alguns exemplos típicos (sem aprofundar demais).

## Exemplos de aplicações

- Processamento de áudio (filtragem, equalização)
- Processamento de imagem (realce, detecção)
- Processamento de vídeo (filtros, compressão em tempo real)
- Telecomunicações (modulação/demodulação, filtragem)
- Sistemas modernos de comunicação (quando há sinais e alta taxa)
- Radar e sensores (processamento em tempo real)
- Sensores industriais e instrumentação (filtros e análise)
- Robótica (fusão de sensores)
- Inteligência artificial / machine learning (operações repetitivas em alguns cenários)
- Sistemas embarcados e IoT (quando o processamento precisa ser rápido e eficiente)

## Tabela (aplicação, sinal, operação e por quê FPGA)

| Aplicação | Sinal processado | Exemplo de operação | Por que usar FPGA |
|---|---|---|---|
| Áudio | Amostras de som | Filtro e equalização | MAC repetitivo e baixa latência |
| Imagem | Pixels | Realce de bordas | Paralelismo por pixel/linha |
| Vídeo | Frames | Filtros por quadro | Alto throughput |
| Telecom | Rádio | Filtragem | Muitas multiplicações por amostra |
| Radar | Retornos de sinal | Detecção/filtragem | Tempo real e paralelismo |
| Instrumentação | Sensor | Média/filtragem | Resposta rápida e estabilidade |

## Lembrete

FPGA não é “melhor” sempre. Ele faz sentido quando:

- o problema tem muito paralelismo;
- há muita conta repetitiva;
- há necessidade de tempo real/baixa latência.

