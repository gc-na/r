<!--
Meta Description: # merge.data.frame: Cómo combinar data frames en R ## Sinopsis La función `merge.data.frame` en R permite combinar dos data frames basándose en column...
Meta Keywords: data, frames, all, merge, las
-->

# merge.data.frame: Cómo combinar data frames en R

## Sinopsis
La función `merge.data.frame` en R permite combinar dos data frames basándose en columnas o filas comunes, facilitando la unificación de conjuntos de datos para análisis más complejos.

## Documentación
### Propósito
La función `merge` se utiliza para unir dos data frames en R. Es especialmente útil cuando se trabaja con bases de datos que comparten una o más claves. Esta operación es fundamental en análisis de datos, ya que permite consolidar información dispersa en diferentes tablas.

### Uso
La sintaxis básica de la función es:

```R
merge(x, y, by = NULL, by.x = NULL, by.y = NULL, all = FALSE, all.x = FALSE, all.y = FALSE, sort = TRUE, suffixes = c(".x", ".y"), ...)
```

#### Argumentos
- **x, y**: Los data frames a combinar.
- **by**: Columnas o nombres de filas en los que se basará la fusión. Si es NULL, se utilizarán las columnas comunes.
- **by.x, by.y**: Especifican columnas a usar en `x` e `y` si no son las mismas.
- **all**: Si se establece en TRUE, devuelve todas las filas de ambos data frames. 
- **all.x**: Si es TRUE, se devuelven todas las filas de `x`, incluso si no hay coincidencias en `y`.
- **all.y**: Similar a `all.x`, pero para `y`.
- **sort**: Si es TRUE (predeterminado), las filas se ordenan por las claves.
- **suffixes**: Un vector de longitud 2 que especifica sufijos que se agregarán a las columnas que se duplican en ambos data frames.
- **...**: Argumentos adicionales que se pueden pasar a `merge`.

### Detalles
La función `merge` realiza un "join" tipo SQL sobre los data frames, permitiendo diferentes tipos de combinaciones (inner, outer, left, right) según los parámetros `all`, `all.x`, y `all.y`. Es importante tener en cuenta que las columnas usadas para la combinación deben estar en el mismo formato y tipo.

## Ejemplos
### Ejemplo básico de combinación
```R
# Crear dos data frames de ejemplo
df1 <- data.frame(id = 1:3, nombre = c("Ana", "Luis", "Pedro"))
df2 <- data.frame(id = 2:4, edad = c(23, 34, 29))

# Combinar los data frames por la columna 'id'
resultado <- merge(df1, df2, by = "id")
print(resultado)
```

### Ejemplo de combinación externa
```R
# Combinar los data frames con una combinación externa
resultado_externo <- merge(df1, df2, by = "id", all = TRUE)
print(resultado_externo)
```

## Explicación
Al utilizar `merge`, es común encontrarse con problemas si las columnas clave tienen diferentes tipos de datos (por ejemplo, `integer` vs. `character`). Además, si no se especifican correctamente los parámetros `by`, `by.x`, y `by.y`, se pueden obtener resultados inesperados o perder información. Siempre es recomendable hacer una revisión previa de los data frames para asegurarse de que las columnas clave estén alineadas.

## Resumen en una línea
La función `merge.data.frame` en R permite combinar data frames eficientemente basándose en columnas comunes, facilitando la integración de datos para análisis más profundos.