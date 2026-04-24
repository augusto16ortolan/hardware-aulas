---
description: >-
  Nesta página do Conteúdo 6, você vai entender funções em `packages`
  (reutilização) de forma progressiva, com foco no essencial para iniciantes.
---

# Funções em `packages` (reutilização)

## O que é um `package` em VHDL?

Um `package` é como uma “caixa de ferramentas”:

- você declara coisas reutilizáveis (tipos, constantes, funções, procedimentos),
- e depois importa essas coisas em outros arquivos.

Isso ajuda a organizar projetos e evitar repetição.

## Por que declarar funções em `packages`?

Porque você pode:

- usar a mesma função em várias `architectures`,
- compartilhar funções entre projetos,
- manter o código mais limpo e modular.

## Função na `architecture` vs função no `package`

- **Função dentro da `architecture`:** boa quando é específica daquele circuito.
- **Função em `package`:** boa quando você quer reutilizar em vários circuitos/projetos.

## Exemplo de `package` com a função `equal`

### Declaração (interface do package)

```vhdl
package minhas_funcoes is
    function equal(a, b : bit_vector) return boolean;
end minhas_funcoes;
```

### Implementação (`package body`)

```vhdl
package body minhas_funcoes is

    function equal(a, b : bit_vector) return boolean is
    begin
        if a'length = b'length then
            for idx in 0 to a'length - 1 loop
                if a(idx) /= b(idx) then
                    return false;
                end if;
            end loop;

            return true;
        else
            report "Tamanhos diferentes." severity note;
            return false;
        end if;
    end function;

end minhas_funcoes;
```

## Como usar em outro arquivo

Você pode importar o que precisa com `use`.

Exemplos comuns:

```vhdl
library work;
use work.minhas_funcoes.equal;
```

Ou importar tudo do package:

```vhdl
library work;
use work.minhas_funcoes.all;
```

Explicação:

- o `package` declara a função disponível,
- o `package body` implementa a função,
- o `use` permite chamar a função em outro arquivo.

Na próxima página, vamos falar sobre simulação e síntese: o que acontece com funções quando o objetivo é gerar hardware real.

