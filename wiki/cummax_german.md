<!--
Meta Description: # cummax in R: Eine umfassende Anleitung zur Verwendung der kumulativen Maximalfunktion ## Synopsis Die Funktion `cummax` in R berechnet die kumulativ...
Meta Keywords: die, cummax, funktion, matrix, werte
-->

# cummax in R: Eine umfassende Anleitung zur Verwendung der kumulativen Maximalfunktion

## Synopsis
Die Funktion `cummax` in R berechnet die kumulativen Maximalwerte eines Vektors oder einer Matrix. Diese Funktion ist besonders nützlich, um den maximalen Wert bis zu jedem Punkt in einem Datensatz zu bestimmen.

## Dokumentation
### Zweck
Die `cummax`-Funktion wird verwendet, um die maximalen Werte in einem Vektor oder in jeder Spalte einer Matrix kumulativ zu berechnen. Dies bedeutet, dass für jeden Index im Datensatz der größte Wert von den ersten Elementen bis zu diesem Index zurückgegeben wird.

### Verwendung
Die grundlegende Syntax der `cummax`-Funktion ist wie folgt:

```R
cummax(x)
```

**Parameter:**
- `x`: Ein numerischer Vektor oder eine Matrix.

**Rückgabewert:**
Die Funktion gibt einen Vektor oder eine Matrix zurück, der/die die kumulativen Maximalwerte enthält.

### Details
- Die Funktion ignoriert NA-Werte standardmäßig und gibt NA zurück, wenn alle Werte NA sind.
- Bei Matrizen wird die Funktion auf jede Spalte angewendet.
- `cummax` ist besonders nützlich in Zeitreihenanalysen, wenn man den höchsten Wert bis zu einem bestimmten Zeitpunkt erfassen möchte.

## Beispiele
### Beispiel 1: Anwendung auf einen Vektor
```R
vec <- c(1, 3, 2, 5, 4)
cummax_vec <- cummax(vec)
print(cummax_vec)
```
**Ausgabe:**
```
[1] 1 3 3 5 5
```

### Beispiel 2: Anwendung auf eine Matrix
```R
mat <- matrix(c(1, 2, 3, 4, 2, 1), nrow = 2)
cummax_mat <- cummax(mat)
print(cummax_mat)
```
**Ausgabe:**
```
     [,1] [,2]
[1,]    1    2
[2,]    1    2
```

## Erklärung
Ein häufiges Missverständnis besteht darin, dass `cummax` die maximalen Werte über alle Elemente hinweg berechnet. Stattdessen werden die maximalen Werte nur bis zu dem jeweiligen Punkt im Vektor oder in der Matrix ermittelt. Ein weiterer Punkt ist, dass NA-Werte die Berechnung beeinflussen können; es ist wichtig sicherzustellen, dass NA-Werte entsprechend behandelt werden, um unerwartete Ergebnisse zu vermeiden.

## One Line Summary
Die `cummax`-Funktion in R berechnet die kumulativen Maximalwerte eines Vektors oder einer Matrix und ist nützlich für Datenanalysen in Zeitreihen.