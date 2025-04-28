<!--
Meta Description: # Filtro em R: Como Utilizar a Função Filter para Manipulação de Dados ## Sinopse A função `filter` do pacote **dplyr** em R é utilizada para selecion...
Meta Keywords: filter, dados, valor, data, condições
-->

# Filtro em R: Como Utilizar a Função Filter para Manipulação de Dados

## Sinopse
A função `filter` do pacote **dplyr** em R é utilizada para selecionar linhas de um data frame com base em condições específicas, permitindo a manipulação eficiente de conjuntos de dados.

## Documentação
A função `filter` é parte do pacote **dplyr**, amplamente utilizado para a transformação e manipulação de dados em R. O seu principal objetivo é extrair subconjuntos de dados que atendam a critérios definidos pelo usuário.

### Uso
A sintaxe básica da função `filter` é a seguinte:

```R
filter(.data, ...)
```

- **.data**: Um data frame ou tibble a ser filtrado.
- **...**: Uma ou mais expressões lógicas que determinam quais linhas devem ser mantidas.

### Detalhes
- O `filter` retorna um novo data frame contendo somente as linhas que satisfazem as condições especificadas.
- É possível combinar múltiplas condições usando operadores lógicos como `&` (E) e `|` (OU).
- As condições podem incluir comparações como `==`, `!=`, `<`, `>`, `<=`, `>=`.

## Exemplos

### Exemplo Básico
```R
library(dplyr)

# Criando um data frame de exemplo
dados <- data.frame(
  id = 1:5,
  valor = c(10, 20, 30, 40, 50)
)

# Filtrando linhas onde o valor é maior que 20
resultado <- filter(dados, valor > 20)
print(resultado)
```

### Filtragem com Múltiplas Condições
```R
# Filtrando linhas onde o valor é maior que 20 e menor que 50
resultado_multiplas <- filter(dados, valor > 20 & valor < 50)
print(resultado_multiplas)
```

### Usando o operador OR
```R
# Filtrando linhas onde o valor é igual a 10 ou 30
resultado_or <- filter(dados, valor == 10 | valor == 30)
print(resultado_or)
```

## Explicação
Ao usar `filter`, é importante ter em mente que:

- A ordem das condições pode afetar o desempenho em conjuntos de dados muito grandes.
- Verifique sempre os tipos de dados das colunas ao aplicar condições, pois comparações entre tipos incompatíveis podem gerar erros ou resultados inesperados.
- O uso de `filter` é case-sensitive, ou seja, ao filtrar strings, a capitalização conta.

## Resumo em uma Linha
A função `filter` em R permite a seleção eficiente de linhas de um data frame com base em condições específicas, facilitando a manipulação de dados.