---
description: >-
  Introdução e visão geral do Conteúdo 1, com objetivos de aprendizagem e a
  sequência do que será estudado.
---

# Processadores RISC e CISC

Nesta aula, vamos entender **duas grandes “famílias de ideias”** sobre como um processador pode ser projetado: **CISC** e **RISC**.

A intenção aqui não é decorar siglas, e sim responder perguntas bem práticas:

* Por que PCs costumam usar **x86/x86-64** (Intel/AMD)?
* Por que celulares, tablets e o **Raspberry Pi** usam tanto **ARM**?
* Por que alguns dispositivos priorizam **desempenho**, outros **bateria**, e outros **custo**?

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

## Objetivos de aprendizagem

Ao final do conteúdo, você deve ser capaz de:

* Explicar, com suas palavras, o que é um **processador (CPU)** e o que são **instruções**.
* Descrever a ideia geral de **CISC** e **RISC** (filosofia e características típicas).
* Comparar RISC e CISC em termos de **instruções, registradores, acesso à memória, hardware e eficiência**.
* Entender que **não existe “melhor” absoluto**: a escolha depende da aplicação.
* Relacionar **PC**, **Raspberry Pi** e **smartphone** com suas arquiteturas mais comuns.

## O que será estudado (sequência)

1. O que é um processador e como ele executa programas
2. Arquitetura **CISC**: ideia, vantagens, desvantagens e exemplos reais
3. Arquitetura **RISC**: ideia, vantagens, desvantagens e exemplos reais
4. Comparação direta (com tabela)
5. Exemplo prático conceitual (pseudo-assembly)
6. Comparação de dispositivos: PC × Raspberry Pi × celular
7. Resumo para fixação
8. Atividades com gabarito

## Conexão com dispositivos reais

Você já usa RISC e CISC todos os dias, mesmo sem perceber:

* **Computadores e notebooks (PCs):** em geral com processadores Intel Core / AMD Ryzen (família **x86-64**).
* **Servidores (datacenters):** muitos usam x86-64 (Intel Xeon / AMD EPYC), e alguns também usam ARM dependendo do caso.
* **Smartphones e tablets:** quase sempre **ARM**, buscando bom desempenho com baixo consumo.
* **Raspberry Pi e vários sistemas embarcados:** geralmente **ARM**, focando custo, consumo e flexibilidade.

Nas próximas páginas, vamos construir esse entendimento passo a passo.
