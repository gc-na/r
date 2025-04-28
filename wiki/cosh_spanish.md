<!--
Meta Description: # cosh en R: Cálculo del coseno hiperbólico ## Sinopsis El comando `cosh` en R se utiliza para calcular el coseno hiperbólico de un número o de un vec...
Meta Keywords: cosh, coseno, hiperbólico, del, vector
-->

# cosh en R: Cálculo del coseno hiperbólico

## Sinopsis
El comando `cosh` en R se utiliza para calcular el coseno hiperbólico de un número o de un vector de números. Esta función es fundamental en matemáticas, especialmente en áreas relacionadas con la trigonometría hiperbólica y el análisis complejo.

## Documentación
### Propósito
La función `cosh` proporciona una forma sencilla y eficiente de calcular el coseno hiperbólico, que es definido como:

\[
\cosh(x) = \frac{e^x + e^{-x}}{2}
\]

donde \( e \) es la base del logaritmo natural, aproximadamente igual a 2.71828.

### Uso
La sintaxis básica de la función `cosh` es:

```R
cosh(x)
```

- **x**: Un número o un vector numérico. `x` puede ser tanto un valor escalar como una matriz o un vector de valores.

### Detalles
- `cosh` devuelve el coseno hiperbólico de cada elemento en `x`.
- Si `x` es un vector, la función opera elemento por elemento y devuelve un vector de la misma longitud.
- La función es parte del paquete base de R, por lo que no se requiere cargar ningún paquete adicional.

## Ejemplos
### Ejemplo 1: Cálculo del coseno hiperbólico de un número
```R
# Cálculo del coseno hiperbólico de 0
resultado <- cosh(0)
print(resultado) # Salida: 1
```

### Ejemplo 2: Cálculo del coseno hiperbólico de un vector
```R
# Cálculo del coseno hiperbólico de un vector
valores <- c(-1, 0, 1)
resultado_vector <- cosh(valores)
print(resultado_vector) # Salida: 1.5430806348152437 1.0000000000000000 1.5430806348152437
```

### Ejemplo 3: Cálculo del coseno hiperbólico de una matriz
```R
# Cálculo del coseno hiperbólico de una matriz
matriz <- matrix(c(-1, 0, 1, 2), nrow = 2)
resultado_matriz <- cosh(matriz)
print(resultado_matriz)
# Salida:
#      [,1]      [,2]
# [1,] 1.5430806 1.7627458
# [2,] 1.0000000 3.7621957
```

## Explicación
### Errores comunes y notas adicionales
- Asegúrate de que los valores de entrada sean numéricos. Si se pasan valores no numéricos, se generará un error.
- Ten en cuenta que `cosh` retornará valores muy grandes para entradas grandes, ya que la función crece exponencialmente.
- Recuerda que el coseno hiperbólico siempre es positivo, independientemente de si la entrada es negativa o positiva.

## Resumen en una línea
La función `cosh` en R calcula el coseno hiperbólico de un número o de un vector de números de manera eficiente y sencilla.