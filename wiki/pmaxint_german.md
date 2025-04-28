<!--
Meta Description: # pmax.int in R: Maximale Werte zwischen Integer-Vektoren ## Synopsis Die Funktion `pmax.int` in R ermöglicht es Benutzern, die maximalen Werte aus me...
Meta Keywords: pmax, int, die, werte, integer
-->

# pmax.int in R: Maximale Werte zwischen Integer-Vektoren

## Synopsis
Die Funktion `pmax.int` in R ermöglicht es Benutzern, die maximalen Werte aus mehreren Integer-Vektoren zu berechnen. Diese Funktion ist besonders nützlich, wenn man elementweise den größten Wert aus mehreren Datensätzen ermitteln möchte.

## Documentation
### Zweck
Die Funktion `pmax.int` wird verwendet, um den maximalen Wert an jeder Position aus mehreren Integer-Vektoren zu ermitteln. Sie ist Teil der Basis R-Funktionen und bietet eine effiziente Möglichkeit, um Vergleiche zwischen Vektoren anzustellen.

### Verwendung
Die grundlegende Syntax der Funktion lautet:

```R
pmax.int(..., na.rm = FALSE)
```

#### Parameter
- `...`: Eine oder mehrere Integer-Vektoren, deren maximale Werte berechnet werden sollen.
- `na.rm`: Ein logischer Wert (TRUE oder FALSE). Wenn TRUE, werden NA-Werte ignoriert. Der Standardwert ist FALSE.

### Details
`pmax.int` ist eine optimierte Version von `pmax`, die speziell für Integer-Daten entwickelt wurde, um die Leistung zu steigern. Die Funktion gibt einen Integer-Vektor zurück, der die maximalen Werte an jeder Position enthält.

## Examples
Hier sind einige grundlegende Anwendungsbeispiele für `pmax.int`:

### Beispiel 1: Einfache Verwendung
```R
vec1 <- c(1L, 3L, 5L)
vec2 <- c(2L, 2L, 4L)
max_values <- pmax.int(vec1, vec2)
print(max_values)  # Ausgabe: [1] 2 3 5
```

### Beispiel 2: Mit NA-Werten
```R
vec1 <- c(1L, NA, 5L)
vec2 <- c(2L, 3L, NA)
max_values_na <- pmax.int(vec1, vec2, na.rm = TRUE)
print(max_values_na)  # Ausgabe: [1] 2 3 5
```

### Beispiel 3: Mehrere Vektoren
```R
vec1 <- c(1L, 4L, 3L)
vec2 <- c(2L, 3L, 6L)
vec3 <- c(5L, 1L, 2L)
max_values_multi <- pmax.int(vec1, vec2, vec3)
print(max_values_multi)  # Ausgabe: [1] 5 4 6
```

## Explanation
Ein häufiger Fehler bei der Verwendung von `pmax.int` besteht darin, dass Benutzer `NA`-Werte nicht richtig behandeln. Wenn `na.rm` nicht auf TRUE gesetzt ist, kann das Ergebnis ebenfalls `NA` sein, wenn sich in den Eingabevektoren `NA`-Werte befinden. Darüber hinaus ist `pmax.int` ausschließlich für Integer-Vektoren gedacht. Die Verwendung mit anderen Datentypen kann zu unerwarteten Ergebnissen führen.

## One Line Summary
Die Funktion `pmax.int` in R ermittelt elementweise die maximalen Werte aus mehreren Integer-Vektoren und ignoriert optional NA-Werte.