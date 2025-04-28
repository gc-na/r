<!--
Meta Description: # all.equal.default en R: Comparación de Objetos ## Sinopsis `all.equal.default` es una función en R que se utiliza para comparar dos objetos y determ...
Meta Keywords: all, equal, que, objetos, función
-->

# all.equal.default en R: Comparación de Objetos

## Sinopsis
`all.equal.default` es una función en R que se utiliza para comparar dos objetos y determinar si son "iguales" en un sentido flexible, permitiendo cierta tolerancia a diferencias menores en los datos numéricos.

## Documentación
### Propósito
La función `all.equal.default` se usa principalmente para comparar objetos de R, como vectores, listas, matrices, y otros tipos de datos. Su propósito es verificar si dos objetos son equivalentes, teniendo en cuenta posibles diferencias en precisión, tolerancia a errores y otras consideraciones.

### Uso
La sintaxis básica de la función es la siguiente:

```R
all.equal(target, current, tolerance = .Machine$double.eps^0.5, ...)
```

- **target**: El objeto que se desea comparar.
- **current**: El objeto con el que se compara.
- **tolerance**: Un número que especifica la tolerancia permitida para diferencias en los valores numéricos. Por defecto, es la raíz cuadrada de la menor representación positiva de un número en la máquina (.Machine$double.eps).
- **...**: Argumentos adicionales que pueden ser utilizados por métodos específicos.

### Detalles
`all.equal.default` permite a los usuarios realizar comparaciones con tolerancia, lo que resulta útil cuando se trabaja con cálculos numéricos que pueden generar pequeñas diferencias debido a la precisión de los números de punto flotante. La función devuelve `TRUE` si los objetos son considerados iguales o una descripción de las diferencias si no lo son.

## Ejemplos
### Ejemplo 1: Comparar vectores numéricos
```R
vec1 <- c(1.000001, 2, 3)
vec2 <- c(1, 2, 3)
result <- all.equal(vec1, vec2)
print(result)  # Puede devolver "Mean relative difference: ... "
```

### Ejemplo 2: Comparar listas
```R
list1 <- list(a = 1:5, b = 2.5)
list2 <- list(a = 1:5, b = 2.50000001)
result <- all.equal(list1, list2)
print(result)  # Puede devolver TRUE si la tolerancia es suficiente
```

### Ejemplo 3: Comparar matrices
```R
mat1 <- matrix(c(1, 2, 3, 4), nrow = 2)
mat2 <- matrix(c(1, 2, 3, 4), nrow = 2)
result <- all.equal(mat1, mat2)
print(result)  # Debería devolver TRUE
```

## Explicación
Al utilizar `all.equal.default`, es importante recordar que:
- La función está diseñada para manejar comparaciones de datos donde pequeñas diferencias pueden ser irrelevantes, como en cálculos numéricos.
- Si se comparan objetos que no son de tipos compatibles, la función puede devolver un mensaje de error o advertencia.
- La tolerancia puede ajustarse según sea necesario para obtener resultados más precisos en comparación a las expectativas del usuario.

## Resumen en una línea
`all.equal.default` es una función en R que permite comparar dos objetos para verificar su igualdad con una tolerancia flexible en diferencias numéricas.