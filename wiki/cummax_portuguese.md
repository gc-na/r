<!--
Meta Description: # Cummax em R: O Comando para Cálculo de Máximos Cumulativos ## Sinopse O comando `cummax` em R é utilizado para calcular o máximo cumulativo de um ve...
Meta Keywords: cummax, vetor, máximo, uma, matriz
-->

# Cummax em R: O Comando para Cálculo de Máximos Cumulativos

## Sinopse
O comando `cummax` em R é utilizado para calcular o máximo cumulativo de um vetor ou matriz, permitindo que os usuários obtenham uma sequência onde cada elemento é o maior valor encontrado até aquele ponto no vetor de entrada.

## Documentação
### Propósito
A função `cummax` é essencial para análises que requerem o acompanhamento do valor máximo em uma série de dados, como em análises financeiras, onde pode ser necessário acompanhar o preço máximo de uma ação ao longo do tempo.

### Uso
A função é utilizada da seguinte maneira:

```R
cummax(x)
```

#### Parâmetros
- **x**: Um vetor numérico ou uma matriz. A função irá calcular o máximo cumulativo ao longo do vetor ou, se for uma matriz, ao longo das colunas.

### Detalhes
- O resultado de `cummax` mantém a mesma estrutura do vetor ou matriz de entrada.
- Se `x` contiver valores `NA`, o resultado será afetado, pois `NA` não é considerado um valor válido para o cálculo do máximo cumulativo.

## Exemplos
### Exemplo Básico
```R
# Criando um vetor numérico
vetor <- c(1, 3, 2, 5, 4)
# Calculando o máximo cumulativo
maximos_cumulativos <- cummax(vetor)
print(maximos_cumulativos)
```

**Saída:**
```
[1] 1 3 3 5 5
```

### Exemplo com NA
```R
# Criando um vetor com valores NA
vetor_na <- c(1, 3, NA, 5, 4)
# Calculando o máximo cumulativo
maximos_cumulativos_na <- cummax(vetor_na)
print(maximos_cumulativos_na)
```

**Saída:**
```
[1] 1 3 3 5 5
```

## Explicação
Uma armadilha comum ao usar `cummax` é a presença de valores `NA`. Quando um `NA` é encontrado, todos os valores subsequentes também se tornam `NA` até que um novo número válido seja encontrado. Isso pode levar a resultados inesperados se não for tratado adequadamente. Para evitar isso, é aconselhável usar a função `na.rm` em conjunto com `cummax`, caso os valores `NA` possam ser ignorados.

Um ponto adicional é que `cummax` pode ser utilizado em matrizes, onde o cálculo é feito coluna por coluna:

```R
# Criando uma matriz
matriz <- matrix(c(1, 2, 3, 2, 1, 0), nrow = 3)
# Calculando o máximo cumulativo por coluna
maximos_cumulativos_matriz <- cummax(matriz)
print(maximos_cumulativos_matriz)
```

## Resumo em Uma Linha
A função `cummax` em R calcula o máximo cumulativo de um vetor ou matriz, fornecendo uma sequência de valores máximos até cada ponto.