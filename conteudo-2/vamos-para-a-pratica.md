---
description: >-
  Atividade prática guiada do Conteúdo 2 para aplicar os conceitos de forma
  objetiva e consolidar o aprendizado.
---

# Exemplo prático com Assembly (conceitual)

Nesta página, vamos usar exemplos de “assembly conceitual” para praticar leitura.

> Importante: os exemplos abaixo são didáticos e não garantem ser executáveis em uma arquitetura real específica.

## Exemplo 1 — Somar dois valores

Objetivo: somar 10 e 15 e guardar em `resultado`.

```asm
; Somar dois valores
MOV R1, 10
MOV R2, 15
ADD R3, R1, R2
STORE R3, resultado
```

### Explicação linha por linha

- `MOV R1, 10` coloca 10 no registrador R1.
- `MOV R2, 15` coloca 15 no registrador R2.
- `ADD R3, R1, R2` soma R1 e R2 e guarda o resultado em R3.
- `STORE R3, resultado` salva o valor de R3 em `resultado` (pense como uma posição na memória).

## Exemplo 2 — Desvio condicional (comparar e decidir)

Objetivo: se dois valores forem iguais, colocar `1` em `resultado`.

```asm
MOV R1, 10
MOV R2, 10
CMP R1, R2
JE valores_iguais
JMP fim

valores_iguais:
MOV R3, 1

fim:
STORE R3, resultado
```

### Explicação linha por linha

- `MOV R1, 10` e `MOV R2, 10`: colocam valores nos registradores.
- `CMP R1, R2`: compara os valores (conceitualmente, isso ajusta “flags” internas).
- `JE valores_iguais`: “Jump if Equal” (pule para `valores_iguais` se a comparação indicar igualdade).
- `JMP fim`: se não forem iguais, pula direto para o fim.
- `valores_iguais:` é um rótulo (label), um “nome” para um ponto do código.
- `MOV R3, 1`: se forem iguais, define R3 como 1.
- `fim:` outro rótulo.
- `STORE R3, resultado`: salva o valor final em `resultado`.

### O que são “flags” (explicação bem simples)?

Muitos processadores têm indicadores internos (flags) para guardar o resultado de uma comparação:

- “foi igual?”
- “foi maior?”
- “deu zero?”
- “deu negativo?”

Saltos condicionais (como `JE`) consultam essas flags para decidir o caminho do programa.

Na próxima página, vamos fechar com um resumo e uma tabela de conceitos.

