<!--
Meta Description: # colMeans: Cálculo de Medias por Columna en R ## Sinopsis El comando `colMeans` en R permite calcular la media de cada columna de una matriz o un dat...
Meta Keywords: medias, que, las, una, colmeans
-->

# colMeans: Cálculo de Medias por Columna en R

## Sinopsis
El comando `colMeans` en R permite calcular la media de cada columna de una matriz o un data frame, proporcionando una manera eficiente y rápida de obtener promedios en conjuntos de datos.

## Documentación
### Propósito
`colMeans` es una función que facilita la obtención de las medias de las columnas de matrices y data frames. Es especialmente útil en el análisis de datos, donde se requiere resumir información cuantitativa.

### Uso
La función tiene la siguiente sintaxis:

```R
colMeans(x, na.rm = FALSE, dims = 1)
```

#### Parámetros
- `x`: Una matriz o un data frame del cual se desean calcular las medias.
- `na.rm`: Un valor lógico que indica si se deben ignorar los valores `NA` (predeterminado es `FALSE`).
- `dims`: Un entero que indica la dimensión de las medias que se desean calcular (predeterminado es `1`, lo que significa que se calculan las medias por columnas).

### Detalles
- La función devuelve un vector con las medias de cada columna.
- Si `na.rm` es `TRUE`, los valores `NA` se omiten en el cálculo de las medias.
- La función es vectorizada, lo que significa que es eficiente incluso para grandes conjuntos de datos.

## Ejemplos
### Ejemplo Básico
```R
# Crear una matriz de ejemplo
matriz <- matrix(1:12, nrow = 3)
print(matriz)

# Calcular las medias de las columnas
medias <- colMeans(matriz)
print(medias)
```

### Ejemplo con NA
```R
# Crear una matriz con valores NA
matriz_con_na <- matrix(c(1, 2, NA, 4, 5, 6), nrow = 3)
print(matriz_con_na)

# Calcular las medias ignorando NA
medias_na <- colMeans(matriz_con_na, na.rm = TRUE)
print(medias_na)
```

## Explicación
Es importante tener en cuenta que `colMeans` solo puede ser utilizado con matrices o data frames que contengan datos numéricos. Si se intenta aplicar a un data frame que incluye factores o caracteres, puede generar un error. Además, si `na.rm` se establece en `FALSE` y existen valores `NA`, se devolverá `NA` como resultado para esa columna.

## Resumen en una línea
`colMeans` es una función de R que calcula las medias de las columnas de una matriz o data frame, permitiendo un análisis eficiente de los datos numéricos.