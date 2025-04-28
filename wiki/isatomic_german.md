<!--
Meta Description: # R-Funktion "is.atomic": Überprüfung auf atomare Datenstrukturen ## Synopsis Die Funktion `is.atomic` in R wird verwendet, um zu überprüfen, ob ein O...
Meta Keywords: atomic, die, ist, funktion, atomar
-->

# R-Funktion "is.atomic": Überprüfung auf atomare Datenstrukturen

## Synopsis
Die Funktion `is.atomic` in R wird verwendet, um zu überprüfen, ob ein Objekt eine atomare Datenstruktur ist. Dies ist besonders nützlich, um die Art von Daten zu identifizieren, mit denen man arbeitet, und um sicherzustellen, dass die Daten in der gewünschten Form vorliegen.

## Dokumentation
### Zweck
Die Funktion `is.atomic` dient dazu, festzustellen, ob ein gegebenes R-Objekt atomar ist. Atomare Datenstrukturen sind grundlegende Datentypen in R, die keine weiteren Unterstrukturen enthalten. Dazu gehören Vektoren, Matrizen und Arrays, die aus einfachen Datentypen wie numerisch, logisch oder Zeichen bestehen.

### Verwendung
Die allgemeine Syntax der Funktion lautet:

```R
is.atomic(x)
```

**Parameter:**
- `x`: Das zu überprüfende Objekt.

**Rückgabewert:**
`is.atomic` gibt einen logischen Wert (`TRUE` oder `FALSE`) zurück, je nachdem, ob das Objekt atomar ist oder nicht.

### Details
Atomare Objekte in R können folgende Typen sein:
- Numerische Vektoren
- Logische Vektoren
- Zeichenvektoren
- Matrizen
- Arrays

Die Funktion unterscheidet sich von ähnlichen Funktionen wie `is.vector`, da sie auch Matrizen und Arrays als atomar betrachtet, während `is.vector` nur eindimensionale Vektoren berücksichtigt.

## Beispiele
Hier sind einige grundlegende Beispiele, die die Verwendung von `is.atomic` veranschaulichen:

```R
# Beispiel 1: Numerischer Vektor
x <- c(1, 2, 3)
is.atomic(x)  # Gibt TRUE zurück

# Beispiel 2: Logischer Vektor
y <- c(TRUE, FALSE)
is.atomic(y)  # Gibt TRUE zurück

# Beispiel 3: Matrix
z <- matrix(1:6, nrow = 2)
is.atomic(z)  # Gibt TRUE zurück

# Beispiel 4: Liste
w <- list(a = 1, b = 2)
is.atomic(w)  # Gibt FALSE zurück

# Beispiel 5: Datenrahmen
df <- data.frame(a = 1:3, b = c("A", "B", "C"))
is.atomic(df)  # Gibt FALSE zurück
```

## Erklärung
Ein häufiges Missverständnis ist, dass alle R-Objekte atomar sind. Es ist wichtig zu beachten, dass komplexe Datenstrukturen wie Listen und Datenrahmen nicht als atomar gelten. Wenn man also `is.atomic` auf solche Objekte anwendet, erhält man `FALSE`. 

Ein weiterer Punkt ist, dass `is.atomic` nur die erste Ebene der Struktur überprüft. Wenn Sie ein verschachteltes Objekt haben, das auf der obersten Ebene atomar ist, aber weitere Listen oder Datenrahmen enthält, wird die Funktion dennoch `TRUE` zurückgeben.

## Einzeiliger Überblick
Die Funktion `is.atomic` in R überprüft, ob ein Objekt atomar ist, und gibt entsprechend `TRUE` oder `FALSE` zurück.