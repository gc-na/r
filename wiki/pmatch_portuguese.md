<!--
Meta Description: # pmatch: Correspondência Parcial de Strings em R ## Sinopse O comando `pmatch` em R é utilizado para realizar correspondência parcial de strings, per...
Meta Keywords: pmatch, que, correspondência, padrões, vetor
-->

# pmatch: Correspondência Parcial de Strings em R

## Sinopse
O comando `pmatch` em R é utilizado para realizar correspondência parcial de strings, permitindo que usuários encontrem elementos em um vetor que correspondam a padrões fornecidos.

## Documentação
### Propósito
O `pmatch` serve para identificar a posição de correspondências parciais entre um vetor de strings e um padrão especificado. É especialmente útil em situações onde você deseja localizar elementos que não correspondem exatamente, mas que contêm partes relevantes do texto.

### Uso
A função `pmatch` tem a seguinte sintaxe:

```R
pmatch(x, table, nomatch = NA_integer_, duplicates.ok = FALSE, ...)
```

#### Argumentos
- **x**: Um vetor de caracteres que contém as strings a serem correspondidas.
- **table**: Um vetor de caracteres que contém os padrões a serem buscados.
- **nomatch**: Um valor a ser retornado quando não há correspondência (padrão é `NA_integer_`).
- **duplicates.ok**: Um valor lógico que indica se duplicatas são permitidas. Se `FALSE`, uma correspondência deve ser única.

### Detalhes
O resultado da função é um vetor de inteiros que indica a posição em `table` correspondente a cada elemento de `x`. Se não houver correspondência, será retornado o valor definido em `nomatch`. O `pmatch` é sensível a maiúsculas e minúsculas, ou seja, "Exemplo" e "exemplo" são considerados diferentes.

## Exemplos
Aqui estão alguns exemplos de como usar o `pmatch`:

```R
# Definindo um vetor de padrões
padrões <- c("maçã", "banana", "laranja")

# Correspondência parcial
resultados <- pmatch(c("ma", "ban"), padrões)
print(resultados)  # Saída: 1 2

# Testando com um padrão não correspondente
resultados_não_encontrados <- pmatch(c("pera", "ma"), padrões)
print(resultados_não_encontrados)  # Saída: NA 1
```

## Explicação
Um erro comum ao usar `pmatch` é não considerar as diferenças de maiúsculas e minúsculas, que podem levar a resultados inesperados. Além disso, se houver múltiplas correspondências possíveis e `duplicates.ok` for definido como `FALSE`, a função retornará `NA` para aqueles elementos. Portanto, é sempre bom verificar seus dados e padrões antes de realizar a correspondência.

## Resumo em Uma Linha
O `pmatch` em R permite realizar correspondência parcial de strings, retornando a posição dos padrões correspondentes em um vetor.