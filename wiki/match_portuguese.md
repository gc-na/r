<!--
Meta Description: # match: Comando para Correspondência de Valores em R ## Sinopse O comando `match` em R é utilizado para identificar as posições de elementos de um ve...
Meta Keywords: match, vetor, que, elementos, função
-->

# match: Comando para Correspondência de Valores em R

## Sinopse
O comando `match` em R é utilizado para identificar as posições de elementos de um vetor em outro vetor, facilitando a pesquisa e a correspondência de dados.

## Documentação
### Propósito
O `match` é uma função que retorna as posições dos primeiros elementos de um vetor que correspondem a elementos de outro vetor. É especialmente útil em operações de manipulação de dados e análise, onde a correspondência entre diferentes conjuntos de dados é necessária.

### Uso
A função `match` possui a seguinte sintaxe:

```R
match(x, table, nomatch = NA_integer_, incomparables = NULL)
```

#### Parâmetros
- **x**: Um vetor cujos elementos devem ser correspondidos.
- **table**: Um vetor ou lista com os quais os elementos de `x` serão comparados.
- **nomatch**: Valor a ser retornado se não houver correspondência. O padrão é `NA_integer_`.
- **incomparables**: Um vetor opcional de valores que não devem ser considerados como correspondências.

### Detalhes
A função `match` é sensível ao tipo dos elementos, o que significa que elementos de diferentes tipos (por exemplo, caracteres e números) não serão considerados correspondentes, mesmo que seus valores sejam semanticamente iguais.

## Exemplos
### Exemplo Básico
```R
# Vetor de pesquisa
x <- c("maçã", "banana", "laranja")

# Vetor de referência
table <- c("banana", "maçã", "kiwi")

# Uso da função match
posicoes <- match(x, table)
print(posicoes) # Resultado: 2 1 NA
```

### Exemplo com nomatch
```R
# Vetor de pesquisa
x <- c("maçã", "banana", "laranja")

# Uso da função match com valor para 'nomatch'
posicoes <- match(x, table, nomatch = 0)
print(posicoes) # Resultado: 2 1 0
```

## Explicação
Um erro comum ao utilizar a função `match` é esperar que ela retorne índices que correspondam a múltiplas ocorrências. O `match` sempre retorna a primeira correspondência encontrada. Além disso, é importante lembrar que se os vetores `x` e `table` contiverem tipos diferentes (por exemplo, números e caracteres), a correspondência não funcionará como esperado. Para evitar confusões, sempre verifique os tipos dos dados antes de aplicar a função.

## Resumo em Uma Linha
A função `match` em R identifica as posições de elementos de um vetor em outro vetor, retornando os índices das correspondências.