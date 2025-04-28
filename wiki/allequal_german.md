<!--
Meta Description: # all.equal: Vergleich von R-Objekten auf Gleichheit ## Synopsis Die Funktion `all.equal` in R wird verwendet, um zwei R-Objekte auf Gleichheit zu übe...
Meta Keywords: die, all, equal, von, vergleich
-->

# all.equal: Vergleich von R-Objekten auf Gleichheit

## Synopsis
Die Funktion `all.equal` in R wird verwendet, um zwei R-Objekte auf Gleichheit zu überprüfen, wobei eine Toleranz für numerische Werte berücksichtigt wird. Dies ist besonders nützlich in der Datenanalyse und beim Testen von Funktionen.

## Dokumentation
### Zweck
`all.equal` ist eine robuste Funktion, die verwendet wird, um festzustellen, ob zwei R-Objekte gleich sind, indem sie die Struktur und die Inhalte der Objekte vergleicht. Sie ist ideal für den Vergleich von Datenrahmen, Matrizen, Vektoren und anderen komplexen Objekten.

### Verwendung
Die Grundsyntax der Funktion lautet:

```R
all.equal(target, current, tolerance = NULL, ...)
```

- **target**: Das Referenzobjekt, das mit dem aktuellen Objekt verglichen werden soll.
- **current**: Das Objekt, das mit dem Zielobjekt verglichen wird.
- **tolerance**: Ein optionaler Parameter, der die maximale zulässige Differenz für numerische Vergleiche angibt.
- **...**: Zusätzliche Argumente, die an spezifische Vergleichsfunktionen übergeben werden können.

### Details
`all.equal` gibt `TRUE` zurück, wenn die Objekte als gleich angesehen werden, oder eine Beschreibung der Unterschiede, falls sie nicht gleich sind. Die Funktion kann insbesondere für numerische Werte eine Toleranz berücksichtigen, was bedeutet, dass zwei Werte, die sich nur minimal unterscheiden, als gleich angesehen werden können.

## Beispiele
### Beispiel 1: Vergleich von Vektoren
```R
v1 <- c(1, 2, 3)
v2 <- c(1, 2, 3)
all.equal(v1, v2) # Gibt TRUE zurück
```

### Beispiel 2: Vergleich mit Toleranz
```R
v3 <- c(1.00001, 2.00001, 3.00001)
v4 <- c(1, 2, 3)
all.equal(v3, v4, tolerance = 0.0001) # Gibt TRUE zurück
```

### Beispiel 3: Vergleich von Datenrahmen
```R
df1 <- data.frame(a = 1:3, b = c("x", "y", "z"))
df2 <- data.frame(a = 1:3, b = c("x", "y", "z"))
all.equal(df1, df2) # Gibt TRUE zurück
```

## Erklärung
Eine häufige Falle beim Gebrauch von `all.equal` ist das Vergleichen von Objekten, die unterschiedliche Strukturen oder Klassen haben. In solchen Fällen kann die Funktion nicht wie erwartet arbeiten und gibt möglicherweise eine Fehlermeldung zurück.

Ein weiterer Punkt ist, dass `all.equal` nicht unbedingt für den Vergleich von Listen geeignet ist, die komplexe Strukturen enthalten. In solchen Fällen kann es sinnvoll sein, spezifische Vergleichsoperationen für die jeweilige Struktur durchzuführen.

## Ein-Satz-Zusammenfassung
Die Funktion `all.equal` in R ermöglicht den flexiblen und robusten Vergleich von Objekten unter Berücksichtigung von Toleranzen für numerische Werte.