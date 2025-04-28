<!--
Meta Description: # commandArgs: Como Utilizar Argumentos de Linha de Comando em R ## Sinopse O `commandArgs` é uma função em R que permite acessar os argumentos passad...
Meta Keywords: argumentos, script, commandargs, que, linha
-->

# commandArgs: Como Utilizar Argumentos de Linha de Comando em R

## Sinopse
O `commandArgs` é uma função em R que permite acessar os argumentos passados para um script a partir da linha de comando. Essa funcionalidade é especialmente útil para a automação de scripts e execução de tarefas com diferentes parâmetros sem precisar modificar o código.

## Documentação
### Descrição
A função `commandArgs` é utilizada para recuperar os argumentos fornecidos na linha de comando quando um script R é executado. Essa funcionalidade é essencial para scripts que precisam de entradas dinâmicas, permitindo que usuários passem diferentes parâmetros ao executar o script.

### Uso
A função `commandArgs` pode ser chamada da seguinte forma:

```R
commandArgs(trailingOnly = FALSE)
```

- **trailingOnly**: Um argumento lógico que determina se apenas os argumentos que vêm após o nome do script devem ser retornados. O valor padrão é `FALSE`, que retorna todos os argumentos, incluindo o caminho do script.

### Detalhes
- Ao executar um script R através da linha de comando, a primeira posição do vetor de retorno incluirá o caminho do executável R, seguido pelo caminho do script e, em seguida, pelos argumentos passados.
- Se `trailingOnly` for definido como `TRUE`, a função retornará apenas os argumentos que estão após o nome do script, o que é muitas vezes desejado para facilitar a manipulação.

## Exemplos
### Exemplo Básico
Suponha que você tenha um script chamado `meu_script.R`, e você deseja passar um argumento de texto para ele. O conteúdo do script poderia ser:

```R
args <- commandArgs(trailingOnly = TRUE)
print(args)
```

Ao executar o script da seguinte forma:

```bash
Rscript meu_script.R "Olá, mundo!"
```

A saída será:

```
[1] "Olá, mundo!"
```

### Exemplo com Múltiplos Argumentos
Se você quiser passar múltiplos argumentos, como números, pode fazer assim:

```R
args <- commandArgs(trailingOnly = TRUE)
num1 <- as.numeric(args[1])
num2 <- as.numeric(args[2])
soma <- num1 + num2
print(soma)
```

E a execução seria:

```bash
Rscript meu_script.R 5 10
```

A saída será:

```
[1] 15
```

## Explicação
### Armadilhas Comuns
- **Falta de Argumentos**: Se o script for executado sem os argumentos necessários, o vetor retornado pode estar vazio ou não conter os valores esperados. É importante validar a entrada.
- **Conversão de Tipos**: Os argumentos são retornados como strings. Caso precise de um tipo numérico ou outro formato, será necessário realizar a conversão explicitamente.
- **Uso em Ambientes Diferentes**: O comportamento de `commandArgs` pode variar em diferentes ambientes de execução (RStudio, terminal, etc.), então sempre teste o script em seu ambiente pretendido.

## Resumo em Uma Linha
A função `commandArgs` em R permite acessar argumentos de linha de comando, facilitando a personalização e automação de scripts.