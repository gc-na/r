<!--
Meta Description: # is.numeric: Verifica si un objeto es numérico en R ## Sinopsis La función `is.numeric` en R se utiliza para determinar si un objeto es de tipo numér...
Meta Keywords: numeric, que, objeto, numérico, función
-->

# is.numeric: Verifica si un objeto es numérico en R

## Sinopsis
La función `is.numeric` en R se utiliza para determinar si un objeto es de tipo numérico. Esta función es fundamental para la validación y manipulación de datos, permitiendo a los usuarios asegurarse de que los elementos de un vector, lista o dataframe cumplen con los criterios esperados para su análisis.

## Documentación
### Propósito
La función `is.numeric` evalúa si un objeto en R es numérico, lo que incluye tanto números enteros como de punto flotante. Esta verificación es esencial en el manejo de datos, especialmente cuando se requiere realizar operaciones matemáticas o estadísticas.

### Uso
```R
is.numeric(x)
```
- **x**: Un objeto R que se quiere verificar. Puede ser un vector, lista, dataframe, entre otros.

### Detalles
- La función devuelve `TRUE` si el objeto es numérico y `FALSE` en caso contrario.
- `is.numeric` es útil en la limpieza de datos, ya que permite filtrar o transformar datos basados en su tipo.
- Es importante diferenciar entre `is.numeric` y otras funciones similares como `is.integer`, que solo verifica si un objeto es un entero.

## Ejemplos
### Ejemplo básico 1: Verificación de un vector numérico
```R
vec <- c(1, 2, 3.5)
is.numeric(vec)  # Devuelve TRUE
```

### Ejemplo básico 2: Verificación de una lista
```R
lista <- list(a = 1, b = "texto")
is.numeric(lista)  # Devuelve FALSE
```

### Ejemplo básico 3: Verificación de un dataframe
```R
df <- data.frame(col1 = c(1, 2, 3), col2 = c("a", "b", "c"))
is.numeric(df$col1)  # Devuelve TRUE
is.numeric(df$col2)  # Devuelve FALSE
```

## Explicación
- **Errores comunes**: Un error común es asumir que un objeto es numérico solo porque contiene números en formato de texto. Por ejemplo, `is.numeric("123")` devolverá `FALSE` ya que es una cadena de texto, no un número.
- **Diferenciación de tipos**: Es importante recordar que `is.numeric` no distingue entre enteros y números de punto flotante, mientras que `is.integer` solo devuelve `TRUE` para objetos de tipo entero.
- **Uso en condiciones**: Esta función es frecuentemente utilizada en condicionales para ejecutar diferentes bloques de código dependiendo del tipo de datos.

## Resumen en una línea
La función `is.numeric` en R se utiliza para verificar si un objeto es numérico, devolviendo `TRUE` o `FALSE` según el tipo de dato.