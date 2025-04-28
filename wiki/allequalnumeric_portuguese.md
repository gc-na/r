<!--
Meta Description: # all.equal.numeric: Comparação de Números em R ## Sinopse O `all.equal.numeric` é uma função em R que permite comparar dois números (ou vetores numér...
Meta Keywords: all, equal, números, que, uma
-->

# all.equal.numeric: Comparação de Números em R

## Sinopse
O `all.equal.numeric` é uma função em R que permite comparar dois números (ou vetores numéricos) para verificar se eles são praticamente iguais, levando em consideração uma tolerância para comparação.

## Documentação
### Propósito
A função `all.equal.numeric` é utilizada para comparar valores numéricos com uma precisão específica. É especialmente útil em situações onde a comparação direta pode falhar devido a pequenas discrepâncias, como aquelas que podem surgir de cálculos numéricos. 

### Uso
A sintaxe básica da função é:

```R
all.equal(target, current, tolerance = .Machine$double.eps^0.5, ...)
```

#### Parâmetros:
- **target**: O número ou vetor numérico que você deseja comparar.
- **current**: O número ou vetor numérico a ser comparado com o `target`.
- **tolerance**: Um valor que define o quão próximos os números devem estar para serem considerados iguais. O padrão é a raiz quadrada do menor número positivo representável em R.
- **...**: Argumentos adicionais que podem ser passados para métodos específicos.

### Detalhes
A função retorna um valor lógico (`TRUE` ou `FALSE`) ou uma mensagem indicando a diferença entre os valores, caso eles não sejam considerados iguais. A comparação é feita com base na tolerância especificada, o que a torna mais flexível em relação à função `==`, que pode falhar em comparação de números de ponto flutuante.

## Exemplos
### Exemplo Básico
```R
# Comparando dois números iguais
all.equal(0.1 + 0.2, 0.3)
# Saída: [1] TRUE

# Comparando dois números com pequena diferença
all.equal(0.1 + 0.2, 0.3000000001)
# Saída: [1] "Mean relative difference: 3.333333e-10"
```

### Exemplo com Vetores
```R
# Comparando dois vetores numéricos
a <- c(1.00001, 2.00001, 3.00001)
b <- c(1, 2, 3)

all.equal(a, b)
# Saída: [1] "Mean relative difference: 3.333333e-10"
```

## Explicação
Embora `all.equal.numeric` seja uma ferramenta poderosa, existem algumas armadilhas comuns que os usuários devem estar cientes:

1. **Precisão de Ponto Flutuante**: Devido à forma como os números de ponto flutuante são representados na memória, pequenas diferenças podem ocorrer. É essencial ajustar a tolerância quando necessário.
   
2. **Comparação Direta**: Para números que devem ser exatamente iguais, a comparação direta (`==`) deve ser utilizada, pois `all.equal` é projetada para verificar igualdade "aproximada".

3. **Diferenças de Escala**: Ao comparar números em escalas muito diferentes, considerar a tolerância é crucial para evitar falsas negativas.

## Resumo em Uma Linha
`all.equal.numeric` em R é uma função que compara números e vetores numéricos, permitindo uma comparação flexível com base em uma tolerância definida.