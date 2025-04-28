<!--
Meta Description: # loadedNamespaces: Verificando os Namespaces Carregados em R ## Sinopse O comando `loadedNamespaces` em R permite verificar quais namespaces de pacot...
Meta Keywords: namespaces, pacotes, loadednamespaces, carregados, que
-->

# loadedNamespaces: Verificando os Namespaces Carregados em R

## Sinopse
O comando `loadedNamespaces` em R permite verificar quais namespaces de pacotes estão carregados na sessão atual, oferecendo uma visão clara dos pacotes que estão disponíveis para uso.

## Documentação
O `loadedNamespaces` é uma função da linguagem R que retorna uma lista de todos os namespaces dos pacotes que foram carregados na sessão atual. Isto é especialmente útil para desenvolvedores e analistas que desejam entender o ambiente de trabalho no qual estão operando, permitindo uma melhor gestão de dependências e evitando conflitos entre pacotes.

### Uso
A sintaxe básica é:

```R
loadedNamespaces()
```

### Detalhes
- **Retorno**: A função retorna um vetor de caracteres contendo os nomes dos namespaces que estão atualmente carregados.
- **Contexto**: É importante notar que os namespaces são diferentes dos pacotes carregados; um pacote pode ser carregado e não estar em uso, mas seu namespace ainda estará disponível.

## Exemplos

### Exemplo 1: Listar Namespaces Carregados
```R
# Carregando alguns pacotes
library(ggplot2)
library(dplyr)

# Verificando os namespaces carregados
namespaces_carregados <- loadedNamespaces()
print(namespaces_carregados)
```

### Exemplo 2: Verificar Namespaces Após Carregar Pacotes
```R
# Carregando mais pacotes
library(tidyr)

# Listando novamente os namespaces
namespaces_carregados <- loadedNamespaces()
print(namespaces_carregados)
```

## Explicação
Um dos erros comuns ao usar `loadedNamespaces` é não entender que ele apenas lista namespaces e não pacotes carregados. Por exemplo, se um pacote não foi carregado com `library()`, seu namespace não aparecerá na lista. Além disso, namespaces podem conter funções e objetos que, mesmo não visíveis diretamente, podem ser utilizados com o operador `::`.

### Observações Adicionais
- Evite confundir `loadedNamespaces` com `search()`, que lista os pacotes na busca do R, não os namespaces.
- Esta função é particularmente útil em ambientes de desenvolvimento e depuração, onde a gestão de pacotes é crítica.

## Resumo em Uma Linha
O `loadedNamespaces` permite listar os namespaces de pacotes carregados na sessão atual do R, facilitando a gestão de dependências e o entendimento do ambiente de trabalho.