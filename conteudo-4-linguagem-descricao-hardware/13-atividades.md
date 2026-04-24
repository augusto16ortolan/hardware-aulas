# Atividades

## Parte A — Questões discursivas (curtas)

Responda com 3 a 6 linhas.

1. Explique com suas palavras o que é uma **HDL**.
2. Por que dizemos que HDL **não é** uma linguagem de programação comum?
3. Cite dois problemas de tentar projetar circuitos grandes apenas com portas e fios em diagramas.
4. O que é **simulação** em HDL e por que ela é útil antes de implementar no hardware?
5. O que é **síntese** e como ela se relaciona com FPGA/CPLD?
6. Explique a diferença entre **FPGA**, **CPLD** e **ASIC** (visão introdutória).
7. O que é uma `entity` em VHDL? E uma `architecture`?
8. O que é uma **FSM** e dê um exemplo de sistema que pode ser modelado como FSM.

## Parte B — Múltipla escolha (5 alternativas)

Marque apenas uma alternativa (A, B, C, D ou E).

1. O objetivo principal de uma HDL é:
   - A) Criar aplicativos para celular
   - B) Controlar diretamente a CPU com instruções de máquina
   - C) Descrever e validar circuitos digitais
   - D) Substituir linguagens como Python e C
   - E) Armazenar arquivos em binário

2. Em VHDL, a `entity` representa:
   - A) A simulação do circuito
   - B) A interface (entradas e saídas) do circuito
   - C) O clock do circuito
   - D) Um arquivo de configuração da FPGA
   - E) Apenas comentários do projeto

3. Qual alternativa descreve melhor um circuito **combinacional**?
   - A) Depende do clock para funcionar
   - B) A saída depende das entradas atuais, sem memória do passado
   - C) Sempre guarda um estado anterior
   - D) Só existe em software
   - E) Só funciona com flip-flops

4. Um flip-flop D, de forma simples, serve para:
   - A) Somar dois números
   - B) Guardar 1 bit de informação
   - C) Fazer uma tabela-verdade
   - D) Programar uma CPU
   - E) Substituir portas lógicas

5. Sobre simulação e síntese, é correto dizer que:
   - A) São a mesma coisa
   - B) Simulação implementa o circuito físico diretamente
   - C) Síntese converte a descrição em hardware implementável; simulação testa o comportamento
   - D) Síntese só existe para software
   - E) Simulação só funciona em protoboard

## Parte C — Verdadeiro ou falso

Escreva **V** (verdadeiro) ou **F** (falso).

1. ( ) HDL descreve circuitos digitais (hardware).
2. ( ) Em VHDL, `architecture` define o funcionamento do circuito.
3. ( ) Circuitos combinacionais têm memória e dependem do clock.
4. ( ) FPGA e CPLD permitem implementar circuitos sem fabricar um chip do zero.
5. ( ) Todo código VHDL é automaticamente sintetizável sem nenhuma restrição.

## Parte D — Interpretação de VHDL (3 exercícios)

Considere os trechos abaixo como exemplos introdutórios.

1. Na descrição abaixo, identifique as entradas e saídas:

```vhdl
entity exemplo is
port (
    a, b : in bit;
    s    : out bit
);
end exemplo;
```

2. Em uma frase, explique o que faz a linha:

```vhdl
f <= (not c) and (h or p);
```

3. No trecho abaixo, explique o papel do `process(clk)` e o que significa “borda de subida”:

```vhdl
process(clk)
begin
    if clk'event and clk = '1' then
        q <= d;
    end if;
end process;
```

## Parte E — Comparação combinacional vs sequencial (2 exercícios)

1. Explique a diferença entre um circuito combinacional e um circuito sequencial.
2. Dê um exemplo de algo do dia a dia que “precisa lembrar do passado” (pode ser um semáforo, contador, senha, etc.) e diga por que isso lembra um circuito sequencial.

## Parte F — Entity e architecture (2 exercícios)

1. Explique, com suas palavras, a diferença entre `entity` e `architecture`.
2. Por que é útil separar “interface” e “funcionamento” ao descrever um circuito?

---

# Gabarito

## Parte A — Sugestão de respostas (resumo)

1. HDL é uma linguagem para descrever e validar circuitos digitais.
2. Porque descreve hardware/sinais/conexões; não é uma sequência de instruções para CPU.
3. Fica difícil de ler/manter/testar; muitos fios; alta chance de erro; comunicação ruim.
4. Simulação testa o comportamento do circuito antes de implementar fisicamente.
5. Síntese transforma a descrição em hardware implementável (ex.: na FPGA/CPLD).
6. FPGA é reconfigurável e mais flexível; CPLD é mais simples; ASIC é chip específico (alto custo inicial, bom em volume).
7. Entity é a interface (ports); architecture descreve o funcionamento.
8. FSM é um modelo por estados e transições; exemplo: semáforo.

## Parte B — Múltipla escolha

1. C
2. B
3. B
4. B
5. C

## Parte C — Verdadeiro ou falso

1. V
2. V
3. F
4. V
5. F

## Parte D — Interpretação

1. Entradas: `a` e `b`; saída: `s`.
2. “f vale 1 quando c=0 e (h=1 ou p=1)”.
3. O `process(clk)` reage ao clock; borda de subida é a mudança de 0 para 1; nessa borda q recebe d.

## Parte E — Comparação

1. Combinacional depende só das entradas atuais; sequencial tem memória/estado e geralmente depende de clock.
2. Ex.: semáforo precisa lembrar em qual cor está; contador lembra o valor atual.

## Parte F — Entity e architecture

1. Entity define interface; architecture define comportamento/estrutura.
2. Para organizar o projeto, reutilizar módulos e manter clareza.

