<!--
Meta Description: # endsWith: Verificando Sufixos em Strings no R ## Sinopse A função `endsWith` em R é utilizada para verificar se uma string termina com um determinad...
Meta Keywords: endswith, sufixo, strings, função, uma
-->

# endsWith: Verificando Sufixos em Strings no R

## Sinopse
A função `endsWith` em R é utilizada para verificar se uma string termina com um determinado sufixo. Essa funcionalidade é útil em operações de manipulação de texto, permitindo filtrar ou identificar strings com base em seus finais.

## Documentação
A função `endsWith` faz parte do pacote base do R e tem a seguinte sintaxe:

```R
endsWith(x, suffix)
```

### Parâmetros
- **x**: Uma string ou vetor de strings que será avaliado.
- **suffix**: O sufixo a ser verificado. Pode ser uma string única ou um vetor de strings.

### Retorno
A função retorna um vetor lógico (TRUE ou FALSE) indicando se cada elemento de `x` termina com o sufixo especificado.

## Exemplos

```R
# Exemplo básico
strings <- c("programacao", "Rprogram", "data")
sufixo <- "gram"
resultado <- endsWith(strings, sufixo)
print(resultado)  # Saída: FALSE  TRUE  FALSE

# Verificando com outro sufixo
sufixo2 <- "data"
resultado2 <- endsWith(strings, sufixo2)
print(resultado2)  # Saída: FALSE FALSE  TRUE
```

## Explicação
Um erro comum ao usar `endsWith` é não considerar a sensibilidade a maiúsculas e minúsculas. A função distingue letras maiúsculas de minúsculas, portanto, "Program" e "program" seriam tratados como diferentes. 

Além disso, ao passar um vetor de sufixos, `endsWith` só aceita um único sufixo de cada vez. Se você quiser verificar múltiplos sufixos, precisará implementar uma lógica adicional, como um loop ou aplicar a função em conjunto com `sapply`.

## Resumo em Uma Linha
A função `endsWith` em R permite verificar se uma string termina com um sufixo específico, retornando um vetor lógico correspondente.