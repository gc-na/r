<!--
Meta Description: # Função is.nan em R: Verificando Valores NaN ## Sinopse A função `is.nan` em R é utilizada para identificar valores "Not a Number" (NaN) em vetores e...
Meta Keywords: nan, valores, que, função, false
-->

# Função is.nan em R: Verificando Valores NaN

## Sinopse
A função `is.nan` em R é utilizada para identificar valores "Not a Number" (NaN) em vetores e matrizes, sendo essencial para a manipulação e limpeza de dados.

## Documentação
A função `is.nan` pertence ao ambiente básico do R e tem como propósito principal verificar se os elementos de um vetor ou matriz são NaN. Os valores NaN surgem frequentemente em operações aritméticas inválidas, como a divisão de zero por zero.

### Uso
```R
is.nan(x)
```

#### Parâmetros
- `x`: Um vetor numérico ou matriz que será testado para a presença de valores NaN.

#### Valor Retornado
A função retorna um vetor lógico do mesmo comprimento que `x`, onde cada elemento é `TRUE` se o correspondente em `x` for NaN e `FALSE` caso contrário.

### Detalhes
- NaN é um conceito importante em computação numérica, representando um valor indefinido ou não representável.
- A função `is.nan` é especialmente útil em análises de dados, onde a presença de NaNs pode afetar resultados estatísticos ou gráficos.
- Diferentemente de `NA`, que indica valores ausentes, NaN refere-se especificamente a números que não são válidos.

## Exemplos

### Exemplo 1: Identificando NaN em um vetor
```R
vetor <- c(1, 2, NaN, 4)
resultado <- is.nan(vetor)
print(resultado)
# [1] FALSE FALSE  TRUE FALSE
```

### Exemplo 2: Identificando NaN em uma matriz
```R
matriz <- matrix(c(1, 2, NaN, 4, 5, 6), nrow = 2)
resultado <- is.nan(matriz)
print(resultado)
#      [,1]  [,2]
# [1,] FALSE FALSE
# [2,]  TRUE FALSE
```

### Exemplo 3: Trabalhando com operações que geram NaN
```R
resultado <- 0 / 0
print(is.nan(resultado))
# [1] TRUE
```

## Explicação
Um erro comum ao utilizar a função `is.nan` é confundi-la com `is.na`, que verifica a presença de valores ausentes (`NA`). Enquanto `is.nan` detecta apenas valores NaN, `is.na` cobre ambos NaN e NA. Outro ponto importante é que NaN é considerado um número em R, portanto, funções que esperam um valor numérico podem não se comportar como esperado se NaNs estiverem presentes.

## Resumo em uma linha
A função `is.nan` em R é utilizada para verificar a presença de valores "Not a Number" em vetores e matrizes, facilitando a manipulação de dados numéricos.