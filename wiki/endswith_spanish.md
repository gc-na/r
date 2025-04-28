<!--
Meta Description: # endsWith: Función en R para Verificar Sufijos de Cadenas ## Sinopsis La función `endsWith` en R permite verificar si un vector de cadenas de texto t...
Meta Keywords: endswith, función, vector, con, true
-->

# endsWith: Función en R para Verificar Sufijos de Cadenas

## Sinopsis
La función `endsWith` en R permite verificar si un vector de cadenas de texto termina con un sufijo específico. Esta función es útil en la manipulación de cadenas y en la limpieza de datos.

## Documentación
### Propósito
`endsWith` es una función que se utiliza para determinar si los elementos de un vector de caracteres terminan con una cadena determinada. Esto es especialmente útil en situaciones donde se necesita filtrar o validar datos basados en sufijos.

### Uso
La función se utiliza de la siguiente manera:

```R
endsWith(x, suffix)
```

#### Parámetros
- `x`: Un vector de caracteres.
- `suffix`: Una cadena de caracteres que se desea verificar como sufijo.

#### Detalles
`endsWith` devuelve un vector lógico del mismo tamaño que `x`, donde cada elemento indica si el correspondiente elemento de `x` termina o no con el `suffix` especificado.

## Ejemplos
A continuación se presentan algunos ejemplos básicos de uso de la función `endsWith`:

```R
# Ejemplo 1: Verificar sufijos
vector <- c("manzana", "banana", "naranja", "fresa")
resultado <- endsWith(vector, "ana")
print(resultado) # Imprime: TRUE FALSE TRUE FALSE

# Ejemplo 2: Uso con un sufijo diferente
resultado2 <- endsWith(vector, "a")
print(resultado2) # Imprime: TRUE TRUE FALSE TRUE
```

## Explicación
Algunos puntos importantes a considerar al utilizar `endsWith`:

- **Sensibilidad a mayúsculas y minúsculas**: La función distingue entre mayúsculas y minúsculas. Por ejemplo, `endsWith("Texto", "texto")` devolverá `FALSE`.
- **Sufijos vacíos**: Si el `suffix` está vacío, `endsWith` devolverá `TRUE` para todos los elementos, ya que todas las cadenas "terminan" con una cadena vacía.
- **Tipo de datos**: Asegúrate de que el primer argumento sea un vector de caracteres, de lo contrario, la función generará un error.

## Resumen en una línea
La función `endsWith` en R permite verificar de manera eficiente si las cadenas de un vector terminan con un sufijo específico.