<!--
Meta Description: # Função cosh em R: Cálculo do Cosseno Hiperbólico ## Sinopse A função `cosh` em R é utilizada para calcular o cosseno hiperbólico de um número ou de ...
Meta Keywords: cosh, cosseno, hiperbólico, função, cálculo
-->

# Função cosh em R: Cálculo do Cosseno Hiperbólico

## Sinopse
A função `cosh` em R é utilizada para calcular o cosseno hiperbólico de um número ou de um vetor de números. Essa função é parte das operações matemáticas básicas disponíveis na linguagem R e é amplamente utilizada em diversas aplicações científicas e estatísticas.

## Documentação
### Propósito
A função `cosh` calcula o cosseno hiperbólico de um valor ou de múltiplos valores, que é definido matematicamente como:

\[ \text{cosh}(x) = \frac{e^x + e^{-x}}{2} \]

onde \( e \) é a base do logaritmo natural.

### Uso
A sintaxe básica para utilizar a função `cosh` é a seguinte:

```R
cosh(x)
```

#### Argumentos
- `x`: Um número ou um vetor numérico. Pode ser um valor escalar, um vetor ou uma matriz.

### Detalhes
A função `cosh` retorna o cosseno hiperbólico para cada valor de entrada. É importante notar que a função aceita tanto números positivos quanto negativos e retorna sempre valores não negativos.

## Exemplos
### Exemplo 1: Cálculo do cosseno hiperbólico de um único valor
```R
# Cálculo do cosseno hiperbólico de 0
resultado <- cosh(0)
print(resultado)  # Resultado: 1
```

### Exemplo 2: Cálculo do cosseno hiperbólico de um vetor
```R
# Cálculo do cosseno hiperbólico de um vetor
valores <- c(-1, 0, 1)
resultados <- cosh(valores)
print(resultados)  # Resultado: 1.5430806348152437 1.0000000000000000 1.5430806348152437
```

### Exemplo 3: Cálculo do cosseno hiperbólico de uma sequência
```R
# Cálculo do cosseno hiperbólico de uma sequência de valores
sequencia <- seq(-2, 2, by = 0.5)
resultados <- cosh(sequencia)
print(resultados)
```

## Explicação
Embora a função `cosh` seja bastante direta, alguns usuários podem enfrentar algumas dificuldades:

- **Entradas Não Numéricas**: A função não aceitará entradas que não sejam numéricas e retornará um erro.
- **Resultados Negativos**: Como o cosseno hiperbólico só produz valores não negativos, qualquer expectativa de resultado negativo deve ser revista.
- **Desempenho com Vetores Grandes**: Ao trabalhar com vetores muito grandes, o desempenho pode ser afetado, embora a função seja otimizada para lidar com operações vetoriais.

## Resumo em uma Frase
A função `cosh` em R calcula o cosseno hiperbólico de um número ou vetor de números, retornando sempre valores não negativos.