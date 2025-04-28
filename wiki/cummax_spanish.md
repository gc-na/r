<!--
Meta Description: # Función cummax en R: Calculo del Máximo Acumulado ## Sinopsis La función `cummax` en R es utilizada para calcular el máximo acumulado de un vector o...
Meta Keywords: vector, cummax, máximo, función, acumulado
-->

# Función cummax en R: Calculo del Máximo Acumulado

## Sinopsis
La función `cummax` en R es utilizada para calcular el máximo acumulado de un vector o una serie de datos. Esta función es fundamental en análisis de series temporales y otras aplicaciones donde se requiere identificar el valor máximo en un conjunto de datos en una secuencia acumulativa.

## Documentación
### Propósito
La función `cummax` tiene como objetivo proporcionar el máximo acumulado de sus elementos en un vector, devolviendo un vector del mismo tamaño que el original. Es útil en análisis de datos donde se desea entender la tendencia máxima hasta cada punto de un conjunto de datos.

### Uso
La sintaxis de la función es la siguiente:

```R
cummax(x)
```

#### Parámetros
- `x`: Un vector numérico, que puede ser un vector simple o un objeto que se puede convertir a un vector.

#### Detalles
- La función `cummax` evalúa los elementos de `x` en el orden en que aparecen y calcula el máximo acumulado en cada posición del vector.
- El resultado es un vector de la misma longitud que `x`, donde cada elemento representa el máximo de todos los elementos anteriores en `x`, incluido el elemento actual.

## Ejemplos
### Ejemplo 1: Uso básico de cummax
```R
# Definir un vector numérico
vec <- c(1, 3, 2, 5, 4)

# Calcular el máximo acumulado
max_acumulado <- cummax(vec)

# Mostrar el resultado
print(max_acumulado)
```
**Salida:**
```
[1] 1 3 3 5 5
```

### Ejemplo 2: Vector con números negativos
```R
# Definir un vector con elementos negativos
vec_neg <- c(-1, -3, -2, -5, -4)

# Calcular el máximo acumulado
max_acum_neg <- cummax(vec_neg)

# Mostrar el resultado
print(max_acum_neg)
```
**Salida:**
```
[1] -1 -1 -1 -1 -1
```

### Ejemplo 3: Vector con cero
```R
# Definir un vector que incluye cero
vec_cero <- c(0, 2, 0, 3, 1)

# Calcular el máximo acumulado
max_acum_cero <- cummax(vec_cero)

# Mostrar el resultado
print(max_acum_cero)
```
**Salida:**
```
[1] 0 2 2 3 3
```

## Explicación
Al usar `cummax`, es importante tener en cuenta que:
- La función no altera el vector original; en su lugar, devuelve un nuevo vector con los máximos acumulados.
- Si se introducen elementos no numéricos en el vector, la función generará un error.
- En el caso de series temporales, `cummax` es particularmente útil para identificar picos o máximos históricos en los datos.

## Resumen en una Frase
La función `cummax` en R calcula el máximo acumulado de un vector, devolviendo un nuevo vector que representa el máximo hasta cada punto del original.