<!--
Meta Description: # mapply in R: Effiziente Anwendung von Funktionen auf mehrere Vektoren ## Synopsis Die Funktion `mapply` in R ermöglicht es, eine Funktion auf mehrer...
Meta Keywords: die, mapply, funktion, eine, der
-->

# mapply in R: Effiziente Anwendung von Funktionen auf mehrere Vektoren

## Synopsis
Die Funktion `mapply` in R ermöglicht es, eine Funktion auf mehrere Vektoren oder Listen gleichzeitig anzuwenden. Sie ist eine erweiterte Version von `sapply` und bietet eine einfache Möglichkeit, elementweise Berechnungen durchzuführen.

## Dokumentation
### Zweck
`mapply` wird verwendet, um eine Funktion auf die entsprechenden Elemente mehrerer Vektoren oder Listen anzuwenden. Diese Funktion ist besonders nützlich, wenn Sie mehrere Eingabewerte haben, die in Paaren verarbeitet werden müssen.

### Nutzung
Die grundlegende Syntax von `mapply` lautet:

```R
mapply(FUN, ..., MoreArgs = NULL, SIMPLIFY = TRUE, USE.NAMES = TRUE)
```

- **FUN**: Die Funktion, die auf die Elemente angewendet werden soll.
- **...**: Die Vektoren oder Listen, auf die `FUN` angewendet wird.
- **MoreArgs**: Eine optionale Liste von zusätzlichen Argumenten, die an `FUN` übergeben werden.
- **SIMPLIFY**: Ein logischer Wert, der angibt, ob das Ergebnis vereinfacht werden soll (Standard: TRUE).
- **USE.NAMES**: Ein logischer Wert, der angibt, ob die Namen der Eingabewerte verwendet werden sollen (Standard: TRUE).

### Details
`mapply` ist besonders vorteilhaft, wenn die Eingabewerte unterschiedlich lang sind, da es die kürzesten Vektoren automatisch wiederholt. Es kann auch auf Listen angewendet werden, was eine flexible Handhabung der Daten ermöglicht. Diese Funktion ist ein wichtiges Werkzeug für die Datenmanipulation und -verarbeitung in R.

## Beispiele
### Beispiel 1: Einfache Addition
```R
x <- c(1, 2, 3)
y <- c(4, 5, 6)
result <- mapply(sum, x, y)
print(result)  # Ausgabe: 5 7 9
```

### Beispiel 2: Verwendung einer benutzerdefinierten Funktion
```R
multiply <- function(a, b) {
  return(a * b)
}
x <- c(1, 2, 3)
y <- c(4, 5, 6)
result <- mapply(multiply, x, y)
print(result)  # Ausgabe: 4 10 18
```

### Beispiel 3: Mit zusätzlichen Argumenten
```R
add_const <- function(x, const) {
  return(x + const)
}
x <- c(1, 2, 3)
result <- mapply(add_const, x, MoreArgs = list(const = 10))
print(result)  # Ausgabe: 11 12 13
```

## Erklärung
Ein häufiger Fehler bei der Verwendung von `mapply` ist das Missverständnis der Argumentübergabe. Wenn die Längen der Vektoren unterschiedlich sind, wird der kürzeste Vektor wiederholt, was zu unerwarteten Ergebnissen führen kann. Achten Sie deshalb immer darauf, wie viele Elemente in den Eingabewerten vorhanden sind.

Ein weiterer Punkt ist, dass `mapply` die Rückgabewerte in einem Vektor oder einer Matrix zusammenfassen kann, was je nach Zielsetzung sowohl vorteilhaft als auch nachteilig sein kann. Nutzen Sie den Parameter `SIMPLIFY`, um das Verhalten entsprechend Ihren Anforderungen anzupassen.

## Zusammenfassung in einem Satz
`mapply` ist eine effiziente R-Funktion, die es ermöglicht, eine Funktion auf mehrere Vektoren oder Listen gleichzeitig anzuwenden und so elementweise Berechnungen durchzuführen.