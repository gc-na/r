<!--
Meta Description: # Duplicados en R: Función `duplicated.default` ## Sinopsis La función `duplicated.default` en R se utiliza para identificar elementos duplicados en u...
Meta Keywords: duplicados, vector, función, duplicated, que
-->

# Duplicados en R: Función `duplicated.default`

## Sinopsis
La función `duplicated.default` en R se utiliza para identificar elementos duplicados en un vector. Esta función es fundamental para la limpieza y el análisis de datos, ya que permite detectar y manejar registros redundantes.

## Documentación
### Propósito
La función `duplicated.default` forma parte del sistema de manejo de datos en R y se utiliza para señalar la presencia de elementos duplicados dentro de un vector. Es especialmente útil en situaciones donde es necesario asegurar la unicidad de los datos antes de realizar análisis estadísticos o visualizaciones.

### Uso
La sintaxis básica de la función es:

```R
duplicated(x)
```

#### Parámetros
- `x`: Un vector o un objeto que puede ser convertido en un vector.

#### Detalles
La función devuelve un vector lógico del mismo tamaño que `x`, donde cada elemento indica si el correspondiente elemento en `x` es un duplicado de un elemento anterior. El primer caso de cada conjunto de duplicados se marca como `FALSE`, mientras que los duplicados posteriores se marcan como `TRUE`.

## Ejemplos
### Ejemplo 1: Uso básico
```R
# Definir un vector con duplicados
vector <- c(1, 2, 2, 3, 4, 4, 4, 5)

# Identificar duplicados
duplicados <- duplicated(vector)

# Mostrar resultado
print(duplicados)
```
**Salida:**
```
[1] FALSE FALSE  TRUE FALSE FALSE  TRUE  TRUE FALSE
```

### Ejemplo 2: Aplicación en un data frame
```R
# Crear un data frame
datos <- data.frame(id = c(1, 1, 2, 3, 3), valor = c("A", "A", "B", "C", "C"))

# Identificar duplicados en la columna 'id'
duplicados_id <- duplicated(datos$id)

# Mostrar resultado
print(duplicados_id)
```
**Salida:**
```
[1] FALSE  TRUE FALSE FALSE  TRUE
```

## Explicación
Un punto a tener en cuenta al utilizar `duplicated.default` es que la función solo señala duplicados en base a la posición anterior en el vector. Esto significa que si los elementos están desordenados, es posible que no se reconozcan como duplicados. Además, esta función es sensible al tipo de datos; por ejemplo, `1` y `1L` se consideran diferentes. 

Otro aspecto importante es que `duplicated.default` no modifica el vector original, simplemente devuelve un indicador de duplicados. Para eliminar los duplicados, se puede combinar con la función `unique()`.

## Resumen en una línea
La función `duplicated.default` en R identifica elementos duplicados en un vector, devolviendo un vector lógico que indica la presencia de duplicados.