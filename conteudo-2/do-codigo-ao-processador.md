---
description: >-
  Nesta página do Conteúdo 2, você vai entender do código ao processador de
  forma progressiva, com foco no essencial para iniciantes.
---

# Do código ao processador

Nesta aula, a pergunta central é:

> “Se eu escrevo um programa em C/Java/Python, como isso vira algo que a CPU executa?”

## Três “camadas” para não confundir

### 1) Linguagem de alto nível

É a linguagem que a gente escreve para ser produtivo:

* C, C++, Java, C#, Python, JavaScript…

Ela tem conceitos como variáveis, funções, objetos, laços, bibliotecas.

### 2) Assembly

Assembly é uma linguagem **bem mais próxima** do processador. Em vez de “somar listas”, ela fala coisas como:

* mover dados (MOV/LOAD/STORE),
* somar/subtrair (ADD/SUB),
* comparar (CMP),
* desviar (JMP/BEQ…).

> Observação: cada arquitetura tem seu próprio Assembly (x86, ARM, MIPS…). Aqui vamos usar exemplos **conceituais** quando possível.

### 3) Código de máquina

É a representação **real** das instruções que a CPU executa: bytes/bits na memória.

* O Assembly é um “texto” para humanos.
* O código de máquina é “números” para a CPU.

## Por que a CPU não executa Java, C, Python ou JavaScript diretamente?

Porque a CPU entende apenas o conjunto de instruções (ISA) dela. Por exemplo:

* um processador x86-64 entende instruções da ISA x86-64;
* um processador ARM entende instruções da ISA ARM.

Java, Python e JavaScript dependem de:

* **interpretação** (executar por partes) ou
* **máquina virtual (VM)** e/ou
* **compilação JIT** (compila “na hora” partes do programa).

Já C/C++ frequentemente passa por **compilação** para gerar um executável nativo para a ISA do processador.

## Quem faz a “tradução”?

De forma bem simplificada, há três atores principais:

* **Compilador:** transforma alto nível em algo mais baixo (muitas vezes assembly ou direto em código de máquina).
* **Assembler (montador):** transforma Assembly em código de máquina.
* **Sistema operacional (SO):** carrega o programa na memória, organiza permissões e inicia a execução.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

## Exemplo didático em C

Um exemplo bem simples:

```c
int x = 5;
int y = 10;
int z = x + y;
```

Em alto nível, isso parece pequeno. Para a CPU, isso vira uma sequência de passos de “pegar valores” e “fazer contas”.

## Versão conceitual em instruções de baixo nível

Um possível “pseudo-assembly” (exemplo conceitual, não de uma arquitetura real específica) poderia ser:

```asm
LOAD 5, R1        ; R1 = 5
LOAD 10, R2       ; R2 = 10
ADD R3, R1, R2    ; R3 = R1 + R2
STORE R3, z       ; z = R3 (guardar resultado)
```

### O que está acontecendo aqui?

* `LOAD` coloca um valor em um registrador.
* `ADD` soma dois registradores e coloca em um terceiro.
* `STORE` salva o resultado em uma variável (pense como “um lugar na memória”).

## Relacionando com RISC e CISC (sem exagero)

O estilo “LOAD → operação → STORE” lembra muito o padrão típico de **RISC** (operações em registradores e acesso à memória separado).

Já em arquiteturas historicamente associadas a **CISC** (como x86), existem instruções e modos de endereçamento que podem permitir variações mais “compactas” (mas isso depende da instrução e do contexto).

> Por enquanto, guarde a ideia: o programa vira várias instruções simples. Na próxima página vamos definir o que é uma instrução de máquina.
