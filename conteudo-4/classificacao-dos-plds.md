# Classificação dos PLDs (visão introdutória)

PLDs podem ser organizados em uma “família” de dispositivos, desde opções bem simples até as mais complexas.

## Estrutura geral (para visualizar)

PLDs

- Arranjos lógicos programáveis
  - PROM
  - PAL
  - PLA
- Arranjos de portas programáveis
  - SPLD
  - CPLD
  - FPGA

## Explicando o básico (sem aprofundar demais)

### PROM

Uma forma clássica de implementar lógica:

- arranjo **AND fixo**
- arranjo **OR programável**

Hoje, PROM é mais lembrada como conceito histórico e base de entendimento.

### PAL

- arranjo **AND programável**
- arranjo **OR fixo**

### PLA

- arranjos **AND e OR programáveis**

> Observação: PROM/PAL/PLA aparecem como degraus de evolução e ideias de implementação. O foco aqui é preparar o terreno para CPLD e FPGA.

### SPLD

*Simple PLD*: dispositivos programáveis mais simples, para lógicas menores.

### CPLD

*Complex PLD*: mais recursos que SPLD, muito usados em:

- lógica de controle;
- decodificação;
- “cola” entre componentes (glue logic).

### FPGA

Um passo além:

- muitos blocos lógicos menores;
- interconexões programáveis;
- alta flexibilidade;
- recursos extras (memória interna, DSP, etc.).

## Tabela (resumo rápido)

| Dispositivo | Característica principal | Exemplo de uso |
|---|---|---|
| PROM | Conceito de lógica via arranjos | Implementações simples/históricas |
| PAL | Estrutura mais rígida que PLA | Lógica simples e rápida |
| PLA | AND/OR programáveis | Lógicas combinacionais variadas |
| CPLD | Controle e previsibilidade | Decodificação, glue logic |
| FPGA | Alta flexibilidade e paralelismo | DSP, vídeo, telecom, protótipos |

