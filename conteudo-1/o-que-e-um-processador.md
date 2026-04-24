# O que é um processador?

Antes de falar em RISC e CISC, precisamos entender **o que um processador faz**.

## CPU: o “executador” do computador

A **CPU (Central Processing Unit)** é a parte do computador que **executa instruções**. Ela não “pensa” sozinha: ela segue passos bem definidos, em altíssima velocidade.

Uma forma simples de imaginar:

- **Programa** = uma receita
- **Instrução** = um passo da receita (“some”, “compare”, “carregue um valor”, “salve um valor”)
- **CPU** = o cozinheiro que segue os passos
- **Memória (RAM)** = a bancada onde ficam os ingredientes acessíveis rapidamente
- **Armazenamento (SSD/HD)** = a despensa (muito maior, mas mais lenta)

> Sugestão de imagem: diagrama simples com CPU ↔ memória RAM ↔ armazenamento.

## O que são instruções?

Uma **instrução** é um comando básico que o processador entende e executa. Exemplos conceituais (não são comandos reais de uma arquitetura específica):

```asm
ADD R1, R2, R3    ; R1 = R2 + R3
LOAD R1, [END]    ; R1 = memória[END]
STORE [END], R1   ; memória[END] = R1
CMP R1, R2        ; compara R1 e R2 (para decisões)
JMP LABEL         ; desvia para um ponto do programa
```

Perceba que a CPU trabalha com coisas bem “pequenas”: somar, mover dados, comparar, desviar.

## Do “código” até a CPU (visão bem simplificada)

Quando você escreve um programa em uma linguagem de alto nível (como Python, Java, C#):

1. O código passa por um **compilador** (gera um executável) ou por um **interpretador/VM** (executa em etapas).
2. No fim, o que a CPU executa são instruções do **conjunto de instruções** daquela arquitetura (ex.: x86-64, ARM).
3. O sistema operacional carrega o programa para a memória e a CPU começa a executar.

> Importante: linguagens diferentes podem chegar a instruções diferentes, mas **a CPU sempre executa instruções** no final.

## Registradores: a “memória super rápida” dentro da CPU

**Registradores** são espaços de armazenamento **muito pequenos e muito rápidos** dentro do processador.

- A CPU gosta de trabalhar com registradores porque é rápido.
- A memória RAM é maior, mas costuma ser mais lenta para acesso do que registradores.

Uma analogia:

- **Registradores** = post-its na mão do cozinheiro (ele consulta muito rápido)
- **RAM** = a bancada (ainda é rápida, mas não tanto quanto o “na mão”)
- **SSD/HD** = a despensa (mais lenta)

## O ciclo de instrução (buscar → entender → executar)

De forma introdutória, a CPU repete continuamente um ciclo:

1. **Buscar (fetch):** pega a próxima instrução na memória.
2. **Decodificar (decode):** entende qual operação é e quais dados precisa.
3. **Executar (execute):** realiza a operação (somar, comparar, carregar, etc.).
4. (Muitas vezes) **Escrever de volta (write-back):** salva o resultado em registrador ou memória.

Isso acontece bilhões de vezes por segundo.

## Memória e endereços (o “mapa” onde os dados ficam)

A memória pode ser vista como uma grande lista de “caixinhas”, cada uma com um **endereço**.

- **Endereço** = “posição” na memória
- A CPU lê e escreve valores usando esses endereços

Em muitas arquiteturas, a CPU não faz tudo “direto” na memória o tempo todo. Em várias situações ela:

1. carrega da memória para registradores,
2. processa nos registradores,
3. salva de volta na memória.

Esse ponto vai ser essencial para entender **RISC**.

## Fechando a ideia

Se você guardar só isto:

- **CPU executa instruções**
- **registradores são o lugar mais rápido para trabalhar**
- **memória guarda programas e dados**
- **o ciclo fetch/decode/execute se repete sem parar**

…você já tem a base para diferenciar **CISC** e **RISC**.

