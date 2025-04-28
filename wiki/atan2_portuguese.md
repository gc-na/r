<!--
Meta Description: # atan2 em R: Cálculo de Arcos Tangente com Duas Coordenadas ## Sinopse A função `atan2` em R é utilizada para calcular o arco tangente de duas variáv...
Meta Keywords: atan2, ângulo, para, coordenadas, função
-->

# atan2 em R: Cálculo de Arcos Tangente com Duas Coordenadas

## Sinopse
A função `atan2` em R é utilizada para calcular o arco tangente de duas variáveis, permitindo a determinação do ângulo em relação ao eixo X em um plano cartesiano, considerando os sinais das coordenadas.

## Documentação
A função `atan2` é especialmente útil em aplicações de geometria e análise de dados, onde é necessário obter ângulos a partir de coordenadas cartesianas. A função tem a seguinte sintaxe:

```R
atan2(y, x)
```

### Propósito
`atan2` calcula o ângulo θ entre o vetor (x, y) e o eixo X, levando em consideração o quadrante correto, o que evita ambiguidades que podem ocorrer com a função `atan`.

### Uso
- **y**: Coordenada vertical (ordenada).
- **x**: Coordenada horizontal (abscissa).
  
A função retorna o ângulo em radianos, variando de -π até π.

### Detalhes
- O resultado é sensível ao sinal de `x` e `y`, garantindo que o ângulo retornado esteja sempre no quadrante correto.
- A função pode ser aplicada em conjunto com outras funções para conversão de radianos para graus, se necessário, usando `rad2deg` ou similar.

## Exemplos
### Exemplo Básico
```R
# Cálculo do ângulo para as coordenadas (1, 1)
angulo1 <- atan2(1, 1)
print(angulo1)  # Resulta em 0.7853982 (ou π/4 radianos)

# Cálculo do ângulo para as coordenadas (-1, 1)
angulo2 <- atan2(1, -1)
print(angulo2)  # Resulta em 2.3561945 (ou 3π/4 radianos)

# Cálculo do ângulo para as coordenadas (-1, -1)
angulo3 <- atan2(-1, -1)
print(angulo3)  # Resulta em -3.9269908 (ou -π/4 radianos)
```

## Explicação
### Armadilhas Comuns e Notas
- **Quadrantes**: É crucial entender que `atan2` distingue entre os quadrantes, portanto, um ponto no segundo quadrante resultará em um ângulo diferente do mesmo ponto no quarto quadrante.
- **Retorno em Radianos**: Os resultados são retornados em radianos. Para convertê-los em graus, multiplique o resultado por (180/π).
- **Entradas Zero**: Se ambos `x` e `y` forem zero, `atan2(0, 0)` retornará `NaN`, que deve ser tratado adequadamente em aplicações práticas.

## Resumo em Uma Linha
A função `atan2` em R calcula o ângulo entre o eixo X e um vetor definido por coordenadas cartesianas, considerando os sinais das entradas para determinar o quadrante correto.