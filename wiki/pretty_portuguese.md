<!--
Meta Description: # Pretty: Aprimorando a Exibição de Dados em R ## Sinopse O comando `pretty` em R é utilizado para criar sequências de números que são "bonitas" e fác...
Meta Keywords: pretty, que, números, gráficos, intervalo
-->

# Pretty: Aprimorando a Exibição de Dados em R

## Sinopse
O comando `pretty` em R é utilizado para criar sequências de números que são "bonitas" e fáceis de ler, especialmente em gráficos e tabelas. Ele ajuda na formatação de eixos e na apresentação de dados de forma mais amigável.

## Documentação
A função `pretty` gera um vetor de números que dividem um intervalo de maneira mais esteticamente agradável, utilizando intervalos que são múltiplos de valores redondos. É especialmente útil para melhorar a legibilidade de gráficos.

### Propósito
O propósito principal do `pretty` é facilitar a visualização de dados, garantindo que os números nos eixos dos gráficos ou nas tabelas sejam fáceis de entender.

### Uso
A função `pretty` é utilizada da seguinte forma:

```R
pretty(x, n = 5, min.n = 1)
```

- **x**: Um vetor numérico que define o intervalo que você deseja "embelezar".
- **n**: Um número que especifica quantos números bonitos você deseja gerar (o padrão é 5).
- **min.n**: O número mínimo de pontos a serem gerados (o padrão é 1).

### Detalhes
A função `pretty` é frequentemente utilizada em combinação com gráficos, pois ajuda a melhorar a apresentação dos eixos. O resultado é um vetor que pode ser diretamente utilizado no parâmetro `axes` de funções de criação de gráficos.

## Exemplos
Aqui estão alguns exemplos básicos de como usar a função `pretty`:

```R
# Exemplo 1: Criando números bonitos para o intervalo de 1 a 10
numeros_bonitos <- pretty(c(1, 10))
print(numeros_bonitos)  # Saída: [1]  1  2  3  4  5  6  7  8  9 10

# Exemplo 2: Usando com um intervalo mais amplo
numeros_bonitos <- pretty(c(50, 150), n = 8)
print(numeros_bonitos)  # Saída: [1]  50  60  70  80  90 100 110 120 130 140 150
```

## Explicação
Um erro comum ao utilizar `pretty` é não ajustar o parâmetro `n` conforme necessário. Se você estiver lidando com um intervalo muito pequeno, o valor padrão de `n` pode gerar muitos números, tornando a visualização confusa. Além disso, é importante lembrar que o `pretty` pode não sempre produzir os resultados esperados se os dados estiverem muito concentrados em um pequeno intervalo.

## Resumo em Uma Linha
A função `pretty` em R gera sequências de números estéticos e legíveis, melhorando a apresentação de dados em gráficos e tabelas.