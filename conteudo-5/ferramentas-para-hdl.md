# Ferramentas para HDL

Para trabalhar com HDL, normalmente usamos ferramentas que ajudam em etapas diferentes.

## Tipos de ferramentas

### Simuladores

Um simulador executa “virtualmente” o circuito descrito para ver se ele se comporta como esperado.

Exemplos:

- ModelSim
- GHDL (muito usado com VHDL)

### Sintetizadores

Síntese é o processo de transformar a descrição em uma estrutura de hardware implementável (por exemplo, portas/blocos internos de uma FPGA).

Ferramentas famosas:

- Intel Quartus (Quartus II / Quartus Prime)
- Xilinx/AMD Vivado

### Ambientes de desenvolvimento

Além das ferramentas principais, você usa editores/IDEs para escrever o código e organizar o projeto.

## Fluxo básico (do código ao hardware)

1. **Escrever a descrição HDL** (VHDL/Verilog).
2. **Simular o comportamento** (ver se a lógica está correta).
3. **Sintetizar** (transformar a descrição em hardware).
4. **Implementar** em FPGA/CPLD ou preparar para ASIC.
5. **Testar no hardware** (ver o circuito funcionando no mundo real).

## Simulação vs. síntese (explicação simples)

- **Simulação:** “vamos ver se o circuito se comporta como eu espero” (um teste virtual).
- **Síntese:** “vamos transformar isso em um circuito implementável” (hardware real).

Nem tudo que funciona em simulação é necessariamente sintetizável. Por isso:

- em aulas introdutórias, a simulação é ótima para aprender;
- e a síntese/implementação é o passo seguinte quando você vai para FPGA/CPLD.

## Observação educacional

No contexto educacional, ferramentas como **Quartus** podem ser usadas para:

- escrever VHDL,
- simular (dependendo do fluxo),
- sintetizar e programar uma FPGA/CPLD de laboratório,
- testar com LEDs, botões, displays e sensores simples.

Na próxima página, vamos fechar o conteúdo com um resumo para fixação.

