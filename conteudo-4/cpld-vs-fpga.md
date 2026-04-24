---
description: >-
  Nesta página do Conteúdo 4, você vai entender cpld vs fpga de forma progressiva,
  com foco no essencial para iniciantes.
---

# CPLD vs FPGA

Tanto **CPLDs** quanto **FPGAs** são dispositivos lógicos programáveis, mas são usados em cenários diferentes.

## CPLD (visão introdutória)

Em geral, CPLDs são escolhidos para:

- projetos menores;
- lógica de controle;
- decodificação;
- “glue logic” (colar componentes diferentes).

Pontos típicos:

- estrutura com menos blocos (mas mais “grossos”);
- tempo de resposta mais previsível em muitas aplicações;
- inicialização rápida (dependendo do dispositivo).

## FPGA (visão introdutória)

Em geral, FPGAs são escolhidos para:

- projetos maiores e mais complexos;
- paralelismo;
- processamento digital de sinais (DSP);
- quando faz sentido usar memória interna e blocos DSP.

Pontos típicos:

- muitos blocos lógicos menores;
- interconexão mais segmentada e flexível;
- recursos especiais (RAM interna, DSP, etc.).

## Tabela comparativa

| Aspecto | CPLD | FPGA |
|---|---|---|
| Estrutura | Menos blocos maiores | Muitos blocos menores |
| Base tecnológica (ideia) | Foco em controle/cola | Foco em flexibilidade/paralelo |
| Inicialização | Geralmente rápida | Pode exigir configuração (bitstream) |
| Tempo de resposta | Mais previsível em lógica simples | Depende mais do projeto/roteamento |
| Flexibilidade | Média | Alta |
| Recursos especiais | Geralmente poucos | RAM, DSP, interconexões ricas |
| Aplicações | Controle, decodificação | DSP, vídeo, telecom, aceleração |
| Complexidade suportada | Menor | Alta |

## Quando escolher CPLD?

- Projeto menor
- Tempo de resposta crítico e previsível
- Inicialização rápida
- Baixo consumo (dependendo do caso)
- Lógica de controle

## Quando escolher FPGA?

- Projeto complexo
- Necessidade de paralelismo
- Processamento digital de sinais
- Uso de memória interna
- Uso de blocos DSP
- Prototipagem avançada

