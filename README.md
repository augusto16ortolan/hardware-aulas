---
description: >-
  Visão geral do material da disciplina de Hardware e um guia rápido de como
  navegar pelos conteúdos no GitBook.
---

# Hardware - Materiais de Aula

Este repositório reúne os conteúdos da disciplina de **Hardware**, organizados em páginas Markdown compatíveis com GitBook.

O objetivo do material é te ajudar a entender, de forma progressiva e prática:

- como componentes e arquiteturas de computadores se relacionam (CPU, memória, armazenamento, I/O);
- por que existem propostas diferentes de hardware (ex.: eficiência vs desempenho);
- como escolher plataformas e tecnologias para um problema real;
- como evoluir do “conceito” para a aplicação (resumo + atividades com gabarito).

> Público-alvo: estudantes iniciantes em Hardware/Arquitetura de Computadores.

## Como navegar

- Use o menu lateral (gerado a partir do `SUMMARY.md`) para acessar os conteúdos na ordem didática.
- Cada conteúdo segue (na maioria dos casos) a mesma sequência:
  1. **Introdução** (contexto + objetivos de aprendizagem)
  2. **Páginas sequenciais** (conteúdo explicado em passos)
  3. **Resumo** (fixação do essencial)
  4. **Atividades** (questões + gabarito)

## Como estudar (sugestão rápida)

Para uma aula de ~2 horas, uma sugestão de ritmo:

- 10 min: ler a introdução e objetivos
- 60–70 min: páginas principais (fazendo pausas para dúvidas)
- 10 min: ler o resumo
- 20–30 min: responder as atividades (e conferir o gabarito)

Se estiver revisando, vá direto para **Resumo** e **Atividades**.

## Organização do repositório

- `SUMMARY.md`: controla o menu/lateral do GitBook (ordem e links).
- `conteudo-N/`: pasta de cada conteúdo (N = número do conteúdo).
- `.gitbook/assets/`: imagens e arquivos usados nas páginas.
- `prof.-augusto-ortolan.md`: página do professor e contato.

## Conteúdos

- [CONTEÚDO 1 - Processadores RISC e CISC](conteudo-1/introducao-aos-processadores-risc-e-cisc.md)
- [CONTEÚDO 2 - Instruções de máquina](conteudo-2/introducao-as-instrucoes-de-maquina.md)
- [CONTEÚDO 3 - Comparação entre Hardware de PC e Raspberry Pi](conteudo-3/introducao-comparacao-entre-hardware-de-pc-e-raspberry-pi.md)
- [CONTEÚDO 4 - Arquitetura DSP em FPGAs](conteudo-4/introducao-arquitetura-dsp-em-fpgas.md)
- [CONTEÚDO 5 - Linguagem de descrição de hardware](conteudo-5/introducao-a-linguagem-de-descricao-de-hardware.md)
- [CONTEÚDO 6 - Funções em VHDL](conteudo-6/introducao-a-funcoes-em-vhdl.md)

## Professor

- [Prof. Augusto Ortolan](prof.-augusto-ortolan.md)

## Notas e boas práticas

- O material evita depender de especificações de modelos muito recentes para não ficar desatualizado rapidamente.
- Quando aparecer “Sugestão de imagem”, é apenas uma orientação didática (não é um link externo).
- Se encontrar um erro ou quiser sugerir melhoria, a alteração normalmente envolve editar uma página `.md` e, se necessário, ajustar o `SUMMARY.md`.
