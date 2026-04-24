---
description: >-
  Nesta página do Conteúdo 2, você vai entender tipos de instruções (categorias)
  de forma progressiva, com foco no essencial para iniciantes.
---

# Tipos de instruções (categorias)

Uma forma fácil de estudar instruções é agrupar por **objetivo**. Aqui vamos ver as categorias mais comuns, com exemplos conceituais.

## 1) Movimentação de dados

### Objetivo

Trazer dados para registradores, copiar valores, salvar resultados e trabalhar com pilha.

### Exemplos (conceituais)

```asm
MOV R1, 10        ; R1 = 10
LOAD R2, [1000]   ; R2 = memória[1000]
STORE [2000], R2  ; memória[2000] = R2
PUSH R1           ; empilha R1
POP R3            ; desempilha para R3
```

### Situações reais onde aparece

- ler variáveis da memória,
- salvar resultados,
- passar parâmetros de função (muitas vezes usando registradores e/ou pilha),
- armazenar “retorno” de função.

## 2) Aritméticas

### Objetivo

Fazer contas (soma, subtração, multiplicação, divisão).

```asm
ADD R3, R1, R2    ; R3 = R1 + R2
SUB R4, R3, R1    ; R4 = R3 - R1
MUL R5, R1, R2    ; R5 = R1 * R2
DIV R6, R5, R2    ; R6 = R5 / R2
```

### Situações reais onde aparece

- calcular totais (preço, estoque, pontuação),
- ajustar posições em jogos (x, y),
- processar sinais e sensores (robótica/IoT).

## 3) Lógicas

### Objetivo

Operar bit a bit (muito útil para “flags”, máscaras e configurações de hardware).

```asm
AND R1, R1, R2    ; limpa bits onde R2 tem 0
OR  R3, R1, R2    ; liga bits onde R2 tem 1
XOR R4, R4, R4    ; zera R4 (método comum em alguns contextos)
NOT R5, R5        ; inverte bits de R5
```

### Situações reais onde aparece

- ligar/desligar recursos (máscaras),
- checar permissões e estados,
- configurar registradores de periféricos em sistemas embarcados.

## 4) Controle de fluxo

### Objetivo

Fazer o programa “tomar caminhos”, repetir laços e chamar funções.

```asm
CMP R1, R2        ; compara R1 e R2
JZ  iguais        ; pula se resultado foi "igual"
JMP fim           ; pula sempre

iguais:
MOV R3, 1

fim:
```

Outros exemplos comuns:

```asm
CALL funcao
RET
```

### Situações reais onde aparece

- `if/else` viram comparações + saltos condicionais,
- `for/while` viram saltos que voltam para o início do laço,
- chamadas de função viram `CALL/RET` (ou mecanismos equivalentes).

## 5) Manipulação de bits (deslocamentos e rotações)

### Objetivo

Mover bits para a esquerda/direita, o que pode:

- multiplicar/dividir por potências de 2,
- extrair campos de um número,
- preparar dados para comunicação.

Exemplos (nomes variam por arquitetura):

```asm
LSL R1, R1, 1     ; shift left (R1 << 1)
LSR R2, R2, 2     ; shift right lógico (R2 >> 2)
ASR R3, R3, 1     ; shift right aritmético (preserva sinal)
ROR R4, R4, 8     ; rotate right
```

### Situações reais onde aparece

- manipular cores em imagens (RGB em bits),
- protocolos de rede/serialização,
- controle de sensores e periféricos.

Na próxima página, vamos entender como a CPU decide “onde estão os dados” com os **modos de endereçamento**.

