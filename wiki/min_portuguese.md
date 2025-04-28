<!--
Meta Description: # Função `min` em R: Como Encontrar o Mínimo de um Conjunto de Dados ## Sinopse A função `min` em R é utilizada para calcular o valor mínimo em um vet...
Meta Keywords: função, min, valores, menor, que
-->

# Função `min` em R: Como Encontrar o Mínimo de um Conjunto de Dados

## Sinopse
A função `min` em R é utilizada para calcular o valor mínimo em um vetor numérico ou em um conjunto de dados, permitindo ao usuário identificar rapidamente o menor elemento de uma coleção.

## Documentação
A função `min` é uma função básica do R que serve para retornar o menor valor de um vetor ou de múltiplos valores numéricos. É frequentemente utilizada em análises estatísticas e manipulação de dados.

### Propósito
O principal objetivo da função `min` é facilitar a identificação do menor elemento em um conjunto de dados, o que é uma operação comum em estatísticas descritivas.

### Uso
A sintaxe básica da função é a seguinte:

```R
min(..., na.rm = FALSE)
```

- `...`: Um ou mais vetores numéricos. Você pode passar múltiplos vetores separados por vírgulas.
- `na.rm`: Um argumento lógico que indica se os valores `NA` (não disponíveis) devem ser removidos antes do cálculo. O padrão é `FALSE`.

### Detalhes
- Se nenhum argumento for fornecido, a função retornará `Inf` (infinito positivo).
- Se todos os valores forem `NA` e `na.rm` for definido como `FALSE`, a função retornará `NA`.
- Com `na.rm = TRUE`, a função ignora os valores `NA` e calcula o mínimo apenas entre os valores disponíveis.

## Exemplos
### Exemplo 1: Uso Básico
```R
# Criar um vetor de números
numeros <- c(5, 3, 8, 1, 4)

# Encontrar o menor número
menor_numero <- min(numeros)
print(menor_numero)  # Resultado: 1
```

### Exemplo 2: Múltiplos Vetores
```R
# Criar dois vetores
vetor1 <- c(10, 20, 30)
vetor2 <- c(5, 15, 25)

# Encontrar o menor valor entre os dois vetores
menor_valor <- min(vetor1, vetor2)
print(menor_valor)  # Resultado: 5
```

### Exemplo 3: Ignorando NAs
```R
# Criar um vetor com valores NA
numeros_com_na <- c(7, NA, 3, 9, NA)

# Encontrar o menor número ignorando NAs
menor_valor_sem_na <- min(numeros_com_na, na.rm = TRUE)
print(menor_valor_sem_na)  # Resultado: 3
```

## Explicação
Um erro comum ao usar a função `min` é esquecer de lidar com valores `NA`. Se não forem tratados, esses valores podem levar a resultados inesperados, como retornar `NA` quando se espera um número. Sempre que houver a possibilidade de valores ausentes, é recomendável usar o argumento `na.rm = TRUE` para garantir que o cálculo do mínimo seja feito corretamente.

Outra armadilha é passar um vetor vazio para a função, o que resultará em um erro. Certifique-se de que sempre existam elementos nos vetores fornecidos.

## Resumo em Uma Linha
A função `min` em R calcula o menor valor de um vetor numérico, com a opção de ignorar valores ausentes.