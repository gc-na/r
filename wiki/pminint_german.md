<!--
Meta Description: # pmin.int: Minimale Werte in R bestimmen ## Synopsis `pmin.int` ist eine Funktion in R, die verwendet wird, um elementweise den minimalen Wert aus me...
Meta Keywords: pmin, int, werte, ist, die
-->

# pmin.int: Minimale Werte in R bestimmen

## Synopsis
`pmin.int` ist eine Funktion in R, die verwendet wird, um elementweise den minimalen Wert aus mehreren Vektoren oder Zahlen zu ermitteln. Sie eignet sich hervorragend für numerische Berechnungen und Vergleiche.

## Dokumentation
### Zweck
Die Funktion `pmin.int` gehört zur Familie der `pmin`-Funktionen und ist speziell für die Verarbeitung von Ganzzahlen (integer) optimiert. Sie ermöglicht es Anwendern, aus einer Reihe von Werten den jeweils kleinsten Wert auszuwählen, was in statistischen Analysen und Datenverarbeitungen nützlich ist.

### Verwendung
```R
pmin.int(..., na.rm = FALSE)
```

#### Parameter
- `...`: Eine beliebige Anzahl von Vektoren oder skalaren Werten, aus denen die minimalen Werte ermittelt werden sollen.
- `na.rm`: Ein logischer Wert, der angibt, ob fehlende Werte (NA) ignoriert werden sollen (`TRUE`) oder nicht (`FALSE`). Der Standardwert ist `FALSE`.

### Details
`pmin.int` gibt einen Vektor zurück, der die minimalen Werte der Eingabewerte enthält. Diese Funktion ist effizient und speziell für Ganzzahlen optimiert, was sie besonders schnell macht, wenn große Mengen an ganzzahligen Daten verarbeitet werden.

## Beispiele
Hier sind einige einfache Beispiele, wie `pmin.int` verwendet werden kann:

```R
# Beispiel: Minimale Werte aus zwei Vektoren
x <- c(3L, 5L, 2L)
y <- c(4L, 1L, 6L)
min_values <- pmin.int(x, y)
print(min_values)
# Ausgabe: [1] 3 1 2

# Beispiel mit NA-Werten
a <- c(1L, NA, 3L)
b <- c(2L, 5L, NA)
min_values_na <- pmin.int(a, b, na.rm = TRUE)
print(min_values_na)
# Ausgabe: [1] 1 5 3
```

## Erklärung
Ein häufiger Fehler bei der Verwendung von `pmin.int` tritt auf, wenn der Benutzer versucht, Vektoren mit unterschiedlichen Längen zu übergeben. In einem solchen Fall wird die kürzere Länge wiederholt, was möglicherweise zu unerwarteten Ergebnissen führen kann. Außerdem sollte beachtet werden, dass die Verwendung von `na.rm = TRUE` notwendig ist, wenn fehlende Werte in den Eingabedaten vorhanden sind und diese nicht berücksichtigt werden sollen.

## Einzeiliger Zusammenfassung
`pmin.int` ist eine effiziente R-Funktion zur Bestimmung elementweise minimaler Werte aus mehreren Ganzzahlen-Vektoren.