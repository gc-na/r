<!--
Meta Description: # file.info: Comando R para Obter Informações de Arquivos ## Sinopse O comando `file.info` em R é utilizado para obter informações detalhadas sobre ar...
Meta Keywords: arquivos, info, file, informações, data
-->

# file.info: Comando R para Obter Informações de Arquivos

## Sinopse
O comando `file.info` em R é utilizado para obter informações detalhadas sobre arquivos, como tamanho, permissões, data de modificação, entre outros, facilitando a análise de arquivos no sistema.

## Documentação
### Propósito
O `file.info` serve para coletar informações sobre um ou mais arquivos, retornando um data frame com detalhes relevantes que podem auxiliar na gestão e análise de arquivos em projetos de programação e análise de dados.

### Uso
A função é utilizada da seguinte maneira:

```R
file.info(basename)
```

#### Argumentos
- `basename`: Um vetor de caracteres com os nomes dos arquivos ou diretórios para os quais se deseja obter informações.

### Detalhes
O resultado de `file.info` é um data frame com as seguintes colunas:
- `size`: Tamanho do arquivo em bytes.
- `isdir`: Indica se o caminho especificado é um diretório (TRUE ou FALSE).
- `mode`: Permissões do arquivo em formato octal.
- `mtime`: Data e hora da última modificação do arquivo.
- `ctime`: Data e hora da última alteração na estrutura do arquivo.
- `atime`: Data e hora da última leitura do arquivo.

## Exemplos
### Exemplo Básico
Obter informações de um único arquivo:

```R
info <- file.info("exemplo.txt")
print(info)
```

### Múltiplos Arquivos
Obter informações de vários arquivos:

```R
arquivos <- c("exemplo.txt", "dados.csv", "script.R")
info_multiplos <- file.info(arquivos)
print(info_multiplos)
```

### Verificando Diretórios
Verificar se um caminho é um diretório:

```R
info_diretorio <- file.info("meu_diretorio")
print(info_diretorio$isdir)
```

## Explicação
É importante notar que o `file.info` pode retornar NA para arquivos que não existem ou que não podem ser acessados devido a permissões. Além disso, o comportamento pode variar conforme o sistema operacional (Windows, Linux, macOS), então é recomendável validar os caminhos dos arquivos antes de utilizá-los na função.

## Resumo em Uma Linha
O comando `file.info` em R fornece um data frame com informações detalhadas sobre arquivos e diretórios, facilitando sua análise e gerenciamento.