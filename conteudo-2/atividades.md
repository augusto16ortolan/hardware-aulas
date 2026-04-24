---
description: >-
  Exercícios para fixar os conceitos do Conteúdo 2, com gabarito ao final para
  você conferir seu aprendizado.
---

# Atividades

## Parte A — Questões discursivas (curtas)

Responda com 3 a 6 linhas.

1. Explique a diferença entre **linguagem de alto nível**, **Assembly** e **código de máquina**.
2. Por que a CPU executa instruções representadas em **binário**?
3. O que é **opcode** e o que são **operandos**?
4. Explique, de forma simples, o que é **ISA** e por que x86 e ARM não têm exatamente as mesmas instruções.
5. O que é um **modo de endereçamento**? Para que ele serve?
6. O que é o **formato de instrução** e por que dividir em campos ajuda a CPU?
7. Liste as etapas do **ciclo de instrução** e descreva rapidamente cada uma.
8. Dê um exemplo de como um `if` (alto nível) pode virar comparação + salto (baixo nível), sem precisar usar uma sintaxe real.

## Parte B — Múltipla escolha (5 alternativas)

Marque apenas uma alternativa (A, B, C, D ou E).

1. Qual alternativa descreve melhor **código de máquina**?
   - A) Um texto legível com nomes como MOV e ADD
   - B) Um conjunto de bits/bytes que a CPU executa diretamente
   - C) Uma linguagem igual a C, mas com menos palavras
   - D) Um arquivo de texto com comentários
   - E) Um formato usado apenas em celulares

2. Em uma instrução, o **opcode** indica:
   - A) Onde o dado está na memória
   - B) O tipo de registrador usado
   - C) Qual operação deve ser executada
   - D) O nome da variável no código C
   - E) O horário em que a CPU executa

3. Qual é um exemplo de instrução (nome didático) de **controle de fluxo**?
   - A) ADD
   - B) SUB
   - C) JMP
   - D) AND
   - E) MOV

4. Qual sequência representa corretamente o ciclo básico de instrução?
   - A) Executar → Buscar → Armazenar → Decodificar
   - B) Buscar → Decodificar → Executar → Armazenar
   - C) Decodificar → Buscar → Executar → Armazenar
   - D) Buscar → Executar → Decodificar → Armazenar
   - E) Armazenar → Buscar → Decodificar → Executar

5. Sobre ISA, é mais correto afirmar que:
   - A) Todas as CPUs executam as mesmas instruções
   - B) ISA é o conjunto de instruções que uma CPU entende
   - C) ISA é um tipo de memória
   - D) ISA é um programa em Python
   - E) ISA é um cabo de dados

## Parte C — Verdadeiro ou falso

Escreva **V** (verdadeiro) ou **F** (falso).

1. ( ) Assembly é uma representação textual mais legível das instruções.
2. ( ) Código de máquina é executado diretamente pela CPU.
3. ( ) Opcode e operandos são a mesma coisa.
4. ( ) Modos de endereçamento ajudam a indicar onde estão os dados.
5. ( ) x86, ARM e MIPS são exemplos de arquiteturas com ISAs diferentes.

## Parte D — Interpretação de instruções (3 exercícios)

Considere as instruções como **conceituais**.

1. Na instrução `ADD R3, R1, R2`, o que acontece com R3?
2. Na instrução `LOAD R1, [1000]`, de onde vem o valor colocado em R1?
3. Na sequência abaixo, qual o valor final de R3?

```asm
MOV R1, 5
MOV R2, 3
ADD R3, R1, R2
```

## Parte E — Identificar opcode e operandos (2 exercícios)

1. Na instrução `ADD R1, R2`, identifique:
   - opcode:
   - operandos:

2. Na instrução `MOV AX, [1234h]`, identifique:
   - opcode:
   - operandos:
   - em uma frase, explique o que a instrução faz (conceitualmente):

## Parte F — Ciclo de instrução (2 exercícios)

1. Ordene as etapas do ciclo de instrução:
   - Execução, Busca, Armazenamento, Decodificação.

2. Em qual etapa a CPU identifica o opcode e separa os operandos?

---

# Gabarito

## Parte A — Sugestão de respostas (resumo)

1. Alto nível é para humanos; Assembly é textual e mais próximo do hardware; máquina é binário executado pela CPU.
2. Por estados elétricos/digitais; 0 e 1 representam esses estados; é o formato entendido pela CPU.
3. Opcode é a operação; operandos são registradores/valores/endereços usados pela operação.
4. ISA é o conjunto de instruções que uma CPU entende; x86 e ARM são diferentes, então não são compatíveis diretamente.
5. Forma de indicar onde está o dado; aumenta flexibilidade e permite acessar constantes, memória, ponteiros, etc.
6. Define campos (opcode, registradores, imediato…); ajuda a CPU a interpretar a instrução.
7. Buscar (pegar instrução), decodificar (entender), executar (fazer), armazenar (salvar resultado).
8. Um `if` vira comparação (CMP) e um salto condicional (JE/JNE), escolhendo caminhos do programa.

## Parte B — Múltipla escolha

1. B
2. C
3. C
4. B
5. B

## Parte C — Verdadeiro ou falso

1. V
2. V
3. F
4. V
5. V

## Parte D — Interpretação

1. R3 recebe a soma de R1 e R2.
2. Vem da memória no endereço 1000.
3. R3 = 8.

## Parte E — Opcode e operandos

1. opcode: ADD; operandos: R1, R2.
2. opcode: MOV; operandos: AX, [1234h]; “carrega para AX o valor guardado na memória em 1234h”.

## Parte F — Ciclo de instrução

1. Busca → Decodificação → Execução → Armazenamento.
2. Na decodificação.

