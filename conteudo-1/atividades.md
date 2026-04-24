---
description: >-
  Exercícios para fixar os conceitos do Conteúdo 1, com gabarito ao final para
  você conferir seu aprendizado.
---

# Atividades

## Parte A — Questões discursivas (curtas)

Responda com 3 a 6 linhas cada.

1. O que é a CPU e qual é o papel dela em um computador?
2. Explique o que é uma **instrução** e dê dois exemplos de tipos de instruções (ex.: somar, carregar da memória, comparar, desviar).
3. O que são **registradores** e por que eles são importantes para o desempenho?
4. Descreva (de forma simples) o ciclo **buscar → decodificar → executar**.
5. O que significa **CISC** e qual é a ideia geral por trás dessa arquitetura?
6. O que significa **RISC** e qual é a ideia geral por trás dessa arquitetura?
7. Explique o que é o padrão **LOAD/STORE** e por que ele é comum em RISC.
8. Por que não é correto afirmar que “RISC é sempre melhor” ou que “CISC é sempre melhor”?

## Parte B — Múltipla escolha (5 alternativas)

Marque apenas uma alternativa (A, B, C, D ou E).

1. Qual alternativa descreve melhor a ideia de CISC (de forma introdutória)?
   - A) Conjunto reduzido e uniforme de instruções
   - B) Instruções sempre de tamanho fixo
   - C) Conjunto amplo, com instruções mais variadas e algumas mais complexas
   - D) Só permite operações entre registradores
   - E) Não possui modos de endereçamento diferentes

2. Em muitas arquiteturas RISC, qual padrão é comum para acessar memória?
   - A) Todas as instruções acessam memória diretamente
   - B) LOAD e STORE para memória; operações normalmente entre registradores
   - C) Apenas STORE existe, LOAD não
   - D) Apenas LOAD existe, STORE não
   - E) Memória não é usada, só registradores

3. Um exemplo típico de arquitetura muito comum em PCs e notebooks (em geral) é:
   - A) ARM
   - B) MIPS
   - C) x86/x86-64
   - D) SPARC
   - E) Power ISA

4. Qual frase está mais correta sobre processadores modernos?
   - A) Um processador CISC nunca usa pipeline
   - B) Um processador RISC nunca tem hardware complexo
   - C) Processadores atuais podem combinar técnicas e ter otimizações internas complexas
   - D) RISC sempre gera programas menores
   - E) CISC sempre consome menos energia

5. Sobre “código mais longo vs. instruções mais complexas”, é correto dizer que:
   - A) RISC sempre usa menos instruções para a mesma tarefa
   - B) CISC sempre usa menos energia por instrução
   - C) RISC pode usar mais instruções, mas cada instrução tende a ser mais simples
   - D) CISC não pode acessar memória
   - E) RISC não usa registradores

## Parte C — Verdadeiro ou falso

Escreva **V** (verdadeiro) ou **F** (falso).

1. ( ) CISC significa “Complex Instruction Set Computer”.
2. ( ) Em RISC, é comum separar acesso à memória (LOAD/STORE) das operações (ADD/MULT).
3. ( ) Quanto mais complexa a instrução, menor a chance do hardware ser complexo.
4. ( ) x86/x86-64 é um exemplo clássico associado a CISC.
5. ( ) A escolha entre RISC e CISC depende do tipo de dispositivo e do objetivo do projeto.

## Parte D — Cenários práticos (escolha e justifique)

Em cada cenário, diga se você escolheria uma solução mais próxima de **RISC** ou de **CISC**, e justifique em 5 a 8 linhas.

1. Você vai projetar um dispositivo de automação residencial alimentado por bateria, que precisa ficar ligado por muito tempo e executar tarefas simples (sensores e comunicação).
2. Você vai montar um laboratório de informática com PCs para rodar programas antigos e atuais, com compatibilidade máxima para vários softwares.
3. Você vai criar um robô educacional de baixo custo que precisa rodar Linux leve e controlar motores e sensores.

---

# Gabarito

## Parte A — Sugestão de respostas (resumo)

1. CPU executa instruções e coordena operações; é o “centro de execução”.
2. Instrução é um comando básico; exemplos: ADD, LOAD, STORE, CMP, JMP (conceituais).
3. Registradores são memórias internas muito rápidas; reduzem acesso à RAM e aceleram execução.
4. Buscar instrução na memória, decodificar o que fazer, executar e (se necessário) escrever resultado.
5. CISC: conjunto amplo de instruções, com formatos variados e algumas instruções complexas.
6. RISC: conjunto mais reduzido e uniforme; instruções simples; foco em pipeline e previsibilidade.
7. LOAD/STORE: memória é acessada via instruções específicas; operações geralmente entre registradores.
8. Porque o melhor depende do objetivo (consumo, compatibilidade, custo, desempenho) e de otimizações internas modernas.

## Parte B — Múltipla escolha

1. C
2. B
3. C
4. C
5. C

## Parte C — Verdadeiro ou falso

1. V
2. V
3. F
4. V
5. V

## Parte D — Cenários práticos (respostas esperadas)

1. Mais próximo de RISC (eficiência energética, tarefas simples, bateria).
2. Mais próximo de CISC (compatibilidade com ecossistema x86 em PCs).
3. Mais próximo de RISC (baixo custo/consumo, uso comum de ARM em placas e robótica educacional).

