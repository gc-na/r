<!--
Meta Description: # all.equal.numeric: Comparación de Números en R ## Sinopsis `all.equal.numeric` es una función en R que permite comparar dos vectores numéricos para ...
Meta Keywords: all, equal, numeric, que, números
-->

# all.equal.numeric: Comparación de Números en R

## Sinopsis
`all.equal.numeric` es una función en R que permite comparar dos vectores numéricos para determinar si son aproximadamente iguales, considerando tolerancias en la comparación.

## Documentación
La función `all.equal.numeric` es parte de la función `all.equal`, diseñada específicamente para comparar objetos numéricos en R. Su propósito principal es evaluar si dos números son iguales dentro de un margen de error definido, lo cual es especialmente útil en análisis numérico y computacional donde los errores de redondeo pueden afectar los resultados.

### Uso
```R
all.equal.numeric(target, current, tolerance = .Machine$double.eps^0.5, ...)
```

- **target**: El primer número a comparar.
- **current**: El segundo número a comparar.
- **tolerance**: Un valor numérico que define el margen de error aceptable. Por defecto, se utiliza la raíz cuadrada del valor más pequeño representable en el sistema.
- **...**: Argumentos adicionales que pueden ser pasados a la función.

### Detalles
`all.equal.numeric` devuelve `TRUE` si los números son aproximadamente iguales dentro del rango de tolerancia especificado. Si no son iguales, devuelve un mensaje que describe la discrepancia.

## Ejemplos
### Ejemplo 1: Comparación Exacta
```R
resultado1 <- all.equal.numeric(3.14, 3.14)
print(resultado1)  # TRUE
```

### Ejemplo 2: Comparación con Tolerancia
```R
resultado2 <- all.equal.numeric(3.14, 3.14159)
print(resultado2)  # "Mean relative difference: ..."
```

### Ejemplo 3: Uso de Tolerancia Personalizada
```R
resultado3 <- all.equal.numeric(1.00001, 1, tolerance = 1e-5)
print(resultado3)  # TRUE
```

## Explicación
Es importante tener en cuenta que `all.equal.numeric` no considera dos números como iguales si la diferencia entre ellos excede la tolerancia especificada. Esto puede llevar a resultados inesperados si no se establece adecuadamente el parámetro de tolerancia. También es crucial recordar que esta función está diseñada para ser utilizada con números, y su comportamiento puede diferir si se aplica a otros tipos de datos.

## Resumen en Una Línea
`all.equal.numeric` en R es una función que compara dos números para verificar si son aproximadamente iguales dentro de un margen de tolerancia definido.