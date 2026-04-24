# Instruções em arquiteturas diferentes (x86, ARM, MIPS)

## Cada arquitetura tem sua própria ISA

**ISA (Instruction Set Architecture)** é o conjunto de instruções que uma CPU entende.

Isso significa que:

- um código compilado para **x86-64** não roda diretamente em **ARM**;
- um código compilado para **ARM** não roda diretamente em **MIPS**;

…a menos que exista alguma forma de tradução/compatibilidade (emuladores, camadas de tradução, VMs, etc.).

## Relacionando com RISC e CISC (do conteúdo anterior)

- **x86** é historicamente associado a **CISC** (muitas instruções e formatos variados).
- **ARM** e **MIPS** são exemplos clássicos associados a **RISC** (instruções mais uniformes, forte uso de registradores).

> Lembrete: processadores modernos são cheios de otimizações internas; aqui o foco é a ideia introdutória da ISA e exemplos de nomes de instruções.

## Exemplos de nomes de instruções por arquitetura (visão geral)

### x86 (associada historicamente a CISC)

Exemplos comuns de nomes:

- `MOV`, `ADD`, `SUB`, `PUSH`, `POP`, `JMP`, `CALL`, `RET`

### ARM (RISC muito usada em móveis/embarcados)

Exemplos comuns de nomes:

- `MOV`, `LDR` (load), `STR` (store), `ADD`, `SUB`, `B` (branch), `BEQ`, `BNE`

### MIPS (RISC muito usada como referência didática)

Exemplos comuns de nomes:

- `LW` (load word), `SW` (store word), `ADD`, `SUB`, `J` (jump), `BEQ`, `BNE`

## Tabela comparativa (exemplos)

| Objetivo | x86 (ex.) | ARM (ex.) | MIPS (ex.) | Observação |
|---|---|---|---|---|
| Mover dado/constante | `MOV` | `MOV` | (varia; pode usar `ADD` com zero em exemplos didáticos) | nomes variam |
| Carregar da memória | (depende da forma) | `LDR` | `LW` | “load” |
| Salvar na memória | (depende da forma) | `STR` | `SW` | “store” |
| Somar | `ADD` | `ADD` | `ADD` | comum |
| Comparar | `CMP` | `CMP` | (geralmente faz comparação via instruções/branches) | depende da ISA |
| Desvio | `JMP` | `B` | `J` | “jump/branch” |
| Desvio condicional | (varia) | `BEQ`, `BNE` | `BEQ`, `BNE` | “branch if …” |

> Atenção: esta tabela serve para você reconhecer padrões de nomes. Não é uma lista completa nem uma regra rígida.

Na próxima página, vamos fazer dois exemplos completos em **assembly conceitual**, com explicação linha a linha.

