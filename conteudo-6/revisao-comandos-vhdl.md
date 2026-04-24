---
description: >-
  Nesta página do Conteúdo 6, você vai entender revisão: comandos em vhdl
  (concorrentes e sequenciais) de forma progressiva, com foco no essencial para
  iniciantes.
---

# Revisão: comandos em VHDL (concorrentes e sequenciais)

Antes de entrar em funções, vale uma revisão rápida para não confundir VHDL com uma linguagem de programação tradicional.

## VHDL descreve hardware

Em hardware, várias partes trabalham “ao mesmo tempo”:

- entradas mudam,
- sinais internos mudam,
- saídas mudam,
- e (em circuitos sequenciais) o estado muda no clock.

Em VHDL, isso aparece como dois tipos de escrita muito comuns:

- **comandos concorrentes** (parecem “em paralelo”),
- **comandos sequenciais** (executados em ordem dentro de um bloco).

## Comandos concorrentes

### O que são?

São descrições que representam ações que ocorrem “simultaneamente” no hardware.

### Onde aparecem?

Normalmente **no corpo da `architecture`**, depois do `begin`.

### Exemplo (atribuição concorrente)

```vhdl
Sinal_B <= Sinal_A and Sinal_C;
```

Como ler:

- “Sinal_B é sempre o AND de Sinal_A e Sinal_C”.

Não é “linha 1, depois linha 2”. É uma relação contínua entre sinais.

## Comandos sequenciais

### O que são?

São comandos que rodam em ordem **dentro de blocos** como:

- `process`
- funções (`function`)
- procedimentos (`procedure`)

### Onde aparecem?

Dentro de `process` (muito comum), e também dentro de funções.

### Exemplo (processo com `if`)

```vhdl
process(Sinal_A)
begin
    if Sinal_A = '1' then
        Sinal_B <= '0';
    else
        Sinal_B <= '1';
    end if;
end process;
```

Mesmo parecendo “sequencial”, o resultado final ainda descreve hardware:

- quando `Sinal_A` muda, o processo é reavaliado e `Sinal_B` recebe o valor correspondente.

## Tabela-resumo

| Tipo de comando | Onde aparece | Como se comporta | Exemplo |
|---|---|---|---|
| Concorrente | `architecture` (após `begin`) | Em paralelo (relação contínua entre sinais) | `B <= A and C;` |
| Sequencial | dentro de `process`, `function`, `procedure` | Em ordem dentro do bloco | `if ... then ... else ... end if;` |

## Onde entram as funções nisso?

Funções são **blocos sequenciais** que você usa dentro de expressões e atribuições.

Você vai declarar a função (normalmente antes do `begin`) e depois “chamar” a função para obter um valor.

Na próxima página, vamos definir exatamente o que é uma função em VHDL.

