---
description: >-
  Nesta página do Conteúdo 2, você vai entender opcode e operandos de forma
  progressiva, com foco no essencial para iniciantes.
---

# Opcode e operandos

Uma instrução, em geral, pode ser vista como:

> **OPERAÇÃO + DADOS (ou referências a dados)**

## O que é opcode?

**Opcode** (operation code) é o “código da operação”. Ele diz o que a CPU deve fazer:

- somar, mover, comparar, pular…

Exemplos de nomes que usamos para facilitar:

- `ADD`, `SUB`, `MOV`, `LOAD`, `STORE`, `JMP`, `CMP`…

> Em máquinas reais, o opcode costuma ser um número (binário/hex). Usar nomes é só para estudo.

## O que são operandos?

**Operandos** são as “informações” usadas pela operação. Eles dizem com o que a CPU vai trabalhar:

- registradores (R1, R2),
- valores imediatos (10),
- endereços de memória ([1234h]),
- posições relativas (pular +10),
- etc.

## Estrutura geral de uma instrução (conceitual)

Exemplos conceituais:

```asm
ADD R1, R2
MOV AX, 10h
LOAD R1, 1000
STORE R1, 2000
```

Como ler:

- opcode: `ADD`, `MOV`, `LOAD`, `STORE`
- operandos: `R1`, `R2`, `AX`, `10h`, `1000`, `2000`

## Tabela de exemplos

| Instrução | Opcode | Operandos | Significado (conceitual) |
|---|---|---|---|
| `ADD R1, R2` | ADD | R1, R2 | soma R2 em R1 |
| `MOV AX, 10h` | MOV | AX, 10h | coloca 10h em AX |
| `LOAD R1, 1000` | LOAD | R1, 1000 | carrega de memória[1000] para R1 |
| `STORE R1, 2000` | STORE | R1, 2000 | salva R1 em memória[2000] |

> Atenção: a sintaxe real e os significados exatos variam por arquitetura. Aqui é didático.

## Exemplos de opcodes comuns (nomes didáticos)

Movimentação de dados:

- `MOV`, `LOAD`, `STORE`, `PUSH`, `POP`

Aritméticas:

- `ADD`, `SUB`, `MUL`, `DIV`

Lógicas:

- `AND`, `OR`, `XOR`, `NOT`

Controle de fluxo:

- `JMP`, `CMP` (comparação), saltos condicionais (ex.: `JZ`, `JNZ`), `CALL`, `RET`

Na próxima página, vamos organizar esses opcodes por **categorias** e ver usos práticos.

