# Aplicações de HDL

HDLs aparecem em diversos contextos onde precisamos projetar e validar circuitos digitais.

## Onde HDLs são usadas?

- **Dispositivos lógicos programáveis** (FPGA e CPLD)
- **ASICs** (chips feitos sob medida)
- **Simulação de circuitos** (para validar antes de implementar)
- **Prototipagem de hardware**
- **Ensino** (eletrônica digital, arquitetura de computadores)

## Tabela de aplicações

| Aplicação | O que é | Exemplo de uso |
|---|---|---|
| FPGA | Circuito programável em campo (reconfigurável) | Criar um controlador, um processador simples, interfaces de comunicação |
| CPLD | Dispositivo lógico programável mais simples | “Cola lógica” entre componentes, decodificadores, controle simples |
| ASIC | Chip específico para uma aplicação | Chip de criptografia, acelerador de IA, circuitos de alto volume |
| Simulação | Testar comportamento sem hardware físico | Conferir tabela-verdade, temporização lógica e fluxos de controle |

## Observações importantes (bem introdutórias)

- **FPGA e CPLD** permitem testar e implementar circuitos sem fabricar um chip do zero.
- **ASIC** costuma ser usado quando se deseja fabricar um circuito específico em larga escala (alto custo inicial, custo baixo por unidade em volume).
- **Simulação** ajuda a encontrar erros cedo: é melhor corrigir no código do que depois de montar o hardware.

Na próxima página, vamos começar a ver VHDL: a estrutura básica.

