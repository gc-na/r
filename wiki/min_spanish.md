<!--
Meta Description: # Función `min` en R: Encuentra el Valor Mínimo de un Conjunto de Datos ## Sinopsis La función `min` en R se utiliza para calcular el valor mínimo en ...
Meta Keywords: min, función, valores, datos, mínimo
-->

# Función `min` en R: Encuentra el Valor Mínimo de un Conjunto de Datos

## Sinopsis
La función `min` en R se utiliza para calcular el valor mínimo en un conjunto de datos. Es fundamental en el análisis de datos, ya que permite identificar el menor valor en vectores, listas, y otros tipos de datos.

## Documentación
### Propósito
La función `min` permite obtener el valor más pequeño de un conjunto de números. Es útil en diversas aplicaciones, como estadísticas descriptivas, análisis de datos y procesamiento de datos.

### Uso
La sintaxis básica de la función `min` es la siguiente:

```R
min(..., na.rm = FALSE)
```

#### Parámetros
- `...`: Uno o más vectores numéricos. Se pueden introducir múltiples argumentos separados por comas.
- `na.rm`: Un argumento lógico que indica si se deben ignorar los valores `NA` (por defecto es `FALSE`). Si se establece en `TRUE`, los valores `NA` no se consideran en la búsqueda del mínimo.

### Detalles
- La función `min` puede trabajar con vectores, listas y matrices.
- Si todos los valores son `NA` y `na.rm` es `FALSE`, el resultado será `NA`.
- Para conjuntos vacíos, la función también devuelve `NA`.

## Ejemplos
### Ejemplo Básico
```R
# Calcular el mínimo de un vector
valores <- c(3, 5, 2, 8, 1)
valor_minimo <- min(valores)
print(valor_minimo)  # Salida: 1
```

### Ignorar Valores NA
```R
# Calcular el mínimo ignorando NA
valores_con_na <- c(3, NA, 2, 8, 1)
valor_minimo_sin_na <- min(valores_con_na, na.rm = TRUE)
print(valor_minimo_sin_na)  # Salida: 1
```

### Múltiples Argumentos
```R
# Mínimo de múltiples vectores
vector1 <- c(10, 20, 30)
vector2 <- c(5, 15, 25)
valor_minimo_multiple <- min(vector1, vector2)
print(valor_minimo_multiple)  # Salida: 5
```

## Explicación
### Errores Comunes
- **Uso de `NA` sin `na.rm`:** Si se pasan valores `NA` sin establecer `na.rm = TRUE`, el resultado será `NA`, lo que puede ser confuso.
- **Conjuntos Vacíos:** Si se llama a `min` sin argumentos, se generará un aviso y el resultado será `NA`.

### Notas Adicionales
- La función `min` es parte de la base de R y no requiere paquetes adicionales.
- Es importante considerar el tipo de datos que se está pasando a la función, ya que valores no numéricos pueden dar lugar a errores.

## Resumen en Una Línea
La función `min` en R se utiliza para encontrar el valor más pequeño en un conjunto de datos, permitiendo la opción de ignorar valores `NA`.