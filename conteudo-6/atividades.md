# Atividades

## Parte A — Questões discursivas (curtas)

Responda com 3 a 6 linhas.

1. Explique com suas palavras o que é uma função em VHDL.
2. Qual é a principal vantagem de usar funções em um projeto VHDL?
3. Por que funções em VHDL retornam apenas um único valor?
4. Qual a diferença entre comandos concorrentes e comandos sequenciais em VHDL?
5. Explique a diferença entre `signal` e `variable` (visão básica).
6. Em uma função com `if/else`, por que todos os caminhos devem retornar um valor?
7. Explique a diferença entre declarar uma função dentro da `architecture` e dentro de um `package`.
8. Por que uma função pode ser útil em uma conversão “número → display de 7 segmentos”?

## Parte B — Múltipla escolha (5 alternativas)

Marque apenas uma alternativa (A, B, C, D ou E).

1. Uma função em VHDL:
   - A) Executa várias saídas ao mesmo tempo
   - B) Retorna um único valor de um tipo declarado
   - C) Só pode ser usada em circuitos sequenciais
   - D) Só funciona em simulação e nunca em síntese
   - E) Substitui a `entity`

2. Onde é comum declarar uma função para uso local (apenas naquele circuito)?
   - A) Sempre dentro de `entity`
   - B) No preâmbulo da `architecture` (antes do `begin`)
   - C) No `port map`
   - D) Somente dentro de `process(clk)`
   - E) Somente em comentários

3. O que `return` faz dentro de uma função?
   - A) Atualiza um sinal imediatamente
   - B) Define o clock do circuito
   - C) Devolve o valor final da função
   - D) Declara uma variável
   - E) Instancia um componente

4. Em VHDL, o código dentro de uma função é:
   - A) Sempre concorrente
   - B) Sempre sequencial
   - C) Sempre executado pela CPU
   - D) Sempre sintetizado em um bloco pronto
   - E) Sempre proibido de usar `if`

5. Sobre funções e síntese:
   - A) Uma função vira necessariamente um “chip função”
   - B) O sintetizador interpreta a lógica e gera hardware equivalente
   - C) Toda função com `report` é sempre sintetizável
   - D) Funções só existem em linguagens de programação, não em HDL
   - E) Síntese e simulação são a mesma coisa

## Parte C — Verdadeiro ou falso

Escreva **V** (verdadeiro) ou **F** (falso).

1. ( ) Funções em VHDL recebem parâmetros e retornam um único valor.
2. ( ) É possível usar uma função em uma atribuição concorrente como `saida <= funcao(x);`.
3. ( ) O corpo de uma função em VHDL é escrito com comandos concorrentes.
4. ( ) Em funções com `if/else`, todo caminho deve retornar um valor.
5. ( ) Colocar funções em `packages` pode ajudar na reutilização do projeto.

## Parte D — Interpretação de funções (3 exercícios)

1. Na função abaixo, identifique o nome, os parâmetros e o tipo de retorno:

```vhdl
function soma (a : integer; b : integer) return integer is
begin
    return a + b;
end function;
```

2. O que será retornado por `soma(5, 3)`?

3. Na função abaixo, o que ela retorna quando `valor = -2`? E quando `valor = 15`?

```vhdl
function limita_0_9 (valor : integer) return integer is
begin
    if valor < 0 then
        return 0;
    elsif valor > 9 then
        return 9;
    else
        return valor;
    end if;
end function;
```

## Parte E — Identificar parâmetros e retorno (2 exercícios)

1. Na função abaixo, quais são os parâmetros e qual é o tipo de retorno?

```vhdl
function eh_zero (valor : integer) return boolean is
begin
    if valor = 0 then
        return true;
    else
        return false;
    end if;
end function;
```

2. Por que é importante o tipo de retorno ser compatível com o valor do `return`?

## Parte F — Completar funções simples (2 exercícios)

1. Complete a função para retornar o dobro de um número:

```vhdl
function dobro (valor : integer) return integer is
begin
    -- completar aqui
end function;
```

2. Complete a função para retornar o maior entre `a` e `b`:

```vhdl
function maior (a : integer; b : integer) return integer is
begin
    -- completar aqui
end function;
```

## Parte G — Exercício prático: display de 7 segmentos (1 exercício)

1. Explique por que a conversão “número → padrão do display” é um bom caso para usar função em VHDL.

---

# Gabarito

## Parte A — Sugestão de respostas (resumo)

1. Função recebe parâmetros, executa lógica sequencial e retorna um valor.
2. Reutilização/legibilidade/evitar repetição.
3. Porque o objetivo da função é produzir um resultado único que pode ser usado em expressões.
4. Concorrente descreve relações em paralelo; sequencial executa em ordem dentro de blocos (`process`, `function`).
5. `signal` representa conexão de hardware; `variable` é temporária em blocos sequenciais.
6. Para não ficar sem valor de retorno (indefinido/erro).
7. `architecture` é local; `package` é reutilizável em vários arquivos.
8. Porque é uma lógica de mapeamento que se repete e fica mais legível encapsulada.

## Parte B — Múltipla escolha

1. B
2. B
3. C
4. B
5. B

## Parte C — Verdadeiro ou falso

1. V
2. V
3. F
4. V
5. V

## Parte D — Interpretação

1. Nome: `soma`; parâmetros: `a`, `b` (integer); retorno: `integer`.
2. 8.
3. Para -2 retorna 0; para 15 retorna 9.

## Parte E — Identificar

1. Parâmetro: `valor : integer`; retorno: `boolean`.
2. Para garantir que a função devolve um valor válido do tipo prometido.

## Parte F — Completar

1.

```vhdl
function dobro (valor : integer) return integer is
begin
    return valor * 2;
end function;
```

2.

```vhdl
function maior (a : integer; b : integer) return integer is
begin
    if a > b then
        return a;
    else
        return b;
    end if;
end function;
```

## Parte G — Display

Porque é uma conversão repetida, que retorna um único vetor, e fica mais legível com um nome como `converte_display`.

