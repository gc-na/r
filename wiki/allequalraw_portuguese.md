<!--
Meta Description: # all.equal.raw: Comparando Objetos em R ## Sinopse O comando `all.equal.raw` no R é uma função específica utilizada para comparar objetos de forma de...
Meta Keywords: que, all, equal, raw, objetos
-->

# all.equal.raw: Comparando Objetos em R

## Sinopse
O comando `all.equal.raw` no R é uma função específica utilizada para comparar objetos de forma detalhada, focando em valores brutos. Essa função é especialmente útil para verificar a igualdade de dados em testes unitários e validações.

## Documentação
### Propósito
A função `all.equal.raw` é projetada para avaliar a igualdade de dois objetos, devolvendo um resultado que indica se são equivalentes ou não. É particularmente útil quando se lida com objetos que podem ter pequenas variações em suas representações.

### Uso
A sintaxe básica da função é a seguinte:

```R
all.equal.raw(target, current, ...)
```

**Parâmetros:**
- `target`: O objeto de referência que será comparado.
- `current`: O objeto que está sendo testado para igualdade em relação ao `target`.
- `...`: Argumentos adicionais que podem ser passados para controle de comparação.

### Detalhes
A função `all.equal.raw` retorna um valor lógico (`TRUE` ou `FALSE`), ou uma mensagem detalhada que explica a diferença entre os objetos, se não forem iguais. Essa função é mais rigorosa em comparação com a função `all.equal`, pois se concentra em valores brutos, ignorando aspectos como atributos que não afetam a igualdade dos dados.

## Exemplos
### Exemplo Básico 1: Comparando Vetores
```R
vetor1 <- c(1, 2, 3)
vetor2 <- c(1, 2, 3)
resultado <- all.equal.raw(vetor1, vetor2)
print(resultado)  # TRUE
```

### Exemplo Básico 2: Comparando Listas
```R
lista1 <- list(a = 1, b = 2)
lista2 <- list(a = 1, b = 2)
resultado <- all.equal.raw(lista1, lista2)
print(resultado)  # TRUE
```

### Exemplo Básico 3: Comparando Objetos Diferentes
```R
objeto1 <- c(1, 2, 3)
objeto2 <- c(1, 2, 4)
resultado <- all.equal.raw(objeto1, objeto2)
print(resultado)  # "Componentes '3': 3 != 4"
```

## Explicação
É importante notar que `all.equal.raw` pode não retornar apenas um valor lógico, mas uma string que descreve as diferenças, caso os objetos não sejam equivalentes. Um ponto comum de confusão é pensar que a função se comporta da mesma forma que `identical()`, mas `all.equal.raw` é mais flexível em suas comparações, permitindo pequenas discrepâncias em valores.

Outra armadilha frequente é não considerar a classe dos objetos comparados. Objetos de classes diferentes, mesmo que tenham valores semelhantes, serão considerados diferentes pela função.

## Resumo em Uma Linha
O `all.equal.raw` no R é uma função que compara objetos de forma rigorosa, retornando um valor lógico ou uma descrição das diferenças se os objetos não forem iguais.