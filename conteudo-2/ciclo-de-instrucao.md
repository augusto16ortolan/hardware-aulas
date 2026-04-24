---
description: >-
  Nesta página do Conteúdo 2, você vai entender ciclo de instrução de forma
  progressiva, com foco no essencial para iniciantes.
---

# Ciclo de instrução

O processador executa um programa repetindo um ciclo básico para cada instrução.

## Etapas principais

1. **Busca (fetch)**
2. **Decodificação (decode)**
3. **Execução (execute)**
4. **Armazenamento/Escrita do resultado (write-back)**

> Sugestão de imagem: fluxo com as etapas Busca → Decodificação → Execução → Armazenamento.

## Componentes citados (bem introdutório)

- **PC (Program Counter / Contador de Programa):** guarda o endereço da próxima instrução.
- **Memória:** onde estão as instruções e dados.
- **Registradores:** onde a CPU guarda valores rápidos.
- **Unidade de controle:** coordena as etapas.
- **ULA/ALU:** faz operações aritméticas e lógicas.

## Exemplo passo a passo: somar 10 + 15

Vamos imaginar (de forma conceitual) que o programa tem uma instrução como:

```asm
ADD R3, R1, R2
```

E que:

- `R1 = 10`
- `R2 = 15`

### 1) Busca

- O **PC** aponta para a instrução `ADD`.
- A CPU lê essa instrução na memória.
- O PC é atualizado para apontar para a próxima instrução.

### 2) Decodificação

- A CPU identifica o **opcode**: `ADD`.
- Identifica os **operandos**: destino `R3`, origens `R1` e `R2`.

### 3) Execução

- A ULA/ALU recebe os valores:
  - valor de `R1` (10)
  - valor de `R2` (15)
- A ALU faz a soma: 10 + 15 = 25.

### 4) Armazenamento (resultado)

- A CPU grava o resultado no registrador de destino:
  - `R3 = 25`

## Importante: isso se repete sempre

Um programa inteiro é uma grande sequência desse ciclo acontecendo várias vezes (milhões ou bilhões de vezes por segundo).

Na próxima página, vamos ver que **nem toda CPU tem as mesmas instruções**: isso depende da arquitetura (ISA).

