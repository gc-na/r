<!--
Meta Description: # Média em R: Como Calcular a Média de Conjuntos de Dados ## Sinopse A função `mean()` em R é uma ferramenta essencial para calcular a média aritmétic...
Meta Keywords: valores, média, mean, função, não
-->

# Média em R: Como Calcular a Média de Conjuntos de Dados

## Sinopse
A função `mean()` em R é uma ferramenta essencial para calcular a média aritmética de um conjunto de números, sendo amplamente utilizada em análises estatísticas e manipulação de dados.

## Documentação
### Propósito
A função `mean()` é utilizada para calcular a média aritmética de um vetor de valores numéricos. Essa métrica é fundamental em estatística, pois fornece uma medida central dos dados.

### Uso
A função `mean()` pode ser chamada da seguinte forma:

```R
mean(x, na.rm = FALSE, ...)
```

#### Parâmetros:
- `x`: Um vetor numérico ou uma lista de números. Este é o argumento principal da função.
- `na.rm`: Um parâmetro lógico que indica se os valores `NA` (not available) devem ser removidos antes do cálculo. O valor padrão é `FALSE`.
- `...`: Argumentos adicionais que podem ser passados para métodos específicos.

### Detalhes
A média é calculada somando todos os valores do vetor e dividindo pelo número total de elementos. Se `na.rm` for definido como `TRUE`, todos os valores ausentes (NA) serão ignorados no cálculo, evitando resultados inesperados.

## Exemplos
### Exemplo Básico
```R
# Calculando a média de um vetor simples
numeros <- c(1, 2, 3, 4, 5)
media <- mean(numeros)
print(media)  # Saída: 3
```

### Exemplo com NA
```R
# Calculando a média com valores NA
numeros_com_na <- c(1, 2, NA, 4, 5)
media_na_rm <- mean(numeros_com_na, na.rm = TRUE)
print(media_na_rm)  # Saída: 3
```

## Explicação
Ao usar a função `mean()`, é importante estar ciente de que valores `NA` podem afetar o resultado. Se você não remover esses valores, o resultado da média será `NA`. Portanto, sempre considere o uso do argumento `na.rm` quando houver a possibilidade de valores ausentes em seus dados.

### Armadilhas Comuns
- **Valores NA**: Não se esqueça de que a presença de valores `NA` torna o resultado da média indefinido se não forem removidos.
- **Vetores Não Numéricos**: A função `mean()` não funcionará corretamente se aplicada a vetores que contêm tipos de dados não numéricos, resultando em um erro.

## Resumo em Uma Linha
A função `mean()` em R calcula a média aritmética de um vetor numérico, permitindo análises estatísticas eficazes com consideração para valores ausentes.