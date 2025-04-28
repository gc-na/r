<!--
Meta Description: # mean.default in R: Durchschnittsberechnung für numerische Vektoren ## Synopsis Der Befehl `mean.default` in R wird verwendet, um den arithmetischen ...
Meta Keywords: die, mean, funktion, ist, default
-->

# mean.default in R: Durchschnittsberechnung für numerische Vektoren

## Synopsis
Der Befehl `mean.default` in R wird verwendet, um den arithmetischen Mittelwert eines numerischen Vektors zu berechnen. Diese Funktion ist besonders nützlich in statistischen Analysen und Datenmanipulationen.

## Documentation
### Zweck
Die Funktion `mean.default` ist eine Standardimplementierung der `mean`-Funktion in R, die speziell für numerische Vektoren konzipiert ist. Sie berechnet den Durchschnittswert der Elemente in einem Vektor und ignoriert dabei NA-Werte, sofern nicht anders angegeben.

### Verwendung
```R
mean(x, na.rm = FALSE, ...)
```
- **x**: Ein numerischer Vektor oder eine Liste.
- **na.rm**: Ein logischer Wert (TRUE/FALSE). Wenn TRUE, werden NA-Werte aus der Berechnung ausgeschlossen.
- **...**: Zusätzliche Argumente, die an die Funktion übergeben werden können.

### Details
Die `mean.default`-Funktion ist die Standardmethode zur Berechnung des Mittelwerts in R. Sie wird aufgerufen, wenn die `mean`-Funktion auf einen numerischen Vektor angewendet wird. Die Funktion bietet eine einfache Möglichkeit, den Durchschnitt zu berechnen, wobei der Umgang mit fehlenden Werten (NA) flexibel gestaltet werden kann.

## Examples
### Beispiel 1: Grundlegende Verwendung
```R
# Erstellen eines numerischen Vektors
zahlen <- c(1, 2, 3, 4, 5)

# Berechnung des Durchschnitts
durchschnitt <- mean(zahlen)
print(durchschnitt)  # Ausgabe: 3
```

### Beispiel 2: Umgang mit NA-Werten
```R
# Erstellen eines Vektors mit NA-Werten
zahlen_mit_na <- c(1, 2, NA, 4, 5)

# Berechnung des Durchschnitts ohne NA-Werte
durchschnitt_ohne_na <- mean(zahlen_mit_na, na.rm = TRUE)
print(durchschnitt_ohne_na)  # Ausgabe: 3
```

## Explanation
Ein häufiges Problem beim Arbeiten mit der `mean.default`-Funktion sind NA-Werte, die die Berechnung des Durchschnitts beeinflussen können. Standardmäßig berücksichtigt die Funktion diese Werte, was zu unerwarteten Ergebnissen führen kann. Um dies zu vermeiden, sollte immer das Argument `na.rm = TRUE` verwendet werden, wenn NA-Werte vorhanden sind.

Ein weiterer Aspekt ist, dass die Funktion nur für numerische Daten geeignet ist. Bei anderen Datentypen, wie Zeichenfolgen oder Faktoren, wird ein Fehler ausgegeben. Daher ist es wichtig, sicherzustellen, dass die Eingabedaten korrekt formatiert sind.

## One Line Summary
`mean.default` in R berechnet den arithmetischen Mittelwert eines numerischen Vektors und bietet Optionen zur Behandlung von NA-Werten.