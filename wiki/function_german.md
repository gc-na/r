<!--
Meta Description: # Funktionen in R: Ein umfassender Leitfaden ## Synopsis In R sind Funktionen grundlegende Bausteine, die es ermöglichen, wiederverwendbare Codeabschn...
Meta Keywords: die, funktion, der, funktionen, und
-->

# Funktionen in R: Ein umfassender Leitfaden

## Synopsis
In R sind Funktionen grundlegende Bausteine, die es ermöglichen, wiederverwendbare Codeabschnitte zu erstellen, die spezifische Aufgaben ausführen. Funktionen nehmen Eingabewerte entgegen, führen Berechnungen durch und geben Ergebnisse zurück.

## Dokumentation
### Zweck
Funktionen in R sind dafür konzipiert, den Code modular und übersichtlich zu halten. Sie ermöglichen die Kapselung von Logik und die Wiederverwendbarkeit von Code in verschiedenen Teilen eines Programms oder Skripts.

### Verwendung
Die grundlegende Syntax zum Definieren einer Funktion in R lautet:

```R
funktion_name <- function(parameter1, parameter2, ...) {
  # Funktionskörper
  return(ergebnis)
}
```

- **funktion_name**: Der Name der Funktion, der verwendet wird, um sie aufzurufen.
- **parameter**: Eingabewerte, die die Funktion benötigt. Diese sind optional und können Standardwerte haben.
- **Funktionskörper**: Der Code, der die Logik der Funktion beschreibt.
- **return()**: Optional, um ein Ergebnis explizit zurückzugeben.

### Details
Funktionen können beliebig viele Parameter haben, und sie können auch andere Funktionen als Argumente akzeptieren. Darüber hinaus unterstützen Funktionen in R auch die Verwendung von Variablenanzahl von Argumenten mittels `...`.

## Beispiele
### Beispiel 1: Einfache Funktion
```R
addiere <- function(a, b) {
  return(a + b)
}

resultat <- addiere(3, 5)  # Ergebnis: 8
```

### Beispiel 2: Funktion mit Default-Werten
```R
multipliziere <- function(a, b = 2) {
  return(a * b)
}

resultat1 <- multipliziere(4)     # Ergebnis: 8 (4 * 2)
resultat2 <- multipliziere(4, 3)  # Ergebnis: 12 (4 * 3)
```

### Beispiel 3: Funktion mit variabler Anzahl von Argumenten
```R
summe <- function(...) {
  return(sum(c(...)))
}

resultat <- summe(1, 2, 3, 4)  # Ergebnis: 10
```

## Erklärung
Ein häufiges Problem bei der Arbeit mit Funktionen in R ist das Verständnis von Scoping-Regeln. Variablen, die innerhalb einer Funktion erstellt werden, sind in der Regel nur innerhalb dieser Funktion sichtbar. Ein weiteres typisches Missverständnis ist die Verwendung von `return()`. In R wird das letzte ausgewertete Objekt einer Funktion automatisch zurückgegeben, auch wenn `return()` nicht verwendet wird.

Zusätzlich sollten Benutzer darauf achten, dass die Anzahl und der Typ der übergebenen Argumente zur Funktion passen. Ansonsten kann es zu Fehlern oder unerwarteten Ergebnissen kommen.

## Ein-Satz-Zusammenfassung
Funktionen in R sind essenzielle Werkzeuge, die es ermöglichen, wiederverwendbare Codeabschnitte zu erstellen, die spezifische Aufgaben ausführen und Ergebnisse zurückgeben.