<!--
Meta Description: # is.single: Verificando se um Objeto é um Único Valor em R ## Sinopse O comando `is.single` em R é usado para verificar se um objeto contém exatament...
Meta Keywords: single, único, valor, que, função
-->

# is.single: Verificando se um Objeto é um Único Valor em R

## Sinopse
O comando `is.single` em R é usado para verificar se um objeto contém exatamente um único valor, seja ele numérico, lógico ou de outro tipo. Essa função é útil em diversas situações, especialmente ao validar entradas em funções que exigem um único argumento.

## Documentação
### Propósito
A função `is.single` tem como objetivo determinar se um objeto R é um único valor. Esta verificação é particularmente importante em contextos onde um único valor é esperado, como em operações aritméticas ou funções que não aceitam vetores.

### Uso
A sintaxe básica da função é:
```R
is.single(x)
```
onde `x` é o objeto que você deseja verificar.

### Detalhes
- **Tipo de Retorno**: A função retorna um valor lógico (`TRUE` ou `FALSE`).
- **Comportamento**: `is.single` retorna `TRUE` se `x` for um único valor e `FALSE` caso contrário. Um único valor é definido como uma entrada que não é um vetor ou lista com mais de um elemento.

## Exemplos
Aqui estão alguns exemplos de uso da função `is.single`:

```R
# Verificando um número único
is.single(5) # TRUE

# Verificando um vetor de números
is.single(c(1, 2, 3)) # FALSE

# Verificando uma string única
is.single("Olá") # TRUE

# Verificando um vetor de strings
is.single(c("Olá", "Mundo")) # FALSE

# Verificando um valor lógico
is.single(TRUE) # TRUE

# Verificando um vetor lógico
is.single(c(TRUE, FALSE)) # FALSE
```

## Explicação
Embora a função `is.single` seja bastante direta, alguns pontos devem ser considerados:

- **Estruturas de Dados**: É importante lembrar que listas ou vetores com mais de um elemento não serão considerados "únicos", mesmo que todos os elementos sejam do mesmo tipo.
- **Uso Prático**: Ao escrever funções personalizadas, `is.single` pode ser uma boa prática para validar argumentos, garantindo que os usuários forneçam exatamente o que a função espera.
- **Diferença de Outras Funções**: `is.single` não deve ser confundido com funções como `length` ou `is.atomic`, que têm propósitos diferentes.

## Resumo em Uma Linha
A função `is.single` em R verifica se um objeto contém exatamente um único valor, retornando `TRUE` ou `FALSE`.