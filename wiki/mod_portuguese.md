<!--
Meta Description: # Mod: Operador de Módulo no R ## Sinopse O operador `mod` no R, representado pelo símbolo `%/%` ou `%%`, é utilizado para calcular o resto da divisão...
Meta Keywords: divisão, resultado, mod, operador, resto
-->

# Mod: Operador de Módulo no R

## Sinopse
O operador `mod` no R, representado pelo símbolo `%/%` ou `%%`, é utilizado para calcular o resto da divisão entre dois números. É uma ferramenta fundamental em operações matemáticas e manipulação de dados.

## Documentação
O operador `mod` em R é utilizado para obter o resto da divisão inteira. Ele pode ser acessado através do operador `%%` para o resto e `%/%` para a divisão inteira. O uso do `mod` é essencial em diversas aplicações, como em programação condicional, iterações e manipulação de vetores.

### Propósito
O operador `mod` serve para determinar a parte inteira de uma divisão e o resto, permitindo que os programadores realizem operações que dependem da divisibilidade.

### Uso
A sintaxe básica do operador `mod` é a seguinte:

```R
resultado <- a %% b
```
onde `a` é o dividendo e `b` é o divisor.

## Exemplos
### Exemplo 1: Uso Básico do Operador Módulo
```R
# Resto da divisão entre 10 e 3
resultado <- 10 %% 3
print(resultado)  # Saída: 1
```

### Exemplo 2: Aplicação em Vetores
```R
# Resto da divisão de um vetor
vetor <- c(10, 20, 30)
resultado <- vetor %% 7
print(resultado)  # Saída: 3 6 2
```

### Exemplo 3: Divisão Inteira
```R
# Divisão inteira de 10 por 3
resultado <- 10 %/% 3
print(resultado)  # Saída: 3
```

## Explicação
Um erro comum ao usar o operador `mod` é esquecer que ele retorna o resto da divisão e não o resultado da divisão. Além disso, é importante notar que o resultado do `mod` pode ser negativo se o dividendo for negativo. Por exemplo:

```R
# Resto da divisão de -10 por 3
resultado <- -10 %% 3
print(resultado)  # Saída: 2
```

Isso ocorre porque o resultado do operador `mod` é sempre não negativo quando o divisor é positivo.

## Resumo em Uma Linha
O operador `mod` em R, representado por `%%`, calcula o resto da divisão entre dois números, sendo essencial para operações matemáticas e manipulação de dados.