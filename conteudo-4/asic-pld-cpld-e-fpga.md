# ASIC, PLD, CPLD e FPGA

Antes de focar em FPGAs, vale entender como eles se comparam com outras opções.

## O que é ASIC?

**ASIC** significa *Application-Specific Integrated Circuit* (Circuito Integrado de Aplicação Específica).

Características gerais:

- feito para uma função específica;
- alto desempenho e boa eficiência energética;
- alto custo inicial (projeto e fabricação);
- pouca ou nenhuma flexibilidade depois de pronto;
- costuma valer a pena em produção em massa.

## O que é PLD?

**PLD** é o termo geral para dispositivos lógicos programáveis.

- você configura a lógica após a fabricação;
- mais flexível que um ASIC tradicional;
- ótimo para prototipagem e sistemas que podem mudar.

## O que é CPLD?

**CPLD** significa *Complex Programmable Logic Device*.

Em nível introdutório, pense assim:

- indicado para projetos menores e lógica de controle;
- costuma ter tempo de resposta mais previsível;
- normalmente menos flexível (e menor) do que um FPGA.

## O que é FPGA?

**FPGA** significa *Field Programmable Gate Array*:

- “programável em campo” (pode ser configurado fora da fábrica, pelo usuário);
- tem muitos blocos lógicos e interconexões programáveis;
- pode ter recursos especializados (memória interna e blocos DSP);
- indicado para projetos maiores, paralelos e processamento intensivo.

## Tabela comparativa (visão geral)

| Aspecto | ASIC | CPLD | FPGA |
|---|---|---|---|
| Flexibilidade | Muito baixa | Média | Alta |
| Custo inicial | Alto | Baixo/médio | Médio |
| Custo em grande volume | Baixo | Médio | Médio |
| Tempo de desenvolvimento | Alto | Baixo/médio | Médio |
| Reconfiguração | Não | Sim | Sim |
| Complexidade suportada | Muito alta (mas fixa) | Menor | Alta |
| Aplicações típicas | Produto final em massa | Controle/glue logic | DSP, aceleração, protótipos complexos |

## Ideia para guardar

- ASIC: “**fixo e otimizado**”
- CPLD: “**controle e previsibilidade**”
- FPGA: “**flexível e paralelo**”

