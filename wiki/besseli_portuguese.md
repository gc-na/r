<!--
Meta Description: # besselI: Função Bessel de Primeira Classe em R ## Sinopse A função `besselI` em R é utilizada para calcular a função de Bessel de primeira classe. E...
Meta Keywords: função, bessel, besseli, valores, primeira
-->

# besselI: Função Bessel de Primeira Classe em R

## Sinopse
A função `besselI` em R é utilizada para calcular a função de Bessel de primeira classe. Essa função é amplamente aplicada em problemas de matemática e física, especialmente em teorias que envolvem ondas e vibrações.

## Documentação
A função `besselI` calcula os valores da função de Bessel de primeira classe \( I_n(x) \) para um ou mais valores de \( x \) e ordens \( n \).

### Uso
```R
besselI(x, n, expon.scaled = FALSE)
```

### Parâmetros
- **x**: Um número ou um vetor de números nos quais se deseja calcular a função de Bessel.
- **n**: A ordem da função de Bessel. Pode ser um número inteiro não negativo ou um vetor de inteiros.
- **expon.scaled**: Um argumento lógico que, se definido como TRUE, retorna a função de Bessel escalonada exponencialmente.

### Detalhes
A função de Bessel de primeira classe é uma solução das equações diferenciais que aparecem em problemas de física e engenharia. A função `besselI` é particularmente útil em aplicações de eletricidade, acústica e mecânica quântica.

## Exemplos
### Exemplo Básico
Calcule a função de Bessel de primeira classe para \( x = 1 \) e ordem \( n = 0 \):
```R
besselI(1, 0)
```

### Vários Valores
Calcule a função de Bessel para um vetor de valores:
```R
valores <- c(0, 1, 2, 3)
besselI(valores, 1)
```

### Escalonamento Exponencial
Utilizando o argumento `expon.scaled`:
```R
besselI(1, 0, expon.scaled = TRUE)
```

## Explicação
Um dos principais erros ao usar a função `besselI` é a confusão entre as ordens. As ordens devem ser inteiros não negativos. Além disso, o usuário deve ter cuidado ao selecionar o argumento `expon.scaled`, pois a interpretação dos resultados muda. A função de Bessel é uma função complexa, e a precisão do resultado pode ser afetada por valores de entrada muito grandes ou muito pequenos.

## Resumo em Uma Linha
A função `besselI` em R calcula a função de Bessel de primeira classe para dados reais e ordens específicas, sendo essencial em diversas aplicações científicas.