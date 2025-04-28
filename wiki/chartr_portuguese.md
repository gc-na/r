<!--
Meta Description: # chartr: Função em R para Substituição de Caracteres ## Sinopse A função `chartr` em R é utilizada para substituir caracteres em strings de forma efi...
Meta Keywords: caracteres, chartr, função, strings, uma
-->

# chartr: Função em R para Substituição de Caracteres

## Sinopse
A função `chartr` em R é utilizada para substituir caracteres em strings de forma eficiente. É uma ferramenta poderosa para manipulação de texto, especialmente útil em processos de limpeza de dados.

## Documentação
### Propósito
A função `chartr` tem como principal objetivo substituir caracteres específicos em uma string por outros caracteres. Essa funcionalidade é frequentemente utilizada em tarefas de pré-processamento de dados, onde a limpeza e a formatação de strings são necessárias.

### Uso
A sintaxe básica da função é a seguinte:

```R
chartr(old, new, x)
```

#### Parâmetros
- **old**: Uma string contendo os caracteres que você deseja substituir.
- **new**: Uma string contendo os caracteres que substituirão os caracteres especificados em `old`. Os caracteres devem estar na mesma ordem que em `old`.
- **x**: A string ou vetor de strings onde a substituição será realizada.

### Detalhes
A função `chartr` é sensível a maiúsculas e minúsculas. Portanto, "A" e "a" são tratados como caracteres distintos. Além disso, a função não realiza substituições parciais ou baseadas em substrings; ela substitui apenas os caracteres exatos fornecidos.

## Exemplos
### Exemplo Básico
```R
# Substituindo caracteres em uma string
resultado <- chartr("abc", "123", "aabbcc")
print(resultado)  # Saída: "112233"
```

### Exemplo com Várias Strings
```R
# Substituindo caracteres em um vetor de strings
strings <- c("abc", "def", "ghi")
resultado <- chartr("abc", "123", strings)
print(resultado)  # Saída: "123" "def" "ghi"
```

## Explicação
Um dos principais cuidados ao usar a função `chartr` é garantir que os vetores `old` e `new` tenham o mesmo comprimento. Caso contrário, a função irá gerar um erro. Além disso, como a função não realiza substituições parciais, se você precisar substituir uma substring maior, é recomendável usar a função `gsub` em vez de `chartr`.

Outro ponto a considerar é a performance; `chartr` é otimizada para substituições simples e rápidas, mas para manipulações mais complexas que envolvem padrões, `gsub` e `sub` devem ser preferidos.

## Resumo em Uma Linha
A função `chartr` em R permite substituir caracteres específicos em strings de forma eficiente e direta.