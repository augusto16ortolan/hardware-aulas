# Atividades (com gabarito)

## Parte 1 — Questões discursivas curtas (8)

1. Explique com suas palavras o que é um **FPGA**.
2. Qual é a diferença entre **ASIC**, **CPLD** e **FPGA** em termos de flexibilidade?
3. O que é um **PLD** e por que ele é útil na prototipagem?
4. O que é uma **LUT** e por que ela é importante em FPGAs?
5. O que significa **DSP**?
6. Por que blocos **DSP** são úteis em FPGAs?
7. Explique a operação MAC: `resultado = resultado + (a * b)`.
8. Por que FPGAs podem ser vantajosos em aplicações de processamento de sinais?

## Parte 2 — Múltipla escolha (5 questões, 5 alternativas)

1. Qual alternativa descreve melhor a diferença entre CPU e FPGA?
   - A) FPGA executa instruções como uma CPU
   - B) CPU e FPGA são iguais, muda só o tamanho
   - C) FPGA é configurado para virar um circuito; CPU executa instruções
   - D) FPGA só serve para acender LEDs
   - E) CPU não pode fazer cálculos matemáticos

2. Qual é um exemplo típico de operação otimizada por blocos DSP?
   - A) Ler um botão
   - B) Multiplicar e acumular (MAC)
   - C) Abrir um navegador
   - D) Salvar arquivo em disco
   - E) Mostrar uma janela na tela

3. Em nível introdutório, qual dispositivo tende a ser mais indicado para lógica de controle simples e previsível?
   - A) GPU
   - B) CPLD
   - C) ASIC sempre
   - D) FPGA sempre
   - E) Nenhum

4. Qual alternativa melhor descreve LUT?
   - A) Um tipo de cabo de conexão
   - B) Uma pequena tabela de consulta que implementa função lógica
   - C) Um ventilador do FPGA
   - D) Um arquivo de texto do projeto
   - E) Um tipo de botão

5. Qual alternativa é mais alinhada com o uso de FPGA + DSP?
   - A) Processamento de vídeo em tempo real
   - B) Acender um LED com um botão
   - C) Trocar a bateria do celular
   - D) Instalar um aplicativo
   - E) Digitar um texto

## Parte 3 — Verdadeiro ou falso (5)

Marque (V) ou (F):

1. ( ) FPGAs são sempre melhores que CPUs em qualquer aplicação.
2. ( ) Blocos DSP são úteis para operações matemáticas repetitivas.
3. ( ) LUTs podem implementar funções lógicas.
4. ( ) CPLDs e FPGAs são iguais em estrutura e aplicação.
5. ( ) FPGAs podem ser usados em telecomunicações e processamento de vídeo.

## Parte 4 — Cenários práticos (5)

Em cada cenário, responda se **FPGA com DSP** faz sentido (Sim/Não/Depende) e justifique em 2–4 linhas.

1. Aplicar um filtro digital em várias amostras de áudio em tempo real.
2. Acender um LED quando um botão for pressionado.
3. Processar vídeo em tempo real para aplicar um filtro por frame.
4. Suavizar leituras de um sensor de temperatura uma vez por segundo.
5. Implementar um algoritmo com muitas multiplicações e somas em baixa latência.

## Parte 5 — Associação (3 exercícios)

### Associação 1 — Termo e definição

Associe:

- (1) PLD
- (2) ASIC
- (3) CPLD
- (4) FPGA

Com:

a) Chip fixo para uma função específica ( )  
b) Dispositivo lógico programável (hardware configurável) ( )  
c) Programável, bom para controle e projetos menores ( )  
d) Programável, alta flexibilidade e paralelismo ( )  

### Associação 2 — Componentes de FPGA

Associe:

- (1) CLB
- (2) IOB
- (3) Switch Matrix
- (4) Bloco DSP

Com:

a) Interface com pinos de entrada/saída ( )  
b) Bloco de lógica configurável ( )  
c) Conexão/roteamento entre blocos ( )  
d) Operações matemáticas (multiplicar/somar/acumular) ( )  

### Associação 3 — DSP e aplicação

Associe:

- (1) DSP
- (2) MAC
- (3) Paralelismo

Com:

a) Processamento digital de sinais ( )  
b) Multiplica e acumula ( )  
c) Várias operações ao mesmo tempo ( )  

## Parte 6 — Exercícios conceituais sobre LUT (2)

1. Uma LUT de 2 entradas possui quantas combinações possíveis de entrada? Explique em uma frase.
2. Considere a função AND. Explique como uma LUT poderia armazenar a saída dessa função para todas as combinações de `A` e `B`.

## Parte 7 — Exercícios conceituais sobre blocos DSP (2)

1. Por que implementar multiplicação usando apenas LUTs pode ser “caro” em um FPGA?
2. Em que tipo de algoritmo a operação MAC aparece com frequência? Dê um exemplo conceitual.

---

# Gabarito

## Parte 1 — Discursivas (respostas esperadas, em resumo)

1. FPGA é um dispositivo reconfigurável que pode ser programado para virar um circuito digital.
2. ASIC é fixo; CPLD/FPGA são reprogramáveis; FPGA tende a suportar mais complexidade e paralelismo.
3. PLD é hardware configurável; ajuda a testar e mudar circuitos sem fabricar chip novo.
4. LUT é uma pequena tabela de consulta (como memória) que define a saída para cada combinação de entradas.
5. DSP é Processamento Digital de Sinais.
6. Porque aceleram multiplicação/soma/acumulação e economizam LUTs.
7. Multiplica `a*b` e soma no acumulador `resultado`, repetindo isso várias vezes.
8. Porque permitem paralelismo e aceleram operações repetitivas com baixa latência.

## Parte 2 — Múltipla escolha

1. C  
2. B  
3. B  
4. B  
5. A  

## Parte 3 — V/F

1. F  
2. V  
3. V  
4. F  
5. V  

## Parte 4 — Cenários (respostas sugeridas)

1. Sim — muitas multiplicações/somas e necessidade de tempo real.
2. Não — problema simples, MCU/CPLD costuma bastar.
3. Sim — alto throughput e paralelismo.
4. Depende — pode ser simples demais; FPGA só se houver outras exigências.
5. Sim/Depende — se baixa latência e paralelismo forem necessários, faz sentido.

## Parte 5 — Associação

Associação 1: a) 2, b) 1, c) 3, d) 4  
Associação 2: a) 2, b) 1, c) 3, d) 4  
Associação 3: a) 1, b) 2, c) 3  

## Parte 6 — LUT

1. 4 combinações (2^2).  
2. A LUT guarda a saída para (0,0), (0,1), (1,0), (1,1), com 0,0,0,1.

## Parte 7 — DSP

1. Multiplicação exige muita lógica; pode consumir LUTs e reduzir desempenho.
2. Filtros digitais e algoritmos de soma de produtos (ex.: saída = soma(xi*ci)).

