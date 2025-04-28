<!--
Meta Description: # Media en R: Cómo Calcular Promedios de Datos ## Sinopsis El comando `mean()` en R se utiliza para calcular el promedio aritmético de un conjunto de ...
Meta Keywords: datos, mean, calcular, valores, que
-->

# Media en R: Cómo Calcular Promedios de Datos

## Sinopsis
El comando `mean()` en R se utiliza para calcular el promedio aritmético de un conjunto de valores numéricos, lo que lo convierte en una herramienta fundamental para el análisis estadístico en R.

## Documentación
### Propósito
La función `mean()` tiene como objetivo calcular el promedio aritmético de un vector numérico. Es una de las funciones más utilizadas en R para resumir y analizar datos.

### Uso
La sintaxis básica de la función es la siguiente:

```R
mean(x, na.rm = FALSE, trim = 0)
```

#### Parámetros
- **x**: Un vector numérico o un objeto que puede ser convertido a un vector numérico.
- **na.rm**: Un valor lógico que indica si se deben eliminar (TRUE) o no (FALSE) los valores `NA` (no disponibles) del cálculo. Por defecto es FALSE.
- **trim**: Un valor numérico que especifica la fracción de los datos que se deben eliminar de ambos extremos antes de calcular la media. Por defecto es 0, lo que significa que no se eliminan datos.

### Detalles
La función `mean()` es especialmente útil para manejar grandes conjuntos de datos y permite obtener un resumen rápido del comportamiento central de los datos. Asegúrese de considerar el parámetro `na.rm` si su conjunto de datos contiene valores faltantes.

## Ejemplos
### Ejemplo 1: Calcular la media de un vector simple
```R
datos <- c(10, 20, 30, 40, 50)
promedio <- mean(datos)
print(promedio)  # Salida: 30
```

### Ejemplo 2: Calcular la media ignorando valores NA
```R
datos_con_na <- c(10, 20, NA, 40, 50)
promedio_sin_na <- mean(datos_con_na, na.rm = TRUE)
print(promedio_sin_na)  # Salida: 30
```

### Ejemplo 3: Calcular la media con recorte
```R
datos_recortados <- c(1, 2, 3, 4, 100)
promedio_recortado <- mean(datos_recortados, trim = 0.2)
print(promedio_recortado)  # Salida: 3
```

## Explicación
Al utilizar la función `mean()`, es importante tener en cuenta algunos aspectos:
- **Valores NA**: Si no se especifica `na.rm = TRUE`, cualquier valor `NA` en el vector resultará en un resultado `NA` para la media.
- **Recorte**: El parámetro `trim` puede ser útil para eliminar valores extremos que puedan sesgar el promedio.

## Resumen en Una Línea
La función `mean()` en R permite calcular el promedio aritmético de un conjunto de valores numéricos, con opciones para manejar valores faltantes y recortar datos extremos.