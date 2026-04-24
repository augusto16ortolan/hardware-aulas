# CONTEÚDO 2 - Instruções de máquina

No conteúdo anterior, você viu que a CPU executa **instruções** e que arquiteturas como **RISC** e **CISC** organizam esse “vocabulário” de maneiras diferentes.

Agora vamos dar um passo a mais e entender o que, de fato, chega até o processador:

- como um programa sai de uma linguagem como C/Java/Python e vira algo que a CPU consegue executar;
- o que é **Assembly** e o que é **código de máquina**;
- como uma instrução é representada (normalmente em **binário**);
- como a CPU **busca, decodifica e executa** instruções.

> Sugestão de imagem: uma seta em etapas “Alto nível → (compilador/VM) → Assembly → (assembler) → Código de máquina → CPU”.

## Objetivos de aprendizagem

Ao final deste conteúdo, você deve conseguir:

- Explicar a diferença entre **linguagem de alto nível**, **Assembly** e **código de máquina**.
- Descrever o que é uma **instrução de máquina** e por que ela é representada em **binário**.
- Identificar **opcode** e **operandos** em exemplos simples.
- Reconhecer categorias de instruções (movimentação, aritmética, lógica, controle de fluxo).
- Explicar, de forma simples, **modos de endereçamento** e por que eles existem.
- Entender o **formato** de uma instrução (campos) e o **ciclo de instrução**.
- Perceber que cada arquitetura (x86, ARM, MIPS) tem sua própria **ISA** (conjunto de instruções).

## O que será estudado (sequência)

1. Do código ao processador: do alto nível até a CPU
2. O que são instruções de máquina
3. Opcode e operandos
4. Tipos de instruções (categorias)
5. Modos de endereçamento (onde estão os dados?)
6. Formato de instrução (campos)
7. Ciclo de instrução (buscar → decodificar → executar → armazenar)
8. Instruções em arquiteturas diferentes (x86, ARM, MIPS)
9. Exemplos práticos em “assembly conceitual”
10. Resumo
11. Atividades com gabarito

## Alto nível, Assembly, código de máquina e CPU (visão inicial)

- **Linguagem de alto nível** (C, Java, Python, JavaScript): feita para humanos, com comandos mais “ricos”.
- **Assembly**: uma forma textual de representar instruções (mais próxima do hardware), mas ainda legível.
- **Código de máquina**: o que a CPU executa de verdade; normalmente é uma sequência de **bits** (0 e 1) na memória.

> Importante: a CPU não “entende” diretamente `if`, `for`, classes, funções de biblioteca. Tudo isso precisa virar instruções básicas.

