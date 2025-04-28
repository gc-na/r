<!--
Meta Description: # ifelse en R: Función Condicional para Decisiones Efectivas ## Sinopsis La función `ifelse` en R permite realizar evaluaciones condicionales de maner...
Meta Keywords: que, ifelse, para, condición, valores
-->

# ifelse en R: Función Condicional para Decisiones Efectivas

## Sinopsis
La función `ifelse` en R permite realizar evaluaciones condicionales de manera vectorizada, facilitando la toma de decisiones en la manipulación y análisis de datos. Su uso es fundamental en la programación en R para asignar valores basados en condiciones específicas.

## Documentación
### Propósito
La función `ifelse` se utiliza para evaluar una condición y devolver diferentes valores dependiendo de si la condición es verdadera o falsa. Esto es especialmente útil para hacer asignaciones condicionadas en vectores sin necesidad de recurrir a estructuras de control más complejas como `if` y `else`.

### Uso
La sintaxis de la función `ifelse` es la siguiente:

```R
ifelse(condición, valor_si_verdadero, valor_si_falso)
```

- **condición**: Un vector lógico que se evalúa. Cada elemento del vector se examina y se decide si es verdadero o falso.
- **valor_si_verdadero**: El valor que se devolverá para los elementos donde la condición sea verdadera.
- **valor_si_falso**: El valor que se devolverá para los elementos donde la condición sea falsa.

### Detalles
- La función `ifelse` es vectorizada, lo que significa que puede operar sobre vectores completos, devolviendo un vector de la misma longitud.
- Si la longitud de los argumentos `valor_si_verdadero` y `valor_si_falso` es menor que la longitud de la condición, R reciclará estos valores.
- Es importante que la condición sea un vector lógico, ya que de lo contrario puede generar advertencias o errores.

## Ejemplos
### Ejemplo Básico
```R
# Crear un vector de números
numeros <- c(10, 15, 20, 25)

# Usar ifelse para clasificar los números
resultado <- ifelse(numeros > 15, "Mayor que 15", "15 o menor")
print(resultado)
```
**Salida:**
```
[1] "15 o menor" "15 o menor" "Mayor que 15" "Mayor que 15"
```

### Ejemplo con valores numéricos
```R
# Crear un vector de edades
edades <- c(14, 22, 18, 30)

# Clasificar edades
grupo <- ifelse(edades < 18, "Menor de edad", "Mayor de edad")
print(grupo)
```
**Salida:**
```
[1] "Menor de edad" "Mayor de edad" "Mayor de edad" "Mayor de edad"
```

## Explicación
Al utilizar `ifelse`, es importante tener en cuenta algunos aspectos:
- **Reciclaje de vectores**: Si se proporcionan valores para `valor_si_verdadero` o `valor_si_falso` que son más cortos que el vector de condición, R reciclará estos valores. Esto puede llevar a resultados inesperados si no se maneja cuidadosamente.
- **Vectorización**: Aunque `ifelse` es muy eficiente para operaciones vectorizadas, puede no ser la mejor opción para condiciones muy complejas o anidadas, donde el uso de `if` y `else` puede ser más legible.
- **Evaluación de NA**: Si la condición incluye valores NA, el resultado también será NA para esas posiciones, lo que puede ser relevante en análisis de datos reales.

## Resumen en una línea
La función `ifelse` en R permite realizar evaluaciones condicionales de manera eficiente y vectorizada, facilitando la asignación de valores basados en condiciones específicas.