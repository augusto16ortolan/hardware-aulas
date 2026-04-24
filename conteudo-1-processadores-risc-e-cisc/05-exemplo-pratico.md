# Exemplo prático (conceitual)

Nesta página, vamos usar um **pseudo-assembly** (exemplo conceitual) para comparar a ideia de “uma instrução faz bastante coisa” versus “quebrar em passos menores”.

> Importante: os comandos abaixo são **didáticos**. Eles não representam exatamente o assembly real de uma arquitetura específica.

## Cenário: multiplicar dois valores guardados na memória

Imagine dois valores guardados em duas posições de memória:

- `2:4` (endereço conceitual) contém o valor **A**
- `4:1` (endereço conceitual) contém o valor **B**

Queremos calcular `A × B` e guardar o resultado de volta.

## Versão “CISC” (uma instrução mais complexa)

Exemplo conceitual:

```asm
MULT 2:4, 4:1
```

Como ler essa ideia:

- “Pegue o valor que está em `2:4`”
- “Pegue o valor que está em `4:1`”
- “Multiplique”
- “Guarde o resultado em algum lugar (depende da definição da instrução)”

Como isso pode acontecer por dentro (explicação conceitual):

1. Ler o valor da memória em `2:4`
2. Ler o valor da memória em `4:1`
3. Multiplicar
4. Escrever o resultado (em registrador ou memória, conforme a regra)

O ponto aqui é a **ideia**: uma instrução “só” representa um trabalho maior.

## Versão “RISC” (quebrando em passos simples)

Agora vamos separar em etapas usando registradores:

```asm
LOAD A, 2:4
LOAD B, 4:1
MULT A, B
STORE 2:4, A
```

### Explicação linha por linha

1) `LOAD A, 2:4`  
Carrega o valor da memória no endereço `2:4` para o registrador `A`.

2) `LOAD B, 4:1`  
Carrega o valor da memória no endereço `4:1` para o registrador `B`.

3) `MULT A, B`  
Multiplica o conteúdo de `A` pelo conteúdo de `B`.  
Aqui estamos assumindo que o resultado fica em `A` (convenção do exemplo).

4) `STORE 2:4, A`  
Guarda o valor do registrador `A` na memória no endereço `2:4`.

## O que esse exemplo quer ensinar?

- Em **RISC**, costuma ser comum o padrão: **LOAD → operação entre registradores → STORE**.
- Em **CISC**, a arquitetura pode permitir instruções que “misturam” acesso à memória e operação.

Mas lembre:

- No mundo real, **x86 e ARM modernos** são cheios de otimizações internas.
- Às vezes, uma instrução “CISC” é convertida internamente em várias operações menores.

Na próxima página, vamos relacionar isso com dispositivos reais.

