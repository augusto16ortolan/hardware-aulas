---
description: >-
  Nesta página do Conteúdo 2, você vai entender formato de instrução (campos) de
  forma progressiva, com foco no essencial para iniciantes.
---

# Formato de instrução (campos)

Uma instrução de máquina, no fundo, é um conjunto de bits. Para a CPU conseguir interpretar esses bits, a instrução é dividida em **campos**.

## O que é “formato de instrução”?

É o “desenho” que define quais pedaços da instrução significam o quê.

Campos comuns:

- **opcode**
- **registrador de destino**
- **registrador de origem**
- **valor imediato** (constante)
- **endereço de memória** (ou parte dele)
- **modo de endereçamento** (quando aplicável)

> Importante: cada ISA (x86, ARM, MIPS…) define seus próprios formatos. Aqui vamos usar exemplos didáticos simplificados.

## Exemplo 1 — Formato para operação entre registradores

Vamos usar a instrução conceitual:

```asm
ADD R3, R1, R2
```

Significado:

- `ADD` é a operação
- `R3` é o destino (onde ficará o resultado)
- `R1` e `R2` são operandos de origem

Um formato didático poderia ser:

| OPCODE | DESTINO | ORIGEM 1 | ORIGEM 2 |
|---|---|---|---|
| ADD | R3 | R1 | R2 |

### Representação binária conceitual (simplificada)

Imagine que cada campo vira bits:

```text
0001 | 0011 | 0001 | 0010
```

Onde, por exemplo:

- `0001` representa o opcode “ADD”
- `0011` representa o registrador R3
- `0001` representa R1
- `0010` representa R2

> Atenção: isso é apenas um exemplo didático. Em arquiteturas reais, o tamanho e o significado dos campos variam.

## Exemplo 2 — Instrução com valor imediato

```asm
MOV R1, 10
```

Formato didático:

| OPCODE | DESTINO | IMEDIATO |
|---|---|---|
| MOV | R1 | 10 |

## Exemplo 3 — Instrução com memória (LOAD/STORE)

```asm
LOAD R1, [1000]
```

Formato didático:

| OPCODE | DESTINO | ENDEREÇO |
|---|---|---|
| LOAD | R1 | 1000 |

## Por que isso importa?

Porque quando a CPU “vê” uma instrução na memória, ela precisa:

- separar os bits em campos,
- identificar o opcode,
- descobrir quais registradores/endereços usar,
- executar a operação corretamente.

Na próxima página, vamos ver como isso acontece no tempo: o **ciclo de instrução**.

