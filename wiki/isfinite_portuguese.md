<!--
Meta Description: # is.finite: Verificando Valores Finitos em R ## Sinopse A função `is.finite` em R é utilizada para verificar se os elementos de um vetor são números ...
Meta Keywords: finite, que, valores, função, dados
-->

# is.finite: Verificando Valores Finitos em R

## Sinopse
A função `is.finite` em R é utilizada para verificar se os elementos de um vetor são números finitos, retornando um vetor lógico que indica a validade de cada elemento.

## Documentação
### Propósito
A função `is.finite` é essencial para a manipulação de dados em R, permitindo que os usuários identifiquem rapidamente elementos que não são finitos, como `Inf`, `-Inf` e `NA`. Isso é especialmente útil em análises estatísticas e limpeza de dados, onde a presença de valores não finitos pode afetar os resultados.

### Uso
A sintaxe básica da função `is.finite` é a seguinte:

```R
is.finite(x)
```

**Parâmetros:**
- `x`: Um vetor numérico, que pode incluir inteiros, números decimais e valores especiais como `Inf`, `-Inf` e `NA`.

**Valor Retornado:**
A função retorna um vetor lógico (TRUE ou FALSE) do mesmo comprimento que `x`, onde TRUE indica que o elemento correspondente é um número finito.

## Exemplos
### Exemplo 1: Verificação Simples
```R
valores <- c(1, 2, Inf, -Inf, NA)
is.finite(valores)
```
**Saída:**
```
[1]  TRUE  TRUE FALSE FALSE FALSE
```

### Exemplo 2: Aplicando em um Data Frame
```R
dados <- data.frame(a = c(1, 2, Inf), b = c(NA, 3, 4))
dados_finitos <- dados[apply(dados, 1, function(x) all(is.finite(x))), ]
print(dados_finitos)
```
**Saída:**
```
  a b
2 2 3
```

## Explicação
### Armadilhas Comuns
- **Valores NA:** A função `is.finite` não considera `NA` como um valor finito. Se você precisa tratar `NA` de forma diferente, considere usar `is.na` em conjunto.
- **Uso em Análises:** Ignorar a presença de valores infinitos ao realizar análises estatísticas pode levar a resultados enganosos. Sempre verifique a finitude dos dados antes de aplicar funções que dependem de valores finitos.

### Notas Adicionais
- A função `is.finite` é frequentemente utilizada em pré-processamento de dados para garantir que os dados estejam limpos e prontos para análise.
- É uma função vetorial, o que significa que pode ser aplicada diretamente a vetores e listas.

## Resumo em Uma Linha
A função `is.finite` em R verifica se os elementos de um vetor são números finitos, retornando um vetor lógico correspondente.