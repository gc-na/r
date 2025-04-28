<!--
Meta Description: # is.finite: Verificación de valores finitos en R ## Sinopsis El comando `is.finite` en R se utiliza para determinar si un valor o conjunto de valores...
Meta Keywords: que, finite, valores, inf, son
-->

# is.finite: Verificación de valores finitos en R

## Sinopsis
El comando `is.finite` en R se utiliza para determinar si un valor o conjunto de valores son finitos, lo que significa que no son infinitos o `NA` (no disponibles). Este comando es esencial para la limpieza de datos y para asegurar que las operaciones matemáticas se realicen solo sobre valores válidos.

## Documentación
### Propósito
La función `is.finite` sirve para identificar elementos en un vector que son finitos. Los valores que son infinitos (`Inf`, `-Inf`) o que son `NA` son considerados no finitos. Esta función es particularmente útil en análisis de datos y preprocesamiento, donde es crucial trabajar con valores numéricos válidos.

### Uso
La sintaxis básica de la función es la siguiente:

```R
is.finite(x)
```

#### Parámetros
- `x`: un objeto que puede ser un vector, lista o matriz. Este objeto se evaluará para determinar qué elementos son finitos.

#### Valor de retorno
La función devuelve un vector lógico del mismo tamaño que `x`, donde cada elemento es `TRUE` si el valor correspondiente en `x` es finito y `FALSE` en caso contrario.

### Detalles
- Los valores finitos son aquellos que no son `Inf`, `-Inf`, o `NA`.
- La función opera de manera element-wise, es decir, se aplica a cada elemento del objeto `x`.

## Ejemplos
Aquí se presentan algunos ejemplos básicos del uso de `is.finite`:

```R
# Ejemplo 1: Vector simple
valores <- c(1, 2, Inf, -Inf, NA, 3.5)
resultado <- is.finite(valores)
print(resultado)
# Salida: TRUE TRUE FALSE FALSE FALSE TRUE

# Ejemplo 2: Matriz
matriz <- matrix(c(1, 2, Inf, 4, NA, -Inf), nrow=2)
resultado_matriz <- is.finite(matriz)
print(resultado_matriz)
# Salida: 
#      [,1]  [,2]
# [1,]  TRUE  TRUE
# [2,] FALSE FALSE
```

## Explicación
### Problemas comunes
- **Valores `NA`**: Recuerda que `NA` no es considerado finito. Si estás trabajando con datos que contienen `NA`, es importante manejar estos casos antes de realizar análisis.
- **Tipo de datos**: `is.finite` solo puede aplicarse a vectores numéricos. Si se pasa un tipo de dato no numérico, la función devolverá un valor lógico de `FALSE`.

### Notas adicionales
- Puedes combinar `is.finite` con otras funciones como `sum`, `mean`, etc., para realizar cálculos solamente sobre los valores finitos de un conjunto de datos.

## Resumen en una línea
La función `is.finite` en R permite identificar elementos finitos en un vector, excluyendo `Inf`, `-Inf` y `NA`.