# Funções e síntese (simulação vs hardware real)

## Relembrando: simulação e síntese

- **Simulação:** você executa a descrição VHDL “virtualmente” para ver se o comportamento está certo.
- **Síntese:** uma ferramenta interpreta a lógica descrita e gera um circuito implementável (por exemplo, para FPGA).

## Uma função não vira um “bloco mágico” chamado função

Em VHDL, uma função é uma forma de **organizar a descrição**.

Na síntese:

- o sintetizador “abre” a lógica da função,
- e gera o hardware correspondente.

Exemplos conceituais:

- uma função de soma pode virar um **somador**,
- uma função de comparação pode virar um **comparador**,
- uma função com `if/else` pode virar uma **lógica de seleção** (multiplexadores).

## “Tempo zero” na simulação vs atraso físico no hardware

Na simulação, às vezes parece que a função “retorna na hora”.

No hardware real:

- o circuito gerado tem atrasos físicos (propagação),
- mesmo que o código não especifique isso diretamente.

> Em aulas iniciais, a gente costuma ignorar atrasos elétricos detalhados e focar no comportamento lógico.

## Cuidados importantes (principalmente para iniciantes)

- Nem todo código VHDL é sintetizável.
- Recursos como `report` são úteis na simulação, mas podem não ser aceitos na síntese.
- Funções devem retornar **um único valor**.
- Todas as rotas de execução devem retornar um valor.
- Use funções para deixar o código **mais claro**, não para esconder confusão.

## Boas práticas (tabela)

| Boa prática | Por quê |
|---|---|
| Usar nomes claros | Facilita leitura e intenção |
| Retornar sempre um valor | Evita comportamento indefinido/erro |
| Manter funções pequenas | Facilita manutenção e teste |
| Evitar lógica desnecessariamente complexa | Facilita entendimento e síntese |
| Reutilizar funções em `packages` quando necessário | Evita repetição no projeto |

Na próxima página, vamos aplicar funções em um caso muito comum em laboratório: **display de 7 segmentos**.

