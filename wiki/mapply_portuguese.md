<!--
Meta Description: # mapply: Função de Aplicação Simultânea em R ## Sinopse A função `mapply` no R é uma ferramenta poderosa que permite aplicar uma função a várias list...
Meta Keywords: função, mapply, vetores, uma, que
-->

# mapply: Função de Aplicação Simultânea em R

## Sinopse
A função `mapply` no R é uma ferramenta poderosa que permite aplicar uma função a várias listas ou vetores de forma simultânea, facilitando operações que requerem a combinação de múltiplos conjuntos de dados.

## Documentação
A função `mapply` é uma extensão da função `sapply`, permitindo que múltiplos argumentos sejam passados para a função especificada. Seu propósito principal é aplicar uma função a cada elemento de uma lista ou vetor, onde a função pode aceitar múltiplos argumentos.

### Uso
A sintaxe básica da função `mapply` é a seguinte:

```R
mapply(FUN, ..., MoreArgs = NULL, SIMPLIFY = TRUE, USE.NAMES = TRUE)
```

- **FUN**: A função a ser aplicada.
- **...**: Vetores ou listas a serem passados como argumentos para a função.
- **MoreArgs**: Lista opcional de argumentos adicionais a serem passados para a função.
- **SIMPLIFY**: Lógico; se `TRUE`, o resultado será simplificado para um vetor ou matriz, quando possível.
- **USE.NAMES**: Lógico; se `TRUE`, os nomes dos resultados serão mantidos.

### Detalhes
A função `mapply` é especialmente útil quando se deseja realizar operações que requerem a combinação de múltiplas fontes de dados. Ao contrário de `lapply`, que itera sobre listas, `mapply` permite passar múltiplos vetores ou listas como argumentos, aplicando a função a cada combinação de elementos.

## Exemplos
### Exemplo Básico 1: Soma de Dois Vetores
```R
# Definindo dois vetores
vetor1 <- c(1, 2, 3)
vetor2 <- c(4, 5, 6)

# Usando mapply para somar elementos correspondentes
resultado <- mapply(sum, vetor1, vetor2)
print(resultado)  # Saída: 5 7 9
```

### Exemplo Básico 2: Função Personalizada
```R
# Função personalizada que calcula a potência
potencia <- function(base, expoente) {
  return(base ^ expoente)
}

# Usando mapply com a função personalizada
resultado <- mapply(potencia, base = c(2, 3, 4), expoente = c(3, 2, 1))
print(resultado)  # Saída: 8 9 4
```

## Explicação
Embora `mapply` seja uma ferramenta poderosa, é importante observar algumas considerações:

- **Dimensões dos vetores**: Todos os vetores ou listas fornecidos devem ter o mesmo comprimento. Caso contrário, `mapply` irá reciclar os elementos dos vetores mais curtos, o que pode levar a resultados inesperados.
  
- **Simplificação**: O parâmetro `SIMPLIFY` pode não simplificar o resultado se a função aplicada retornar estruturas de dados complexas, como listas aninhadas.

- **Nomes**: Se `USE.NAMES` estiver definido como `TRUE`, os nomes dos vetores de entrada serão utilizados nos resultados, facilitando a identificação.

## Resumo em Uma Linha
A função `mapply` em R permite aplicar uma função a múltiplos vetores ou listas simultaneamente, facilitando operações combinadas de forma eficiente.