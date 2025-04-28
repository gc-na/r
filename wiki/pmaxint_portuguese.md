<!--
Meta Description: # pmax.int: Função para o Máximo Elemento em R ## Sinopse A função `pmax.int` em R é utilizada para calcular o máximo elemento entre vetores ou arrays...
Meta Keywords: vetores, pmax, int, resultado, função
-->

# pmax.int: Função para o Máximo Elemento em R

## Sinopse
A função `pmax.int` em R é utilizada para calcular o máximo elemento entre vetores ou arrays de inteiros, retornando um vetor com os valores máximos correspondentes.

## Documentação
### Propósito
A função `pmax.int` é projetada para facilitar a obtenção do valor máximo em cada posição de múltiplos vetores ou arrays de inteiros. Essa função é especialmente útil em operações de comparação entre conjuntos de dados.

### Uso
```R
pmax.int(..., na.rm = FALSE)
```

#### Argumentos
- `...`: Um ou mais vetores ou arrays de inteiros que serão comparados.
- `na.rm`: Um valor lógico que indica se os valores `NA` devem ser removidos antes da comparação. O padrão é `FALSE`.

### Detalhes
A função `pmax.int` retorna um vetor cujos elementos são o máximo correspondente de cada posição dos vetores de entrada. Se for passado um vetor de comprimento diferente, ele será reciclado conforme as regras de reciclagem do R. Caso algum dos vetores contenha `NA` e `na.rm` estiver definido como `FALSE`, o resultado para aquela posição será `NA`.

## Exemplos
Aqui estão alguns exemplos que demonstram o uso da função `pmax.int`:

### Exemplo 1: Comparando dois vetores
```R
vetor1 <- c(1L, 5L, 3L)
vetor2 <- c(2L, 3L, 4L)
resultado <- pmax.int(vetor1, vetor2)
print(resultado)  # Saída: 2 5 4
```

### Exemplo 2: Comparando múltiplos vetores
```R
vetor1 <- c(1L, 5L, NA)
vetor2 <- c(2L, 3L, 4L)
vetor3 <- c(0L, 6L, 1L)
resultado <- pmax.int(vetor1, vetor2, vetor3, na.rm = TRUE)
print(resultado)  # Saída: 2 6 4
```

### Exemplo 3: Com NA e na.rm = FALSE
```R
vetor1 <- c(1L, NA, 3L)
vetor2 <- c(2L, 3L, 4L)
resultado <- pmax.int(vetor1, vetor2)
print(resultado)  # Saída: 2 NA 4
```

## Explicação
Um erro comum ao usar `pmax.int` é esquecer de tratar os valores `NA`. Se `na.rm` é deixado como `FALSE`, e um dos vetores contém `NA`, o resultado para aquela posição será `NA`, o que pode não ser o comportamento esperado. Portanto, é sempre bom considerar se a remoção de `NA` é necessária para a análise desejada.

Outro ponto importante é a reciclagem de vetores. Se os vetores de entrada não têm o mesmo comprimento, R irá reciclar os valores dos vetores menores até que todos tenham o mesmo tamanho. Isso pode levar a resultados inesperados, então tenha cuidado ao passar vetores de diferentes comprimentos.

## Resumo em Uma Linha
A função `pmax.int` em R retorna o máximo elemento entre vetores de inteiros, permitindo operações eficientes de comparação.