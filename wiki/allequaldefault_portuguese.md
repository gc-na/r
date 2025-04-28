<!--
Meta Description: # all.equal.default: Comparação de Objetos em R ## Sinopse O `all.equal.default` é uma função em R que permite comparar objetos de forma flexível, ver...
Meta Keywords: all, equal, objetos, comparação, default
-->

# all.equal.default: Comparação de Objetos em R

## Sinopse
O `all.equal.default` é uma função em R que permite comparar objetos de forma flexível, verificando sua equivalência de maneira tolerante a pequenas diferenças numéricas e atributos.

## Documentação
A função `all.equal.default` é parte do sistema de comparação de objetos em R, projetada para avaliar se dois objetos são quase iguais. Isso é particularmente útil quando se lida com números em ponto flutuante, onde pequenas variações podem ocorrer devido a operações computacionais.

### Propósito
A função serve para verificar a equivalência de dois objetos, retornando um valor lógico ou uma mensagem detalhada sobre as diferenças encontradas.

### Uso
A função pode ser chamada da seguinte forma:

```R
all.equal(target, current, ...)
```

- **target**: O objeto contra o qual você deseja comparar.
- **current**: O objeto que está sendo comparado.
- **...**: Argumentos adicionais que podem ser passados para métodos específicos.

### Detalhes
- A função retorna `TRUE` se os objetos forem considerados iguais, ou uma descrição das diferenças se não forem.
- É útil para comparações que envolvem listas, data frames, e outras estruturas complexas.
- O comportamento padrão pode ser ajustado com argumentos como `tolerance` e `check.attributes`.

## Exemplos
Aqui estão alguns exemplos básicos de como utilizar `all.equal.default`:

### Exemplo 1: Comparação de Números
```R
x <- 0.1 + 0.2
y <- 0.3
all.equal(x, y)  # Retorna TRUE
```

### Exemplo 2: Comparação de Vetores
```R
vec1 <- c(1, 2, 3)
vec2 <- c(1, 2, 3)
all.equal(vec1, vec2)  # Retorna TRUE
```

### Exemplo 3: Comparação de Listas
```R
list1 <- list(a = 1, b = 2)
list2 <- list(a = 1, b = 2)
all.equal(list1, list2)  # Retorna TRUE
```

### Exemplo 4: Comparação com Atributos
```R
attr1 <- structure(c(1, 2, 3), dim = c(3, 1), class = "matrix")
attr2 <- structure(c(1, 2, 3), dim = c(3, 1), class = "matrix")
all.equal(attr1, attr2)  # Retorna TRUE
```

## Explicação
Alguns pontos a serem observados ao utilizar `all.equal.default`:

- **Diferenças Numéricas**: Quando comparando números, a função considera uma tolerância padrão. Para personalizar isso, você pode usar o argumento `tolerance`.
- **Atributos**: Se os atributos dos objetos não forem relevantes para a comparação, você pode usar `check.attributes = FALSE`.
- **Objetos Complexos**: Para listas ou data frames, a comparação pode falhar se as estruturas não forem idênticas, mesmo que os dados sejam equivalentes.
- **Mensagens de Erro**: Se os objetos não forem iguais, `all.equal.default` fornece mensagens descritivas que ajudam a identificar as diferenças.

## Resumo em Uma Linha
O `all.equal.default` em R é uma função que compara objetos de forma flexível, permitindo detectar equivalências com tolerância a pequenas variações numéricas.