<!--
Meta Description: # ifelse: A Função Condicional em R ## Sinopse A função `ifelse` em R é uma ferramenta poderosa que permite realizar operações condicionais em vetores...
Meta Keywords: ifelse, função, condição, para, que
-->

# ifelse: A Função Condicional em R

## Sinopse
A função `ifelse` em R é uma ferramenta poderosa que permite realizar operações condicionais em vetores de maneira eficiente, retornando valores diferentes com base em uma condição lógica.

## Documentação
A função `ifelse` é utilizada para aplicar uma condição a cada elemento de um vetor, retornando um valor específico caso a condição seja verdadeira e outro valor caso seja falsa. Essa função é especialmente útil para manipulação de dados e criação de novas variáveis a partir de condições existentes.

### Uso
A sintaxe da função `ifelse` é a seguinte:

```R
ifelse(condição, valor_se_verdadeiro, valor_se_falso)
```

- **condição**: Um vetor lógico que determina quais elementos devem ser verificados.
- **valor_se_verdadeiro**: O valor que será retornado onde a condição é verdadeira.
- **valor_se_falso**: O valor que será retornado onde a condição é falsa.

### Detalhes
- A função `ifelse` é vetorizada, ou seja, permite que a condição seja aplicada simultaneamente a todos os elementos de um vetor.
- Os valores retornados podem ser de tipos diferentes, mas o R tentará coerci-los para um tipo comum.
- É possível aninhar várias chamadas de `ifelse` para lidar com múltiplas condições, embora isso possa tornar o código mais difícil de ler.

## Exemplos

### Exemplo Básico
```R
# Criando um vetor de notas
notas <- c(5, 7, 9, 4, 6)

# Usando ifelse para classificar as notas
classificacao <- ifelse(notas >= 7, "Aprovado", "Reprovado")
print(classificacao)
```
Saída:
```
[1] "Reprovado" "Aprovado"  "Aprovado"  "Reprovado" "Reprovado"
```

### Exemplo com NAs
```R
# Criando um vetor com NAs
valores <- c(10, NA, 20, NA, 30)

# Substituindo NAs por zero
valores_substituidos <- ifelse(is.na(valores), 0, valores)
print(valores_substituidos)
```
Saída:
```
[1] 10  0 20  0 30
```

## Explicação
Embora a função `ifelse` seja muito útil, alguns cuidados são necessários:
- **Desempenho**: Para grandes conjuntos de dados, `ifelse` pode ser menos eficiente do que funções específicas de manipulação de dados, como `dplyr::mutate`.
- **Aninhamento**: Aninhar várias funções `ifelse` pode levar a um código difícil de entender e manter. Considere usar `dplyr::case_when` para múltiplas condições.
- **Coerção de tipos**: O resultado de `ifelse` pode ter tipos mistos, o que pode causar problemas em operações subsequentes. É sempre bom verificar o tipo do vetor resultante.

## Resumo em Uma Linha
A função `ifelse` em R é uma ferramenta eficiente para realizar operações condicionais em vetores, retornando valores diferentes com base em condições lógicas.