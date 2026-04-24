# Dispositivos lógicos programáveis (PLDs)

## O que são PLDs?

**PLD** vem de *Programmable Logic Device* (Dispositivo Lógico Programável).

De forma simples: é um chip que permite **configurar a lógica digital** depois que ele já foi fabricado.

Ou seja, em vez de comprar um chip “pronto” com uma função fixa, você pode:

- definir qual lógica ele deve implementar;
- programar o dispositivo para virar aquele circuito.

## Por que surgiram os dispositivos lógicos programáveis?

Em projetos de hardware, é comum precisar:

- corrigir erros;
- testar versões diferentes do circuito;
- mudar requisitos no meio do caminho.

Se o circuito fosse sempre “fixo”, qualquer mudança exigiria refazer a fabricação do chip (caro e demorado).

PLDs surgiram para trazer mais **flexibilidade** no desenvolvimento de sistemas digitais.

## Configurar hardware por “software”

Quando falamos em “programar” um PLD, não é como escrever um programa para a CPU.

A ideia é:

- você descreve o circuito desejado;
- a ferramenta gera uma configuração;
- o chip passa a se comportar como aquele circuito.

## Circuito fixo vs circuito reconfigurável

- **Circuito fixo:** feito para uma função específica e não muda.
- **Circuito reconfigurável:** pode assumir funções diferentes ao longo do tempo (basta reprogramar).

## Por que PLDs são úteis?

PLDs são muito usados para:

- prototipagem (testar ideias rapidamente);
- automação e controle (lógica personalizada);
- integração (“glue logic”) entre componentes;
- testes e validação de circuitos digitais;
- projetos que podem evoluir ao longo do tempo.

## Analogia (para fixar)

- Um circuito fixo é como uma **ferramenta feita para uma única função** (ex.: uma chave específica).
- Um PLD é como uma **ferramenta reconfigurável**, que pode virar diferentes ferramentas conforme a necessidade.

## Conceitos importantes (tabela)

| Conceito | Explicação |
|---|---|
| PLD | Chip cuja lógica pode ser configurada após a fabricação |
| Reconfiguração | Capacidade de mudar a função do dispositivo reprogramando |
| Hardware configurável | O chip “vira” um circuito digital definido pelo projeto |
| Prototipagem | Testar e validar uma solução antes de “fechar” o design |
| Sistema digital personalizado | Circuito feito sob medida para um problema específico |

