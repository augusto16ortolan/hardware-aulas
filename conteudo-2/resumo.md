# Resumo

## Recapitulação dos principais pontos

- A CPU executa **instruções de máquina** armazenadas na memória.
- **Código de alto nível** não é executado diretamente pela CPU: ele é traduzido (compilado/interpretado) até chegar ao nível de instruções.
- **Assembly** é uma representação textual mais legível das instruções.
- **Código de máquina** é a forma real (bits/bytes) que a CPU executa.
- Uma instrução costuma ter **opcode** (o que fazer) e **operandos** (com o quê/onde).
- Instruções podem ser agrupadas em categorias: dados, aritmética, lógica, controle de fluxo, manipulação de bits.
- **Modos de endereçamento** dizem onde estão os dados (imediato, direto, indireto, indexado, relativo, pilha).
- O **formato da instrução** divide a instrução em campos (opcode, registradores, imediato, etc.).
- O **ciclo de instrução** repete: buscar → decodificar → executar → armazenar.
- Cada arquitetura tem sua própria **ISA** (x86, ARM, MIPS), relacionada às ideias de CISC/RISC.

## Tabela resumida de conceitos

| Conceito | O que é (bem curto) |
|---|---|
| Instrução | comando básico executado pela CPU |
| Opcode | parte que indica a operação (ADD, MOV, JMP…) |
| Operando | registrador, imediato, endereço, etc. |
| Registrador | memória pequena e muito rápida dentro da CPU |
| Modo de endereçamento | como a instrução encontra o dado |
| Formato de instrução | divisão em campos (opcode, regs, imediato…) |
| Ciclo de instrução | buscar/decodificar/executar/armazenar |
| ISA | conjunto de instruções de uma arquitetura |

## Frases-chave para memorização

- “A CPU executa binário; Assembly é o ‘texto’ para humanos.”
- “Opcode diz o que fazer; operandos dizem com o quê.”
- “Nem toda CPU entende as mesmas instruções: isso depende da ISA.”
- “O ciclo buscar/decodificar/executar se repete para cada instrução.”

## Conclusão didática

Entender instruções de máquina é como entender o “alfabeto” do processador. Com isso, você começa a enxergar como `if`, `for` e expressões de alto nível viram operações básicas dentro da CPU, e por que arquiteturas diferentes (RISC/CISC) organizam esse alfabeto de formas diferentes.

Na próxima página, você vai praticar com atividades e gabarito.

