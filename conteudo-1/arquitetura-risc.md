---
description: >-
  Nesta página do Conteúdo 1, você vai entender arquitetura risc de forma
  progressiva, com foco no essencial para iniciantes.
---

# Arquitetura RISC

## O que significa RISC?

**RISC** vem de **Reduced Instruction Set Computer** (Computador com Conjunto Reduzido de Instruções).

A ideia principal (bem resumida) é:

- ter **menos tipos de instruções**,
- deixar as instruções mais **simples e previsíveis**,
- facilitar execução rápida em **pipeline**,
- e muitas vezes melhorar **eficiência energética**.

## Filosofia RISC (a ideia por trás)

Em vez de “uma instrução fazer muita coisa”, a estratégia é:

- cada instrução faz **um passo pequeno e bem definido**,
- o programa pode usar **mais instruções**, mas cada uma é simples,
- o hardware pode ficar mais direto, e o pipeline pode funcionar melhor.

## Características típicas de RISC

> Atenção: são características comuns “clássicas”. Processadores modernos podem misturar técnicas.

### 1) Conjunto reduzido de instruções (mais uniformes)

Há menos instruções diferentes e, em geral, elas seguem formatos mais padronizados.

### 2) Instruções simples e geralmente de tamanho fixo

Muitas arquiteturas RISC usam tamanho fixo (por exemplo, todas as instruções com o mesmo número de bits).

Isso costuma facilitar:

- buscar a próxima instrução,
- decodificar rapidamente,
- organizar pipeline de forma previsível.

### 3) Uso intenso de registradores

Como a CPU quer trabalhar “dentro dela” o máximo possível, o uso de registradores costuma ser bem forte.

### 4) Modelo LOAD/STORE (operações com memória são separadas)

Uma ideia muito comum em RISC é:

- **LOAD**: trazer da memória para registrador
- **STORE**: levar do registrador para memória
- operações como **ADD/MULT/CMP** geralmente trabalham **entre registradores**

Isso dá mais previsibilidade (a CPU sabe quando vai acessar memória).

### 5) Pipeline e previsibilidade

“Pipeline” é como uma linha de montagem:

- enquanto uma instrução está sendo executada,
- outra pode estar sendo decodificada,
- outra pode estar sendo buscada, etc.

Instruções simples e uniformes ajudam a linha de montagem a ficar eficiente.

### 6) Eficiência energética (muito relevante hoje)

Em celulares e dispositivos com bateria, gastar menos energia é essencial.

RISC é muito associado a esse tipo de projeto (embora eficiência dependa de vários fatores, não só da arquitetura).

## Exemplos reais

Alguns exemplos bem conhecidos:

- **ARM** (muito comum em smartphones, tablets, Raspberry Pi e sistemas embarcados)
- **MIPS** (histórico em ensino e sistemas embarcados)
- **SPARC** e **Power ISA** (importantes em diversos sistemas)
- **Apple Silicon (M-series):** usa ISA baseada em **ARM** (foco em desempenho por watt)

## Vantagens (em nível introdutório)

- **Boa eficiência e previsibilidade** para pipeline.
- **Hardware potencialmente mais simples** em certos aspectos.
- **Muito adequado para baixo consumo** (móveis/IoT/embarcados).

## Desvantagens (em nível introdutório)

- **Código pode ficar maior** (mais instruções) dependendo do caso.
- **Desempenho não é “garantido”** só por ser RISC: depende de cache, frequência, pipeline, paralelismo, etc.
- **Compatibilidade/ecossistema**: varia muito conforme a plataforma (hoje ARM tem um ecossistema enorme, mas historicamente x86 dominou PCs).

## Onde RISC é muito usado na prática?

- **Smartphones e tablets**
- **Raspberry Pi e placas educacionais**
- **IoT (Internet das Coisas)**
- **Robótica e automação**
- **Sistemas embarcados** (carros, eletrodomésticos, equipamentos industriais)

Na próxima página, vamos comparar RISC e CISC lado a lado.

