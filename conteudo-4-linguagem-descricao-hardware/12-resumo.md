# Resumo

## Recapitulação dos principais pontos

- **HDL** é uma linguagem para **descrever hardware** (circuitos digitais), não uma programação “passo a passo” para CPU.
- HDLs ajudam a **projetar**, **documentar**, **simular** e, em muitos casos, **sintetizar/implementar** circuitos.
- **VHDL** é uma HDL muito usada, com estrutura clássica: `entity` (interface) + `architecture` (comportamento/estrutura).
- **Ports** são entradas/saídas; **signals** são “fios” internos.
- **Circuito combinacional:** saída depende só das entradas atuais.
- **Circuito sequencial:** possui memória/estado e normalmente usa **clock**.
- **Flip-flop D** guarda 1 bit e atualiza na borda do clock (ex.: borda de subida).
- **FSM** organiza controle em estados e transições.
- **FPGA** e **CPLD** permitem implementar circuitos sem fabricar chip do zero; **ASIC** é um chip específico para grande escala.
- **Simulação** testa o comportamento; **síntese** transforma a descrição em hardware implementável.

## Tabela resumida de conceitos

| Conceito | O que é (bem curto) |
|---|---|
| HDL | linguagem para descrever circuitos digitais |
| VHDL | uma HDL popular |
| `entity` | interface (entradas/saídas) |
| `architecture` | descrição do funcionamento |
| `port` | entradas e saídas do circuito |
| `signal` | conexões internas (“fios”) |
| `bit` | 0 ou 1 |
| `bit_vector` | conjunto de bits |
| Combinacional | saída depende das entradas atuais |
| Sequencial | saída depende de entradas e estado anterior |
| Flip-flop | elemento de memória (guarda bit) |
| Clock | sinal que marca o ritmo do sequencial |
| FSM | controle por estados e transições |
| FPGA | circuito programável em campo |
| CPLD | programável mais simples |
| ASIC | chip específico para uma aplicação |

## Frases-chave para memorização

- “HDL descreve hardware; não é um programa rodando em CPU.”
- “Entity é a interface; architecture é o funcionamento.”
- “Combinacional não tem memória; sequencial tem estado e clock.”
- “Simular é testar; sintetizar é implementar.”

## Conclusão didática

HDLs existem porque circuitos digitais reais ficam grandes e complexos rapidamente. Com VHDL (ou outra HDL), você pode descrever o circuito de forma clara, testar por simulação e, se for o caso, implementar em FPGA/CPLD. Esse é um passo importante para entender como hardware é projetado “no mundo real”.

Na próxima página, você vai praticar com atividades e gabarito.

