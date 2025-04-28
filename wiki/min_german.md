<!--
Meta Description: # min in R: Der Schlüssel zur Bestimmung des Minimalwerts ## Synopsis Die Funktion `min` in R wird verwendet, um den kleinsten Wert aus einem gegebene...
Meta Keywords: min, der, die, von, werten
-->

# min in R: Der Schlüssel zur Bestimmung des Minimalwerts

## Synopsis
Die Funktion `min` in R wird verwendet, um den kleinsten Wert aus einem gegebenen Vektor oder einer Liste von Werten zu ermitteln. Sie ist ein unverzichtbares Werkzeug in der Datenanalyse und Statistik.

## Dokumentation
Die `min`-Funktion ist Teil der Basis-R-Bibliothek und wird häufig in der Datenverarbeitung eingesetzt, um schnell den minimalen Wert aus einer Sammlung von numerischen Werten zu extrahieren. 

### Zweck
- Bestimmung des kleinsten Wertes in einem Vektor oder einer Liste.
- Unterstützung bei statistischen Berechnungen und Datenanalysen.

### Verwendung
Die Grundsyntax der `min`-Funktion lautet:

```R
min(..., na.rm = FALSE)
```

#### Parameter
- `...`: Eine beliebige Anzahl von numerischen Vektoren oder Werten, aus denen der minimale Wert bestimmt werden soll.
- `na.rm`: Ein logischer Wert (TRUE/FALSE), der angibt, ob NA-Werte (fehlende Werte) ignoriert werden sollen. Der Standardwert ist FALSE.

### Rückgabewert
Die Funktion gibt den kleinsten Wert aus den übergebenen Argumenten zurück.

## Beispiele
Hier sind einige grundlegende Anwendungsbeispiele für die `min`-Funktion:

### Beispiel 1: Einfacher Vektor
```R
werte <- c(5, 3, 8, 1, 4)
min_wert <- min(werte)
print(min_wert)  # Ausgabe: 1
```

### Beispiel 2: Mit fehlenden Werten
```R
werte_mit_na <- c(5, NA, 3, 1, 4)
min_wert_ignorieren_na <- min(werte_mit_na, na.rm = TRUE)
print(min_wert_ignorieren_na)  # Ausgabe: 1
```

### Beispiel 3: Mehrere Vektoren
```R
vektor1 <- c(10, 20, 30)
vektor2 <- c(5, 15, 25)
min_wert_multiple <- min(vektor1, vektor2)
print(min_wert_multiple)  # Ausgabe: 5
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von `min` ist die Handhabung von NA-Werten. Wenn NA-Werte im Vektor enthalten sind und `na.rm` nicht auf TRUE gesetzt ist, wird das Ergebnis ebenfalls NA sein. Dies kann zu Verwirrung führen, wenn nicht darauf geachtet wird. 

Zusätzlich ist es wichtig zu beachten, dass `min` nur mit numerischen Werten funktioniert. Das Übergeben von Zeichenfolgen oder anderen Datentypen führt zu einem Fehler.

## Ein-Satz-Zusammenfassung
Die `min`-Funktion in R ermöglicht es, den kleinsten Wert aus einer Vielzahl von Werten schnell und effizient zu bestimmen, wobei die Option besteht, fehlende Werte zu ignorieren.