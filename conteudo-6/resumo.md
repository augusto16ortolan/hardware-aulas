# Resumo

## Recapitulação dos principais pontos

- Funções em VHDL encapsulam uma lógica e retornam **um único valor**.
- Uma função pode melhorar legibilidade e evitar repetição de código.
- O código dentro de uma função é **sequencial**.
- Toda função precisa retornar um valor compatível com seu tipo de retorno.
- Uma função não é, necessariamente, um componente físico pronto: na síntese, o sintetizador gera o hardware correspondente à lógica descrita.
- Funções podem ser declaradas:
  - dentro da `architecture` (útil quando é específica do circuito),
  - ou em `packages` (útil para reutilização).

## Tabela resumida de conceitos

| Conceito | O que é (bem curto) |
|---|---|
| Função | bloco de lógica que retorna um valor |
| Parâmetro | valor que a função recebe |
| Tipo de retorno | tipo do valor devolvido |
| `return` | devolve o resultado da função |
| Variável local | usada dentro da função para cálculos |
| `signal` | sinal/conexão de hardware |
| `package` | “caixa de ferramentas” reutilizável |
| `package body` | implementação do package |
| Função na `architecture` | útil quando é específica |
| Função no `package` | útil quando será reutilizada |
| Simulação | testar comportamento |
| Síntese | gerar hardware implementável |
| `std_logic_vector` | vetor usado com `std_logic` (comum em FPGA) |
| `bit_vector` | vetor de `bit` (didático) |
| `'length` | tamanho do vetor |

## Frases-chave para memorização

- “Funções em VHDL retornam um único valor.”
- “Uma função melhora a legibilidade e evita repetição.”
- “O corpo da função é sequencial.”
- “Toda rota precisa retornar um valor.”
- “O sintetizador gera hardware a partir da lógica descrita.”
- “Use funções pequenas, claras e com nomes significativos.”

Na próxima página, você vai praticar com atividades e gabarito.

