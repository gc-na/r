<!--
Meta Description: # Duplicados no R: Comando `duplicated.default` ## Sinopse O comando `duplicated.default` em R é utilizado para identificar elementos duplicados em um...
Meta Keywords: false, duplicados, duplicated, vetor, que
-->

# Duplicados no R: Comando `duplicated.default`

## Sinopse
O comando `duplicated.default` em R é utilizado para identificar elementos duplicados em um vetor ou em uma lista, retornando um vetor lógico que indica quais elementos são duplicados.

## Documentação
### Propósito
O `duplicated.default` é uma função fundamental no R para detectar valores que aparecem mais de uma vez em um vetor ou lista. Isso é especialmente útil em análises de dados, onde a presença de duplicados pode afetar resultados e interpretações.

### Uso
A função é geralmente chamada através do comando `duplicated()`, que é uma interface mais amigável para o método `duplicated.default`. Sua sintaxe básica é:

```R
duplicated(x, incomparables = FALSE, fromLast = FALSE, ...)
```

- **x**: Um vetor ou uma lista de onde os duplicados serão identificados.
- **incomparables**: Valores que não devem ser considerados na comparação (padrão é FALSE).
- **fromLast**: Se TRUE, a busca por duplicados começa do final do vetor para o início.
- **...**: Outros argumentos que podem ser passados para métodos específicos.

### Detalhes
A função retorna um vetor lógico do mesmo comprimento que `x`, onde cada posição indica se o elemento correspondente é uma duplicata (TRUE) ou não (FALSE). Os primeiros valores idênticos recebem FALSE, enquanto as ocorrências subsequentes retornam TRUE.

## Exemplos
### Exemplo Básico
```R
# Criando um vetor com valores duplicados
valores <- c(1, 2, 3, 2, 1, 4)

# Identificando duplicados
duplicados <- duplicated(valores)
print(duplicados)
```
Saída:
```
[1] FALSE FALSE FALSE  TRUE  TRUE FALSE
```

### Usando `fromLast`
```R
# Identificando duplicados a partir do final
duplicados_reversa <- duplicated(valores, fromLast = TRUE)
print(duplicados_reversa)
```
Saída:
```
[1]  TRUE  TRUE FALSE FALSE FALSE FALSE
```

## Explicação
Um ponto importante a considerar é que o `duplicated.default` não altera o vetor original, apenas fornece um vetor lógico. Além disso, o parâmetro `fromLast` pode ser confuso, pois muda a ordem de verificação dos elementos, o que pode levar a resultados inesperados. Outro detalhe é que a função não considera elementos que não sejam comparáveis (como listas aninhadas) quando `incomparables` é usado.

## Resumo em Uma Linha
O comando `duplicated.default` em R é usado para identificar elementos duplicados em vetores e listas, retornando um vetor lógico correspondente.