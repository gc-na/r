<!--
Meta Description: # pmax.int: Función de R para el Máximo Elemento por Elemento ## Sinopsis La función `pmax.int` en R es utilizada para calcular el máximo de cada elem...
Meta Keywords: vectores, pmax, int, que, los
-->

# pmax.int: Función de R para el Máximo Elemento por Elemento

## Sinopsis
La función `pmax.int` en R es utilizada para calcular el máximo de cada elemento a través de vectores. Permite comparar múltiples vectores o elementos y devolver un nuevo vector que contiene el valor máximo en cada posición correspondiente.

## Documentación

### Propósito
`pmax.int` es una función diseñada para encontrar el valor máximo entre uno o más vectores de enteros de manera eficiente. Es especialmente útil cuando se trabaja con datos en los que se necesita comparar múltiples series de valores.

### Uso
La sintaxis básica de `pmax.int` es la siguiente:

```R
pmax.int(..., na.rm = FALSE)
```

#### Parámetros
- `...`: Vectores de enteros que se compararán.
- `na.rm`: Un valor lógico que indica si se deben ignorar los valores `NA` (por defecto es `FALSE`). Si se establece en `TRUE`, los valores `NA` se omiten en el cálculo.

### Detalles
La función devuelve un vector de enteros que contiene el máximo de cada posición de los vectores de entrada. Si se proporciona un número diferente de elementos en los vectores, se reciclarán hasta que tengan la misma longitud. 

## Ejemplos

### Ejemplo Básico
```R
# Comparar dos vectores de enteros
vector1 <- c(1, 3, 5)
vector2 <- c(2, 1, 4)
resultado <- pmax.int(vector1, vector2)
print(resultado)
# Salida: [1] 2 3 5
```

### Ejemplo con NA
```R
# Comparar vectores incluyendo NA
vector1 <- c(1, NA, 5)
vector2 <- c(2, 3, 4)
resultado <- pmax.int(vector1, vector2, na.rm = TRUE)
print(resultado)
# Salida: [1] 2 3 5
```

## Explicación
**Puntos a Considerar:**
- **Reciclaje de Vectores**: Si se pasan vectores de diferentes longitudes, `pmax.int` aplicará el reciclaje, lo que puede llevar a resultados inesperados si no se tiene cuidado.
- **Manejo de NA**: Es importante gestionar correctamente los valores `NA`, ya que pueden afectar el resultado. Usar `na.rm = TRUE` puede ser útil para evitar que los `NA` influyan en el cálculo.

## Resumen en una Línea
La función `pmax.int` en R permite calcular el máximo elemento por elemento de múltiples vectores de enteros, facilitando comparaciones eficientes y efectivas.