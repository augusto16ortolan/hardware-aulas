# Paralelismo em FPGA para DSP

## O que é paralelismo?

**Paralelismo** é a ideia de executar **várias operações ao mesmo tempo**.

Em hardware, isso pode significar:

- ter vários “caminhos” de circuito trabalhando simultaneamente.

## CPU vs FPGA (ideia central)

De forma introdutória:

- Em uma **CPU**, muitas operações seguem uma sequência de instruções (mesmo com otimizações).
- Em um **FPGA**, você pode construir um circuito com várias partes trabalhando em paralelo.

Isso é muito útil em DSP, porque:

- há muitas amostras para processar;
- há muitos cálculos repetitivos (multiplicar e somar).

## Múltiplos blocos DSP trabalhando juntos

Se um FPGA tem vários blocos DSP, você pode:

- realizar várias multiplicações simultaneamente;
- somar resultados em etapas;
- gerar saídas em alta taxa.

## Exemplo didático: processar 4 amostras

Imagine que você precisa processar 4 amostras `x0, x1, x2, x3`.

Em uma CPU (visão simplificada):

- processa uma sequência de instruções para calcular resultados.

Em um FPGA (visão simplificada):

- pode ter vários blocos fazendo `x0*c0`, `x1*c1`, `x2*c2`, `x3*c3` ao mesmo tempo.

## Comparação (tabela)

| Característica | CPU | FPGA com blocos DSP |
|---|---|---|
| Execução | Instruções sequenciais (visão geral) | Circuitos trabalhando em paralelo |
| Paralelismo | Limitado e gerenciado pela arquitetura | Alto, definido pelo projeto |
| Flexibilidade | Fácil de reprogramar | Reconfigurável, mas exige projeto |
| Desempenho em DSP | Bom para geral, depende do caso | Pode ser excelente em contas repetitivas |
| Consumo de recursos | Menos “hardware dedicado” | Usa recursos do FPGA (LUT/RAM/DSP) |
| Aplicações | Computação geral | DSP, vídeo, telecom, aceleração |

