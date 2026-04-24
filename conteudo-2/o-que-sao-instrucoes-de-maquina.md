---
description: >-
  Nesta página do Conteúdo 2, você vai entender o que são instruções de máquina?
  de forma progressiva, com foco no essencial para iniciantes.
---

# O que são instruções de máquina?

## Definição simples

**Instrução de máquina** é um comando no formato que a CPU consegue **executar diretamente**.

Ela diz, por exemplo:

* “some dois valores”
* “carregue um dado da memória”
* “compare”
* “pule para outro ponto do programa”

## Por que as instruções são representadas em binário?

Dentro do computador, tudo é representado por estados elétricos (em geral, “nível alto” e “nível baixo”).

O binário (0 e 1) é uma forma prática de representar esses estados.

Então, uma instrução de máquina costuma ser um conjunto de bits, por exemplo (representação conceitual):

```
0101 0010 0001 1110
```

> Importante: o binário real depende da arquitetura (ISA) e do formato da instrução.

## O que é “uma instrução” para a CPU?

Pense que a CPU funciona como uma linha de montagem:

1. busca a próxima instrução na memória,
2. entende qual operação é (decodifica),
3. executa usando registradores e a ULA/ALU,
4. salva o resultado (em registrador e/ou memória).

Isso acontece repetidamente, para cada instrução do programa.

## Instrução vs. linha de código de alto nível

Uma linha de alto nível pode virar **várias** instruções.

Exemplo em alto nível:

```c
z = x + y;
```

Isso pode envolver etapas como:

* carregar `x` de algum lugar para um registrador,
* carregar `y` para outro registrador,
* somar,
* guardar em `z`.

Ou seja: a CPU não vê “`z = x + y;`”. Ela vê uma sequência de instruções menores.

## Onde as instruções ficam guardadas?

As instruções do programa ficam na **memória (RAM)**, assim como os dados.

Para a CPU, a memória é como uma rua com casas numeradas (endereços):

* cada endereço aponta para uma parte do programa ou para um dado.

## Memória, registradores e unidade de controle (visão bem básica)

* **Memória:** guarda instruções e dados.
* **Registradores:** guardam valores que a CPU usa rapidamente.
* **Unidade de controle:** coordena o “ritmo” do processador (o que fazer em cada etapa do ciclo).
* **ULA/ALU:** faz operações aritméticas e lógicas (somar, subtrair, AND, OR…).

<figure><img src="../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

Na próxima página, vamos ver como uma instrução costuma ser “montada”: **opcode + operandos**.
