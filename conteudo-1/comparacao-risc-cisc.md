# Comparação RISC e CISC

Agora que você já viu as ideias gerais, vamos comparar de forma direta.

## Visão rápida (tabela comparativa)

| Aspecto | CISC (típico) | RISC (típico) |
|---|---|---|
| Conjunto de instruções | Maior e mais variado | Menor e mais uniforme |
| Tamanho das instruções | Variável | Geralmente fixo |
| Operações na memória | Pode haver instruções que operam direto na memória | Memória via LOAD/STORE |
| Uso de registradores | Importante, mas não é a “única via” | Muito intenso |
| Decodificação | Mais complexa | Mais simples e previsível |
| Pipeline | Mais desafiador em alguns pontos | Geralmente mais previsível |
| Densidade de código | Frequentemente melhor (código menor) | Pode ser menor ou maior (depende) |
| Eficiência energética | Depende da implementação | Muito associada a projetos eficientes |

> Lembrete: “típico” não significa “sempre”. Processadores modernos usam várias técnicas internas.

## Instruções simples vs. instruções complexas

Uma forma de pensar:

- **CISC:** tenta oferecer instruções que fazem “mais coisa de uma vez”.
- **RISC:** prefere quebrar o trabalho em instruções menores e repetíveis.

Na prática, o compilador (ou o programador em assembly) decide como montar o programa com as peças disponíveis.

## Registradores vs. acesso à memória

Outro ponto-chave:

- **RISC:** tende a dizer “faça contas nos registradores” e “use LOAD/STORE para memória”.
- **CISC:** pode permitir mais combinações envolvendo memória em uma única instrução.

Por que isso importa?

- A memória é bem mais lenta que registradores.
- Prever acesso à memória (cache, latência) é uma parte crítica do desempenho.

## Simplicidade de hardware vs. complexidade de hardware

Em termos de filosofia:

- **RISC** tenta facilitar o hardware em algumas áreas (instruções mais uniformes).
- **CISC** pode aumentar a complexidade de decodificação e controle (muitos formatos).

Mas existe um “porém” importante:

- muitos processadores atuais (tanto x86 quanto ARM) têm **otimizações internas** bem complexas (pipelines profundos, execução fora de ordem, cache sofisticado, previsão de desvios, etc.).

Ou seja: a “simplicidade” e “complexidade” são relativas, e o mundo real é cheio de misturas.

## Código mais longo vs. instruções mais complexas

Uma discussão comum:

- **RISC pode usar mais instruções** para fazer a mesma tarefa.
- **CISC pode usar menos instruções** (mais “potentes”).

Isso leva a efeitos práticos:

- **tamanho do programa na memória** (código menor pode caber melhor em cache),
- **trabalho de decodificação** (instruções variáveis podem custar mais para “entender”),
- **eficiência do pipeline**.

## Não existe “melhor em todos os casos”

A frase mais importante do conteúdo:

> Não existe arquitetura melhor em todos os cenários. A melhor escolha depende da aplicação.

Exemplos:

- Para um **PC com milhões de programas legados**, compatibilidade é essencial → x86-64 faz muito sentido.
- Para um **celular com bateria**, eficiência e integração contam muito → ARM costuma ser excelente.
- Para um **sistema embarcado simples**, custo e consumo podem ser prioridade → RISC é comum.

Na próxima página, vamos ver um exemplo prático conceitual para fixar.

