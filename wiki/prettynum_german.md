<!--
Meta Description: # prettyNum in R: Zahlen ansprechend formatieren ## Synopsis Die Funktion `prettyNum` in R dient dazu, numerische Werte in ansprechender und lesbarer ...
Meta Keywords: die, prettynum, zahlen, ist, der
-->

# prettyNum in R: Zahlen ansprechend formatieren

## Synopsis
Die Funktion `prettyNum` in R dient dazu, numerische Werte in ansprechender und lesbarer Form zu formatieren, indem sie beispielsweise Kommas, Dezimalstellen und wissenschaftliche Notation anpasst.

## Dokumentation
Die `prettyNum`-Funktion ist Teil der Basis R-Pakete und wird verwendet, um numerische Werte in einem benutzerfreundlichen Format darzustellen. Sie ermöglicht die Anpassung der Darstellung von Zahlen, um sie für Berichte, Grafiken oder Benutzeroberflächen ansprechender zu gestalten.

### Zweck
Die Funktion `prettyNum` ist speziell dafür entwickelt, um numerische Daten in einem Format darzustellen, das für den Menschen besser lesbar ist. Dies ist besonders nützlich, wenn große oder kleine Zahlen im Spiel sind.

### Nutzung
Die grundlegende Syntax der Funktion lautet:

```R
prettyNum(x, big.mark = ",", scientific = FALSE, ...)
```

#### Parameter:
- `x`: Ein numerischer Vektor, der formatiert werden soll.
- `big.mark`: Ein Zeichen, das als Tausender-Trennzeichen verwendet wird (Standard ist ein Komma).
- `scientific`: Ein logischer Wert, der angibt, ob wissenschaftliche Notation verwendet werden soll (Standard ist `FALSE`).
- `...`: Zusätzliche Parameter, die an die Funktion übergeben werden können.

### Details
Die `prettyNum`-Funktion ist besonders nützlich in der Datenanalyse und -visualisierung, da sie es ermöglicht, Zahlen so zu formatieren, dass sie leicht verständlich sind. Die Anpassungen können auch auf spezifische Anforderungen der Benutzeroberflächen abgestimmt werden.

## Beispiele
Hier sind einige Beispiele für die Verwendung von `prettyNum`:

### Beispiel 1: Grundlegende Nutzung
```R
zahlen <- c(1234567.89, 9876543.21)
prettyNum(zahlen)
# Ausgabe: "1,234,567.89" "9,876,543.21"
```

### Beispiel 2: Anpassung des Tausender-Trennzeichens
```R
prettyNum(zahlen, big.mark = ".")
# Ausgabe: "1.234.567,89" "9.876.543,21"
```

### Beispiel 3: Nutzung wissenschaftlicher Notation
```R
zahlen <- c(0.000123, 0.000456)
prettyNum(zahlen, scientific = TRUE)
# Ausgabe: "1.23e-04" "4.56e-04"
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von `prettyNum` kann sein, dass das gewünschte Format nicht sofort durch die Standardparameter erreicht wird. Es ist wichtig, die Parameter `big.mark` und `scientific` je nach Bedarf anzupassen. Ein weiterer Punkt ist, dass `prettyNum` keine Rundung vornimmt; die zugrunde liegenden Werte bleiben unverändert, was zu unerwarteten Ergebnissen führen kann, wenn man nicht auf die Darstellung achtet.

## Ein-Satz-Zusammenfassung
Die Funktion `prettyNum` in R formatiert numerische Werte ansprechend und leserlich, indem sie Tausender-Trennzeichen anpasst und die wissenschaftliche Notation steuert.