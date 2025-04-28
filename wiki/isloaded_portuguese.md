<!--
Meta Description: # is.loaded: Verificando se um Pacote em R Está Carregado ## Sinopse A função `is.loaded` em R é utilizada para verificar se um determinado símbolo ou...
Meta Keywords: função, símbolo, que, loaded, pacote
-->

# is.loaded: Verificando se um Pacote em R Está Carregado

## Sinopse
A função `is.loaded` em R é utilizada para verificar se um determinado símbolo ou pacote está carregado na sessão atual. Esta função é especialmente útil para desenvolvedores e usuários que precisam gerenciar a memória e o ambiente de trabalho.

## Documentação
### Propósito
A função `is.loaded` tem como objetivo verificar a presença de um símbolo (ou função) em um pacote que já foi carregado. Isso pode ajudar a evitar erros em scripts, garantindo que as funções necessárias estejam disponíveis.

### Uso
A sintaxe básica da função é a seguinte:

```R
is.loaded(symbol)
```

#### Parâmetros
- `symbol`: Um objeto do tipo `character` que representa o nome do símbolo (ou função) que se deseja verificar.

### Detalhes
- A função retorna um valor booleano: `TRUE` se o símbolo estiver carregado e `FALSE` caso contrário.
- É importante notar que `is.loaded` verifica apenas se o símbolo foi carregado, não se o pacote que contém o símbolo está carregado. Para verificar se um pacote está carregado, pode-se usar a função `isNamespaceLoaded`.

## Exemplos
### Exemplo 1: Verificando um símbolo específico
```R
# Verifica se a função 'lm' (linear model) está carregada
is.loaded("lm")
```

### Exemplo 2: Verificando um símbolo que não está carregado
```R
# Verifica se a função 'non_existent_function' está carregada
is.loaded("non_existent_function")  # Retornará FALSE
```

### Exemplo 3: Usando em um pacote específico
```R
library(stats)  # Carrega o pacote stats
# Verifica se a função 'lm' está carregada após carregar o pacote
is.loaded("lm")  # Retornará TRUE
```

## Explicação
É comum que usuários iniciantes confundam a função `is.loaded` com a verificação de pacotes. A função apenas verifica a presença de um símbolo, não garantindo que o pacote que contém esse símbolo esteja ativo. Além disso, a função não deve ser utilizada para verificar objetos criados pelo usuário, pois sua aplicação é restrita a símbolos de pacotes.

## Resumo em Uma Linha
A função `is.loaded` em R é utilizada para verificar se um símbolo específico está carregado na sessão atual, retornando um valor booleano.