<!--
Meta Description: # Função floor em R: Arredondamento para Baixo de Números ## Sinopse A função `floor` em R é utilizada para arredondar números reais para o inteiro ma...
Meta Keywords: floor, para, função, números, que
-->

# Função floor em R: Arredondamento para Baixo de Números

## Sinopse
A função `floor` em R é utilizada para arredondar números reais para o inteiro mais próximo que é menor ou igual ao número especificado. É uma ferramenta essencial em manipulações numéricas e análises estatísticas.

## Documentação
### Propósito
A função `floor` serve para arredondar valores numéricos para baixo, ou seja, ela retorna o maior inteiro que não excede o valor fornecido.

### Uso
A sintaxe da função `floor` é a seguinte:

```R
floor(x)
```

#### Parâmetros
- `x`: Um vetor numérico que você deseja arredondar para baixo.

#### Detalhes
- A função `floor` pode ser aplicada a vetores, e retornará um vetor do mesmo comprimento com os valores arredondados.
- É importante notar que a função opera em cada elemento do vetor de entrada individualmente.

## Exemplos
### Exemplo Básico
```R
# Arredondando um único número
resultado1 <- floor(3.7)
print(resultado1)  # Saída: 3

# Arredondando um vetor de números
resultado2 <- floor(c(2.3, 4.7, 6.1, -1.2))
print(resultado2)  # Saída: 2 4 6 -2
```

### Exemplo com Números Negativos
```R
# Arredondando um número negativo
resultado3 <- floor(-2.5)
print(resultado3)  # Saída: -3
```

## Explicação
A função `floor` é bastante direta e intuitiva, mas alguns pontos comuns podem causar confusão:

1. **Números Negativos**: Para números negativos, o arredondamento é feito para o próximo inteiro menor. Por exemplo, `floor(-2.3)` resulta em `-3`, não em `-2`.

2. **Vetores**: Quando usada com vetores, `floor` aplica a operação de arredondamento em cada elemento individualmente, o que pode ser útil em análises de dados.

3. **Comparação com Outras Funções**: É comum confundir `floor` com funções como `ceiling` (que arredonda para cima) ou `round` (que arredonda para o inteiro mais próximo). Compreender a diferença é crucial para evitar erros em cálculos.

## Resumo em Uma Linha
A função `floor` em R arredonda números reais para o inteiro mais próximo inferior, sendo útil em diversas análises numéricas.