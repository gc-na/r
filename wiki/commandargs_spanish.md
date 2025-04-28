<!--
Meta Description: # commandArgs: Cómo utilizar argumentos en R ## Sinopsis `commandArgs` es una función en R que permite acceder a los argumentos de la línea de comando...
Meta Keywords: argumentos, commandargs, script, los, línea
-->

# commandArgs: Cómo utilizar argumentos en R

## Sinopsis
`commandArgs` es una función en R que permite acceder a los argumentos de la línea de comandos pasados a un script R. Esta herramienta es especialmente útil para la automatización de tareas y el desarrollo de scripts que requieren parámetros de entrada.

## Documentación
### Propósito
La función `commandArgs` tiene como objetivo facilitar la lectura de argumentos directamente desde la línea de comandos al ejecutar scripts en R. Esto es útil para personalizar la ejecución de scripts sin modificar el código fuente.

### Uso
La función se utiliza de la siguiente manera:

```R
commandArgs(trailingOnly = FALSE)
```

- `trailingOnly`: Un argumento lógico que, si se establece en `TRUE`, devuelve solo los argumentos que vienen después del nombre del script. Por defecto, es `FALSE` y devuelve todos los argumentos.

### Detalles
- La función devuelve un vector de caracteres que contiene los argumentos pasados al script.
- Al ejecutar un script, los argumentos se pasan en la línea de comandos después del nombre del script. Por ejemplo:
  
  ```bash
  Rscript mi_script.R arg1 arg2 arg3
  ```

  En este caso, `arg1`, `arg2`, y `arg3` serán accesibles a través de `commandArgs()`.

## Ejemplos
### Ejemplo 1: Acceder a argumentos básicos
```R
# mi_script.R
args <- commandArgs(trailingOnly = TRUE)
print(args)
```
Si se ejecuta desde la línea de comandos:
```bash
Rscript mi_script.R valor1 valor2
```
La salida será:
```
[1] "valor1" "valor2"
```

### Ejemplo 2: Uso de argumentos en un script
```R
# script_suma.R
args <- commandArgs(trailingOnly = TRUE)
num1 <- as.numeric(args[1])
num2 <- as.numeric(args[2])
resultado <- num1 + num2
cat("La suma es:", resultado, "\n")
```
Ejecutando:
```bash
Rscript script_suma.R 5 10
```
La salida será:
```
La suma es: 15 
```

## Explicación
### Errores comunes
- **No se pasan argumentos**: Si se ejecuta el script sin argumentos, `args` será un vector vacío. Esto puede causar errores si el script intenta acceder a elementos inexistentes.
- **Tipado de argumentos**: Los argumentos se reciben como cadenas de texto. Es importante convertirlos al tipo de datos adecuado (por ejemplo, usar `as.numeric` para números) antes de utilizarlos.
- **Ambiente de ejecución**: `commandArgs` solo funciona correctamente en entornos donde R se ejecuta desde la línea de comandos, como Rscript o R CMD BATCH. En entornos interactivos, como RStudio, no se comportará de la misma manera.

## Resumen en una línea
La función `commandArgs` en R permite acceder a los argumentos de la línea de comandos, facilitando la personalización y automatización de scripts.