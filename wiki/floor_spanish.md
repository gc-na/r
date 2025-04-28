<!--
Meta Description: # Función Floor en R: Redondeo hacia Abajo ## Sinopsis La función `floor` en R se utiliza para redondear números hacia abajo al entero más cercano. Es...
Meta Keywords: floor, función, hacia, abajo, redondear
-->

# Función Floor en R: Redondeo hacia Abajo

## Sinopsis
La función `floor` en R se utiliza para redondear números hacia abajo al entero más cercano. Es especialmente útil en análisis de datos donde se requiere manipular valores numéricos sin alterar su parte entera.

## Documentación

### Propósito
La función `floor` redondea un número real hacia el entero más bajo. Esto significa que cualquier valor decimal se elimina, dejando solo la parte entera del número.

### Uso
La sintaxis básica de la función es la siguiente:

```R
floor(x)
```

#### Parámetros
- `x`: Un valor numérico o un vector numérico que se desea redondear hacia abajo.

### Detalles
La función `floor` es parte de las funciones básicas de R y no requiere la carga de paquetes adicionales. Puede aplicarse a vectores, y en este caso, devolverá un vector con el mismo número de elementos, donde cada elemento ha sido redondeado hacia abajo.

## Ejemplos

### Ejemplo 1: Uso básico
```R
# Redondear un número simple
resultado <- floor(3.7)
print(resultado)  # Salida: 3
```

### Ejemplo 2: Aplicación en vectores
```R
# Redondear un vector de números
numeros <- c(1.2, 2.5, 3.8, 4.0)
resultado_vector <- floor(numeros)
print(resultado_vector)  # Salida: 1 2 3 4
```

### Ejemplo 3: Uso con números negativos
```R
# Redondear un número negativo
resultado_negativo <- floor(-2.3)
print(resultado_negativo)  # Salida: -3
```

## Explicación
Al usar `floor`, es importante tener en cuenta que la función siempre redondea hacia el entero más bajo. Esto puede ser confuso para algunos usuarios, especialmente cuando se trabaja con números negativos. Por ejemplo, `floor(-1.5)` regresará `-2`, no `-1`. 

Además, la función `floor` puede ser utilizada junto con otras funciones de manipulación de datos, pero no debe confundirse con `ceiling`, que redondea hacia arriba, o `round`, que redondea al entero más cercano basándose en el valor decimal.

## Resumen en Una Línea
La función `floor` en R redondea números hacia abajo al entero más cercano, siendo útil para la manipulación precisa de datos numéricos.