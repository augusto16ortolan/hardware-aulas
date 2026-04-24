---
description: >-
  Nesta página do Conteúdo 3, você vai entender consumo de energia e aquecimento
  de forma progressiva, com foco no essencial para iniciantes.
---

# Consumo de energia e aquecimento

Uma diferença bem prática entre um PC e um Raspberry Pi é o quanto cada um consome de energia e como isso afeta aquecimento e refrigeração.

## Por que PCs consomem mais energia?

Em geral, um PC pode consumir mais energia porque:

- usa componentes focados em **alto desempenho**;
- pode ter GPU dedicada, vários discos e muitos periféricos;
- precisa manter desempenho estável em tarefas pesadas.

Por isso, PCs costumam precisar de:

- **fontes** mais potentes;
- **coolers** e dissipadores maiores;
- boa ventilação (especialmente em desktops).

## Por que o Raspberry Pi costuma ser mais eficiente?

O Raspberry Pi costuma ser mais eficiente energeticamente porque:

- usa processadores (geralmente ARM) com foco em **baixo consumo**;
- tem menos componentes e é pensado para operar com energia limitada.

Mesmo assim, ele pode aquecer dependendo de:

- carga de trabalho (uso intenso);
- ambiente;
- modelo;
- falta de dissipação (sem dissipador/ventoinha quando necessário).

## Desempenho, energia e calor (regra simples)

- Mais desempenho geralmente exige **mais energia**.
- Mais energia consumida normalmente gera **mais calor**.
- Mais calor exige melhor **resfriamento**.

## Exemplos (para comparar)

- **PC para renderização de vídeo:** tarefa pesada por bastante tempo → maior consumo e maior aquecimento → precisa de bom resfriamento.
- **Raspberry Pi para monitorar temperatura e acionar um ventilador:** tarefa leve e contínua (24/7) → baixo consumo → ideal para ficar ligado o tempo todo.

## Comparação (tabela)

| Critério | PC | Raspberry Pi |
|---|---|---|
| Consumo típico | Geralmente maior | Geralmente menor |
| Aquecimento | Pode ser alto em cargas pesadas | Pode aquecer, mas tende a ser menor |
| Refrigeração | Coolers/dissipadores robustos | Pode usar dissipador/ventoinha dependendo do uso |
| Uso 24/7 | Possível, mas pode gastar mais | Muito comum em projetos de baixo consumo |

