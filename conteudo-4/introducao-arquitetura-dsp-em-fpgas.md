---
description: >-
  Introdução e visão geral do Conteúdo 4, com objetivos de aprendizagem e a
  sequência do que será estudado.
---

# CONTEÚDO 4 - Arquitetura DSP em FPGAs

Nos conteúdos anteriores, você viu conceitos importantes de hardware e arquitetura:

- **RISC e CISC** (ideias por trás de arquiteturas de processador)
- **Instruções de máquina** (como a CPU executa operações básicas)

Agora vamos mudar um pouco o foco: em vez de falar de um processador executando instruções, vamos falar de dispositivos que permitem **configurar hardware** para virar um circuito específico.

Esse é o universo dos **dispositivos lógicos programáveis**, onde se destacam os **FPGAs**.

## Por que isso é importante?

FPGAs são usados quando queremos:

- implementar circuitos digitais personalizados sem fabricar um chip novo;
- prototipar rapidamente um sistema de hardware;
- explorar **paralelismo** (várias operações ao mesmo tempo);
- acelerar operações matemáticas em tempo real (como em áudio, vídeo e telecom).

E um dos recursos que tornam isso mais eficiente em FPGAs modernos são os **blocos DSP** — unidades especializadas para contas frequentes em processamento de sinais, como:

- multiplicação;
- soma;
- acumulação (somar e guardar resultado repetidamente);
- filtragem digital.

## Objetivos de aprendizagem

Ao final do conteúdo, você deve ser capaz de:

- Compreender o que são **dispositivos lógicos programáveis**.
- Diferenciar **ASIC**, **PLD**, **CPLD** e **FPGA**.
- Entender a arquitetura básica de um FPGA (visão geral).
- Identificar componentes típicos de um FPGA: **CLB**, **IOB**, **Switch Matrix**, **LUT**, flip-flops, memória e **blocos DSP**.
- Compreender o papel dos **blocos DSP** em FPGAs.
- Relacionar **DSP** (processamento digital de sinais) com aplicações práticas.
- Identificar aplicações de FPGAs com DSP.
- Comparar **FPGA** e **CPLD** em nível introdutório.

## O que será estudado (sequência)

1. Dispositivos lógicos programáveis (PLDs): ideia e motivação
2. ASIC, PLD, CPLD e FPGA: como se diferenciam e se relacionam
3. Classificação dos PLDs (visão geral)
4. O que é FPGA? (conceito e “programável em campo”)
5. Arquitetura básica de um FPGA (blocos e interconexões)
6. Tecnologia LUT (como lógica é implementada)
7. CPLD vs FPGA (quando usar cada um)
8. O que é DSP? (processamento digital de sinais)
9. Blocos DSP em FPGAs (por que existem e o que fazem)
10. Paralelismo em FPGA para DSP (por que acelera)
11. Exemplo conceitual: filtro digital (padrão de multiplicar e somar)
12. Aplicações de DSP em FPGAs
13. Fluxo de desenvolvimento em FPGA (do VHDL/Verilog ao bitstream)
14. Critérios de escolha (quando FPGA com DSP faz sentido)
15. Resumo e fixação
16. Atividades com gabarito

## Conexão com a disciplina (sem confundir com CPU)

Uma CPU tradicional executa instruções em sequência (mesmo que internamente use otimizações).

Um FPGA, por outro lado, é **configurado** para se comportar como um circuito digital. Ou seja:

- CPU: “executa um programa”
- FPGA: “vira o circuito”

Essa diferença vai aparecer várias vezes ao longo das próximas páginas.

