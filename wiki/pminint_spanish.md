<!--
Meta Description: # pmin.int en R: Comando para el Mínimo Elemento por Elemento ## Sinopsis El comando `pmin.int` en R es utilizado para calcular el mínimo de elementos...
Meta Keywords: pmin, int, vectores, los, que
-->

# pmin.int en R: Comando para el Mínimo Elemento por Elemento

## Sinopsis
El comando `pmin.int` en R es utilizado para calcular el mínimo de elementos entre dos o más vectores de enteros, devolviendo un vector que contiene los valores mínimos correspondientes.

## Documentación
### Propósito
`pmin.int` forma parte de la familia de funciones de R que permiten realizar operaciones vectorizadas. Su propósito es calcular el mínimo valor entre vectores de enteros, facilitando así la comparación y la reducción de datos de manera eficiente.

### Uso
La función se utiliza de la siguiente manera:

```R
pmin.int(..., na.rm = FALSE)
```

#### Parámetros
- `...`: Uno o más vectores de enteros que se compararán entre sí.
- `na.rm`: Un valor lógico que indica si se deben ignorar los valores NA. Por defecto, es `FALSE`.

### Detalles
- La función devuelve un vector con la longitud igual al de los vectores de entrada, donde cada elemento es el mínimo correspondiente entre los vectores proporcionados.
- `pmin.int` es una variante optimizada de `pmin` para trabajar específicamente con enteros, lo que puede resultar en un mejor rendimiento en ciertas aplicaciones.

## Ejemplos
### Ejemplo 1: Comparación de dos vectores
```R
vec1 <- c(3L, 5L, 7L)
vec2 <- c(2L, 8L, 6L)
resultado <- pmin.int(vec1, vec2)
print(resultado)  # Salida: [1] 2 5 6
```

### Ejemplo 2: Comparación con NA
```R
vec1 <- c(NA, 5L, 7L)
vec2 <- c(2L, NA, 6L)
resultado <- pmin.int(vec1, vec2, na.rm = TRUE)
print(resultado)  # Salida: [1] 2 5 6
```

## Explicación
Un error común al usar `pmin.int` es no considerar el manejo de valores NA. Si `na.rm` se deja como `FALSE`, cualquier NA en los vectores de entrada resultará en un NA en el output. Por otro lado, si se desea ignorar estos valores, es importante establecer `na.rm = TRUE`.

Además, `pmin.int` es útil en situaciones donde se necesita comparar múltiples vectores. Sin embargo, todos los vectores deben tener la misma longitud; de lo contrario, R generará un error.

## Resumen en una línea
`pmin.int` es una función en R que calcula el mínimo elemento por elemento entre vectores de enteros, ignorando opcionalmente los valores NA.