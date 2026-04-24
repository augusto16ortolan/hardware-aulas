# PC, Raspberry Pi e dispositivos móveis

Até aqui, falamos de ideias. Agora vamos conectar com o mundo real: por que cada tipo de dispositivo costuma usar uma arquitetura?

## 1) PC tradicional (x86/x86-64)

### Objetivos comuns

- Rodar uma enorme variedade de programas (legado e atual)
- Alto desempenho em tarefas diversas (jogos, criação, multitarefa)
- Facilidade de expansão (placa de vídeo, mais RAM, armazenamento, periféricos)

### O que costuma aparecer

- Arquitetura: **x86-64** (CISC “clássico”)
- Processadores: Intel Core / AMD Ryzen (usuário), Intel Xeon / AMD EPYC (servidor)

### Observação importante

O desempenho do PC não vem “só” de ser x86. Vem de:

- caches grandes e bem projetados,
- altas frequências,
- muitos núcleos,
- técnicas como execução fora de ordem,
- GPUs muito potentes (especialmente em jogos).

## 2) Raspberry Pi (geralmente ARM)

O Raspberry Pi é uma placa famosa para aprender, prototipar e criar projetos.

### Objetivos comuns

- Baixo consumo de energia
- Custo relativamente acessível
- Integração de muitos recursos no mesmo chip (SoC)
- Boa plataforma para educação e projetos

### O que costuma aparecer

- Arquitetura: **ARM** (RISC muito popular)
- Tipo de chip: muitas vezes um **SoC (System-on-a-Chip)**, que integra CPU, GPU, controladores e interfaces.

### Onde ele brilha

- Programação, Linux, redes simples
- Automação e IoT
- Robótica educacional
- Servidores leves (dependendo do uso)

## 3) Smartphones (quase sempre ARM)

No celular, a prioridade número 1 é: **bateria + desempenho “suficiente” + tamanho/temperatura**.

### Objetivos comuns

- Desempenho por watt (bom desempenho gastando pouca energia)
- Muitos recursos integrados (CPU, GPU, modem, IA, ISP da câmera, etc.)
- Controle térmico (não pode esquentar demais na mão do usuário)

### O que costuma aparecer

- Arquitetura: **ARM**
- Modelo: SoC altamente integrado (Qualcomm, MediaTek, Samsung, Apple, etc.)

## Comparando objetivos de projeto (por que são diferentes?)

Um **PC gamer**, um **smartphone** e um **Raspberry Pi** têm metas diferentes:

- **PC gamer:** máximo desempenho e expansão (energia da tomada, ventilação grande).
- **Smartphone:** desempenho por watt e integração (bateria, espaço mínimo, aquecimento limitado).
- **Raspberry Pi:** custo/consumo/educação/prototipagem (equilíbrio entre capacidade e simplicidade).

## Um cuidado: arquitetura (ISA) não é tudo

É comum confundir:

- **ISA (arquitetura do conjunto de instruções):** x86-64, ARM, etc.
- **Microarquitetura:** como o chip é construído por dentro (pipeline, cache, núcleos, etc.)

Dois processadores podem ser **ARM**, mas terem desempenhos muito diferentes por causa da microarquitetura, cache, frequência, número de núcleos e fabricação.

Na próxima página, vamos fechar com um resumo para fixação.

