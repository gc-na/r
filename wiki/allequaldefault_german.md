<!--
Meta Description: # all.equal.default: Vergleich von R-Objekten ## Synopsis `all.equal.default` ist eine Funktion in R, die verwendet wird, um zwei R-Objekte auf Gleich...
Meta Keywords: die, all, equal, von, default
-->

# all.equal.default: Vergleich von R-Objekten

## Synopsis
`all.equal.default` ist eine Funktion in R, die verwendet wird, um zwei R-Objekte auf Gleichheit zu überprüfen. Diese Funktion bietet eine flexible Möglichkeit, Unterschiede zwischen Objekten zu identifizieren, insbesondere bei numerischen Werten, die aufgrund von Rundungsfehlern variieren können.

## Dokumentation
Die Funktion `all.equal.default` ist Teil der `base`-Bibliothek von R und wird verwendet, um die Gleichheit von Objekten zu prüfen. Sie ist besonders nützlich, wenn es darum geht, numerische Daten zu vergleichen, da sie Toleranzen für numerische Ungenauigkeiten berücksichtigt.

### Zweck
Der Hauptzweck von `all.equal.default` besteht darin, zwei Objekte zu vergleichen und dabei Unterschiede zu erkennen, die für den Benutzer möglicherweise von Bedeutung sind, wie z.B. Rundungsfehler oder unterschiedliche Datentypen.

### Verwendung
Die allgemeine Syntax lautet:
```R
all.equal(target, current, ...)
```

- **target**: Das erste Objekt, das verglichen werden soll.
- **current**: Das zweite Objekt, das mit dem ersten verglichen wird.
- **...**: Zusätzliche Argumente, die an interne Vergleichsfunktionen übergeben werden können.

### Details
`all.equal.default` gibt entweder `TRUE` zurück, wenn die Objekte gleich sind, oder eine Beschreibung der Unterschiede, wenn sie nicht gleich sind. Die Funktion berücksichtigt dabei numerische Toleranzen und kann so konzipiert werden, dass sie auch bei kleinen Abweichungen eine Gleichheit akzeptiert.

## Beispiele
Hier sind einige grundlegende Beispiele für die Verwendung von `all.equal.default`:

### Beispiel 1: Vergleich von numerischen Vektoren
```R
v1 <- c(1.0000001, 2, 3)
v2 <- c(1, 2, 3)
result <- all.equal(v1, v2)
print(result)  # Gibt TRUE zurück, da die Toleranz berücksichtigt wird.
```

### Beispiel 2: Vergleich von Datenrahmen
```R
df1 <- data.frame(a = c(1, 2), b = c(3, 4))
df2 <- data.frame(a = c(1, 2), b = c(3, 4))
result <- all.equal(df1, df2)
print(result)  # Gibt TRUE zurück.
```

### Beispiel 3: Vergleich von Listen
```R
list1 <- list(a = 1, b = 2)
list2 <- list(a = 1, b = 2)
result <- all.equal(list1, list2)
print(result)  # Gibt TRUE zurück.
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von `all.equal.default` ist die Annahme, dass es eine strikte Überprüfung vornimmt. Tatsächlich berücksichtigt die Funktion numerische Toleranzen, was zu unerwarteten Ergebnissen führen kann, wenn man mit sehr kleinen oder sehr großen Zahlen arbeitet. Es ist auch wichtig, sicherzustellen, dass die Objekte denselben Typ haben, da Unterschiede in den Datentypen zu unerwarteten Ergebnissen führen können.

## Einzeilige Zusammenfassung
`all.equal.default` ist eine R-Funktion, die zwei Objekte vergleicht und Unterschiede unter Berücksichtigung von numerischen Toleranzen identifiziert.