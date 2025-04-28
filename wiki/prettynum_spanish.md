<!--
Meta Description: # prettyNum: Formateo de Números en R para una Presentación Atractiva ## Sinopsis El comando `prettyNum` en R se utiliza para formatear números de man...
Meta Keywords: que, prettynum, mark, para, como
-->

# prettyNum: Formateo de Números en R para una Presentación Atractiva

## Sinopsis
El comando `prettyNum` en R se utiliza para formatear números de manera que sean más legibles y visualmente atractivos, facilitando la presentación de datos en informes y gráficos.

## Documentación
### Propósito
`prettyNum` tiene como objetivo mejorar la legibilidad de los números en R, permitiendo personalizar su presentación, como agregar comas como separadores de miles, redondear decimales, o incluso agregar prefijos y sufijos.

### Uso
La función `prettyNum` se utiliza de la siguiente manera:

```R
prettyNum(x, big.mark = ",", decimal.mark = ".", scientific = FALSE, ...)
```

#### Argumentos
- `x`: Un vector numérico que se desea formatear.
- `big.mark`: Un carácter que se usa como separador de miles (por defecto es una coma).
- `decimal.mark`: Un carácter que se utiliza como separador decimal (por defecto es un punto).
- `scientific`: Un valor lógico que determina si se debe usar notación científica (por defecto es FALSE).
- `...`: Argumentos adicionales que se pueden pasar a la función.

### Detalles
`prettyNum` es útil en la visualización de datos, especialmente cuando se presentan grandes volúmenes de información numérica. La función permite la personalización del formato, lo cual es crucial para hacer que los datos sean más accesibles y comprensibles para los usuarios finales.

## Ejemplos
### Ejemplo Básico
```R
# Formatear un número simple
n <- 1234567.89
prettyNum(n)
# Resultado: "1,234,567.89"
```

### Ejemplo con Separadores Personalizados
```R
# Usar un espacio como separador de miles
prettyNum(n, big.mark = " ")
# Resultado: "1 234 567.89"
```

### Ejemplo con Notación Científica
```R
# Activar la notación científica
prettyNum(123456789, scientific = TRUE)
# Resultado: "1.23456789e+08"
```

## Explicación
Al usar `prettyNum`, es importante tener en cuenta que los resultados son de tipo carácter, lo que significa que no se pueden usar directamente en cálculos sin convertirlos de nuevo a formato numérico. Además, el uso de `big.mark` y `decimal.mark` puede variar según la localización y las preferencias del usuario.

### Errores Comunes
- **No convertir de carácter a numérico**: Al formatear números, si se necesita realizar cálculos posteriores, se debe tener en cuenta la conversión de nuevo a tipo numérico.
- **Confusión con el formato regional**: Asegúrese de utilizar el separador decimal y de miles que sea apropiado para su localización, ya que puede variar entre diferentes culturas.

## Resumen en una Línea
`prettyNum` es una función de R que permite formatear números para mejorar su legibilidad y presentación en informes y gráficos.