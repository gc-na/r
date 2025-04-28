<!--
Meta Description: # all.equal.numeric: Eine präzise Vergleichsfunktion für numerische Vektoren in R ## Synopsis Die Funktion `all.equal.numeric` in R wird verwendet, um...
Meta Keywords: die, all, equal, von, der
-->

# all.equal.numeric: Eine präzise Vergleichsfunktion für numerische Vektoren in R

## Synopsis
Die Funktion `all.equal.numeric` in R wird verwendet, um die Gleichheit von numerischen Vektoren zu überprüfen. Sie bietet eine flexible Möglichkeit, um festzustellen, ob zwei numerische Werte oder Vektoren als gleich angesehen werden können, unter Berücksichtigung von numerischen Ungenauigkeiten.

## Dokumentation
### Zweck
`all.equal.numeric` ist eine spezialisierte Version der generischen Funktion `all.equal`, die speziell für die Vergleich von numerischen Daten entwickelt wurde. Sie ist nützlich, wenn Präzisionsfehler oder Rundungsfehler bei der Arbeit mit Fließkommazahlen berücksichtigt werden müssen.

### Verwendung
Die Funktion wird wie folgt verwendet:

```R
all.equal(x, y, ...)
```

#### Parameter
- **x**: Der erste numerische Vektor oder Wert, der überprüft werden soll.
- **y**: Der zweite numerische Vektor oder Wert, mit dem verglichen werden soll.
- **...**: Zusätzliche Argumente, die an die generelle `all.equal`-Funktion übergeben werden können, wie z.B. `tolerance` zur Festlegung der zulässigen Abweichung.

### Details
Die Funktion gibt `TRUE` zurück, wenn die numerischen Werte als gleich betrachtet werden können. Andernfalls wird ein beschreibender string zurückgegeben, der die Unterschiede zwischen den beiden Werten erläutert. Die Funktion berücksichtigt dabei die Möglichkeit von Rundungsfehlern und numerischen Ungenauigkeiten, die häufig in Berechnungen auftreten.

## Beispiele
Hier sind einige grundlegende Beispiele zur Verwendung von `all.equal.numeric`:

```R
# Beispiel 1: Vergleich von zwei gleichen Werten
x <- 1.0000001
y <- 1.0000002
result <- all.equal(x, y, tolerance = 1e-7)
print(result)  # Gibt TRUE zurück

# Beispiel 2: Vergleich von zwei unterschiedlichen Werten
x <- 1.0
y <- 1.1
result <- all.equal(x, y)
print(result)  # Gibt einen beschreibenden String zurück

# Beispiel 3: Vergleich von Vektoren
vec1 <- c(1.0, 2.0, 3.0)
vec2 <- c(1.0, 2.0000001, 3.0)
result <- all.equal(vec1, vec2, tolerance = 1e-7)
print(result)  # Gibt TRUE zurück
```

## Erklärung
Ein häufiges Problem bei der Verwendung von `all.equal.numeric` ist das Missverständnis über den `tolerance`-Parameter. Wenn dieser Parameter nicht korrekt eingestellt ist, kann es zu falschen Ergebnissen kommen, insbesondere wenn die verglichenen Werte sehr nah beieinander liegen. Es ist wichtig, die Toleranz entsprechend der Genauigkeit der verwendeten Daten festzulegen.

Ein weiterer Hinweis ist, dass die Funktion nicht für den Vergleich von nicht-numerischen Daten geeignet ist. In solchen Fällen sollte die generische `all.equal`-Funktion verwendet werden.

## Einzeiler-Zusammenfassung
`all.equal.numeric` ist eine nützliche Funktion in R zum Vergleich von numerischen Werten und Vektoren, die Rundungsfehler und numerische Ungenauigkeiten berücksichtigt.