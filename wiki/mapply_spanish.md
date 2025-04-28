<!--
Meta Description: # mapply: Función de Aplicación Múltiple en R ## Sinopsis La función `mapply` en R permite aplicar una función a múltiples argumentos en paralelo, fac...
Meta Keywords: mapply, función, que, una, los
-->

# mapply: Función de Aplicación Múltiple en R

## Sinopsis
La función `mapply` en R permite aplicar una función a múltiples argumentos en paralelo, facilitando la manipulación y transformación de datos de forma eficiente.

## Documentación
### Propósito
`mapply` es una función que combina la funcionalidad de `sapply` y `lapply`, permitiendo aplicar una función a varios vectores o listas al mismo tiempo. Es especialmente útil cuando se necesita realizar operaciones que requieren múltiples entradas.

### Uso
La sintaxis básica de `mapply` es la siguiente:

```R
mapply(FUN, ..., MoreArgs = NULL, SIMPLIFY = TRUE, USE.NAMES = TRUE)
```

#### Argumentos
- **FUN**: La función que se desea aplicar.
- **...**: Los vectores o listas a los que se aplicará la función.
- **MoreArgs**: Argumentos adicionales que se pasan a la función.
- **SIMPLIFY**: Un valor lógico que indica si se debe simplificar el resultado a un vector o lista.
- **USE.NAMES**: Un valor lógico que indica si se deben usar los nombres de los argumentos.

### Detalles
`mapply` es particularmente útil cuando la función que se aplica requiere más de un argumento. La función toma los elementos de los vectores de entrada de manera paralela, creando combinaciones de estos elementos.

## Ejemplos
### Ejemplo 1: Sumar dos vectores
```R
a <- c(1, 2, 3)
b <- c(4, 5, 6)
resultado <- mapply(sum, a, b)
print(resultado)  # Salida: 5 7 9
```

### Ejemplo 2: Concatenar cadenas
```R
nombre <- c("Juan", "Ana", "Luis")
apellido <- c("Pérez", "García", "López")
resultado <- mapply(function(n, a) paste(n, a), nombre, apellido)
print(resultado)  # Salida: "Juan Pérez" "Ana García" "Luis López"
```

### Ejemplo 3: Aplicar una función personalizada
```R
mi_funcion <- function(x, y) {
  return(x^y)
}
resultado <- mapply(mi_funcion, a, b)
print(resultado)  # Salida: 1 32 729
```

## Explicación
Al utilizar `mapply`, es importante tener en cuenta que todos los vectores deben tener la misma longitud. Si no es así, R aplicará reciclaje, lo que puede llevar a resultados inesperados. Además, si se utilizan listas como entrada, `mapply` desglosará automáticamente los elementos de la lista.

Una trampa común es olvidar que `mapply` devuelve un objeto simplificado por defecto. Si se desea mantener la estructura original, asegúrate de establecer `SIMPLIFY = FALSE`.

## Resumen en Una Línea
`mapply` es una función en R que permite aplicar una función a múltiples vectores o listas de forma eficiente y paralela.