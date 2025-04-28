<!--
Meta Description: # Duplicated.default in R: Identifizierung von Duplikaten in Daten ## Synopsis Die Funktion `duplicated.default` in R ist ein wesentliches Werkzeug zu...
Meta Keywords: false, duplicated, die, der, ein
-->

# Duplicated.default in R: Identifizierung von Duplikaten in Daten

## Synopsis
Die Funktion `duplicated.default` in R ist ein wesentliches Werkzeug zur Identifizierung von Duplikaten in Vektoren, Listen und Datenrahmen. Sie ermöglicht es Benutzern, wiederholte Werte auf einfache Weise zu erkennen und zu analysieren.

## Dokumentation
Die Funktion `duplicated.default` gehört zur Familie der `duplicated`-Funktionen in R, die dazu dienen, doppelte Einträge in einem Datensatz zu identifizieren. Die Hauptanwendung besteht darin, festzustellen, ob ein Element in einem Vektor oder einer Liste bereits zuvor aufgetreten ist.

### Zweck
Der Hauptzweck von `duplicated.default` besteht darin, eine logische Vektorausgabe zu generieren, die anzeigt, ob die jeweiligen Elemente eines Vektors oder einer Liste Duplikate sind.

### Verwendung
```R
duplicated(x, incomparables = FALSE)
```

- **x**: Ein Vektor oder eine Liste, in der Duplikate identifiziert werden sollen.
- **incomparables**: Ein optionaler Parameter, der angibt, ob bestimmte Werte bei der Duplikatsprüfung ausgeschlossen werden sollen. Standardmäßig ist dieser Parameter auf `FALSE` gesetzt.

### Details
Die Funktion gibt einen logischen Vektor zurück, der für jedes Element in `x` angibt, ob es ein Duplikat ist (TRUE) oder nicht (FALSE). Der erste Vorkommen eines Wertes wird als nicht dupliziert betrachtet, während alle nachfolgenden Vorkommen als dupliziert markiert werden.

## Beispiele

### Beispiel 1: Einfaches Vektor-Duplikat
```R
x <- c(1, 2, 3, 2, 1)
duplicated(x)
# Ausgabe: FALSE FALSE FALSE TRUE TRUE
```

### Beispiel 2: Duplikate in einer Liste
```R
y <- list(a = 1, b = 2, c = 1, d = 3)
duplicated(y)
# Ausgabe: FALSE FALSE TRUE FALSE
```

### Beispiel 3: Ausschluss von Werten
```R
z <- c(1, 2, 3, NA, 2, NA)
duplicated(z, incomparables = NA)
# Ausgabe: FALSE FALSE FALSE FALSE TRUE FALSE
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von `duplicated.default` ist, dass NA-Werte standardmäßig als gleich behandelt werden. Wenn Sie NA-Werte in Ihren Daten haben, müssen Sie den Parameter `incomparables` anpassen, um die gewünschte Handhabung dieser Werte sicherzustellen. Werden NA-Werte nicht ausgeschlossen, kann dies zu unerwarteten Ergebnissen führen.

Zusätzlich ist es wichtig zu beachten, dass `duplicated` für komplexere Datenstrukturen wie Datenrahmen nicht direkt verwendet werden kann, ohne eine entsprechende Umwandlung vorzunehmen.

## Ein-Satz-Zusammenfassung
Die Funktion `duplicated.default` in R ermöglicht die effektive Identifizierung von Duplikaten in Vektoren und Listen, indem sie logische Vektoren zurückgibt, die angeben, ob die Elemente Duplikate sind.