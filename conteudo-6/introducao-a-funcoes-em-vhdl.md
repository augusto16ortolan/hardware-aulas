---
description: >-
  Introdução e visão geral do Conteúdo 6, com objetivos de aprendizagem e a
  sequência do que será estudado.
---

# Funções em VHDL

No conteúdo anterior, você viu que VHDL é uma **linguagem de descrição de hardware**: a ideia é descrever circuitos (sinais, entradas, saídas e comportamento), e não escrever um “programa” para rodar em uma CPU.

Agora vamos aprender um recurso muito útil para escrever VHDL com mais organização:

> **Funções**: pequenos “blocos de cálculo” que recebem valores, processam uma lógica e **retornam um único valor**.

Funções ajudam a:

* evitar repetição de lógica,
* melhorar a legibilidade,
* facilitar manutenção,
* organizar projetos maiores.

## Objetivos de aprendizagem

Ao final do conteúdo, você deve conseguir:

* Compreender o que é uma **função** em VHDL.
* Identificar a **sintaxe** básica de declaração de função.
* Entender **parâmetros** e **tipo de retorno**.
* Criar funções simples (soma, comparação, decisões).
* Usar funções dentro de **architectures**.
* Entender quando usar uma função e quando não usar.
* Compreender a diferença entre **comandos concorrentes**, **comandos sequenciais** e **funções**.
* Interpretar funções aplicadas a exemplos práticos (soma, comparação de vetores e conversão para display de 7 segmentos).

<figure><img src="../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

## O que será estudado (sequência)

1. Revisão: concorrente vs sequencial em VHDL
2. O que são funções em VHDL
3. Sintaxe básica de funções
4. Função declarada dentro da `architecture`
5. Parâmetros, retorno e variáveis locais
6. Funções com condicionais
7. Funções com vetores (`bit_vector`/`std_logic_vector`)
8. Funções em `packages` (reutilização)
9. Funções e síntese (simulação vs hardware real)
10. Exemplo prático: display de 7 segmentos
11. Exemplo prático: cronômetro simples
12. Resumo
13. Atividades com gabarito

## Por que funções são importantes em VHDL?

Em VHDL você muitas vezes escreve expressões e regras que se repetem:

* uma mesma verificação (ex.: “é zero?”),
* uma conversão (ex.: “número → display”),
* uma comparação de vetores,
* uma seleção de valores.

Sem função, você pode acabar copiando e colando trechos. Com função, você cria uma “ferramenta” com nome claro e usa em vários pontos.

## O que é uma função (em uma frase)?

> Em VHDL, uma função recebe zero ou mais parâmetros, executa uma lógica interna (sequencial) e retorna **um único valor**.
