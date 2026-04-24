# Modos de endereçamento

Quando a CPU executa uma instrução, ela precisa saber:

> “De onde vem o dado?” e “Para onde vai o resultado?”

O **modo de endereçamento** é justamente a forma de indicar isso.

## Por que modos de endereçamento são importantes?

Porque eles deixam as instruções mais flexíveis.

Exemplos do dia a dia:

- às vezes o dado está “no próprio comando” (imediato),
- às vezes está em um endereço fixo (direto),
- às vezes o endereço está dentro de um registrador (indireto),
- às vezes você quer acessar um “vetor” com índice (indexado),
- às vezes quer saltar “um pouco para frente” no código (relativo),
- às vezes quer usar a pilha para chamadas de função (por pilha).

> Observação: os exemplos abaixo usam sintaxes inspiradas em várias arquiteturas, apenas para ilustrar o conceito.

## 1) Endereçamento imediato

O valor está dentro da instrução.

```asm
MOV AX, 10
```

Quando é útil:

- inicializar variáveis,
- somar constantes,
- configurar valores fixos.

## 2) Endereçamento direto

A instrução informa um endereço de memória diretamente.

```asm
MOV AX, [1234h]
```

Leitura conceitual:

- “Pegue o que está na memória no endereço 1234h e coloque em AX”.

Quando é útil:

- acessar uma variável em endereço conhecido (em sistemas simples),
- ler uma posição específica de memória mapeada (hardware).

## 3) Endereçamento indireto

O endereço do dado está dentro de um registrador.

```asm
MOV AX, [BX]
```

Leitura conceitual:

- “BX contém um endereço; use esse endereço para buscar o dado”.

Quando é útil:

- percorrer arrays/vetores,
- trabalhar com ponteiros,
- percorrer estruturas em memória.

## 4) Endereçamento indexado

Usa registradores + deslocamentos para calcular o endereço.

```asm
MOV AX, [BX + SI + 10]
```

Leitura conceitual:

- “Endereço = BX + SI + 10; leia a memória nesse endereço”.

Quando é útil:

- acessar elementos de matrizes/vetores,
- estruturas com campos em offsets (deslocamentos).

## 5) Endereçamento relativo

Muito usado em saltos (jumps/branches). O destino é calculado a partir de “onde eu estou agora”.

```asm
JMP SHORT +10
```

Leitura conceitual:

- “Pule 10 unidades de instrução (ou bytes) à frente”.

Quando é útil:

- `if/else`,
- laços,
- manter código mais compacto (depende da ISA).

## 6) Endereçamento por pilha

A **pilha (stack)** é uma região de memória usada como “pilha de pratos”:

- `PUSH` coloca algo no topo,
- `POP` retira do topo.

```asm
PUSH R1
POP R1
```

Quando é útil:

- salvar estados temporariamente,
- chamadas de função (guardar retorno, parâmetros),
- interrupções (em muitos sistemas).

## Ligando com RISC e CISC (leve)

- Em arquiteturas historicamente associadas a **CISC**, costuma existir uma variedade grande de modos de endereçamento.
- Em arquiteturas **RISC**, a tendência clássica é manter as instruções mais uniformes e controlar com mais clareza quando há acesso à memória.

Na próxima página, vamos ver como uma instrução pode ser dividida em **campos** (formato de instrução).

