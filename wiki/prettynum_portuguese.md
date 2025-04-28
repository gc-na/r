<!--
Meta Description: # prettyNum: Formatação de Números em R ## Sinopse O `prettyNum` é uma função em R que permite formatar números de forma a torná-los mais legíveis e a...
Meta Keywords: prettynum, números, 000, função, que
-->

# prettyNum: Formatação de Números em R

## Sinopse
O `prettyNum` é uma função em R que permite formatar números de forma a torná-los mais legíveis e apresentáveis, especialmente em contextos de relatórios ou visualizações gráficas.

## Documentação
### Propósito
A função `prettyNum` é utilizada para formatar números, permitindo a personalização da apresentação de valores numéricos. Isso é especialmente útil ao lidar com grandes números ou ao desejar uma apresentação mais estética dos dados.

### Uso
A sintaxe básica da função é:

```R
prettyNum(x, ...)
```

#### Argumentos
- `x`: Um vetor numérico que você deseja formatar.
- `...`: Argumentos adicionais que podem ser passados para a função, incluindo:
  - `big.mark`: Um caractere usado como separador de milhar (padrão é `","`).
  - `decimal.mark`: Um caractere usado como separador decimal (padrão é `"."`).
  - `scientific`: Um valor lógico que determina se a saída deve ser em notação científica (padrão é `FALSE`).
  - `preserve.width`: Um valor lógico que indica se a largura do vetor de entrada deve ser preservada na saída (padrão é `FALSE`).

### Detalhes
A função `prettyNum` é especialmente útil em relatórios e visualizações, pois melhora a legibilidade dos números, tornando-os mais intuitivos para os usuários. Ela permite o controle sobre como os números são apresentados, facilitando a interpretação de dados financeiros, estatísticos e científicos.

## Exemplos
Aqui estão alguns exemplos básicos de uso da função `prettyNum`:

```R
# Exemplo 1: Formatação simples
numeros <- c(1000, 2000.5, 3000000)
prettyNum(numeros)
# Saída: "1,000" "2,000.5" "3,000,000"

# Exemplo 2: Mudando o separador de milhar
prettyNum(numeros, big.mark = ".")
# Saída: "1.000" "2.000,5" "3.000.000"

# Exemplo 3: Usando notação científica
prettyNum(c(0.000123, 1234567), scientific = TRUE)
# Saída: "1.23e-04" "1.23e+06"
```

## Explicação
### Armadilhas Comuns
- **Separadores**: Um erro comum é não definir corretamente os separadores de milhar e decimal, o que pode resultar em formatação confusa, especialmente em contextos internacionais onde os padrões podem variar.
- **Preservação de largura**: Ao não usar o argumento `preserve.width`, a saída pode não refletir a formatação esperada em tabelas ou gráficos, já que a largura dos números pode mudar.
- **Notação científica**: Usar a notação científica sem necessidade pode tornar os números mais difíceis de ler, especialmente para o público geral.

## Resumo em Uma Linha
A função `prettyNum` em R formata números para melhor legibilidade, permitindo personalização de separadores e notação.