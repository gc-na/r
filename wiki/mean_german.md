<!--
Meta Description: # Durchschnitt in R: Eine umfassende Anleitung zur Berechnung des Mittelwerts ## Synopsis Der Befehl `mean()` in R wird verwendet, um den Durchschnitt...
Meta Keywords: der, mittelwert, mean, die, werte
-->

# Durchschnitt in R: Eine umfassende Anleitung zur Berechnung des Mittelwerts

## Synopsis
Der Befehl `mean()` in R wird verwendet, um den Durchschnitt (Mittelwert) eines Vektors oder einer Datenreihe zu berechnen. Dies ist eine grundlegende statistische Funktion, die häufig in der Datenanalyse verwendet wird.

## Dokumentation
### Zweck
Die Funktion `mean()` ermöglicht es Benutzern, den arithmetischen Mittelwert einer numerischen Datenreihe zu berechnen. Der Mittelwert ist eine der am häufigsten verwendeten Maße für zentrale Tendenz in der Statistik.

### Verwendung
Die grundlegende Syntax der Funktion lautet:

```R
mean(x, trim = 0, na.rm = FALSE, ...)
```

**Parameter:**
- `x`: Ein numerischer Vektor oder ein Datenrahmen, dessen Mittelwert berechnet werden soll.
- `trim`: Ein numerischer Wert zwischen 0 und 0,5, der angibt, wie viel Prozent der höchsten und niedrigsten Werte beim Berechnen des Mittelwerts ignoriert werden sollen (standardmäßig 0).
- `na.rm`: Ein logischer Wert, der angibt, ob fehlende Werte (NA) ignoriert werden sollen (standardmäßig FALSE).
- `...`: Weitere Parameter, die an andere Funktionen übergeben werden können.

### Details
Der Mittelwert wird berechnet, indem alle Werte in `x` summiert und durch die Anzahl der Werte geteilt werden. Wenn `na.rm = TRUE` gesetzt ist, werden alle NA-Werte aus der Berechnung ausgeschlossen, was in vielen realen Datensätzen wichtig ist, da sie häufig auftreten können.

## Beispiele
Hier sind einige grundlegende Beispiele zur Verwendung der `mean()`-Funktion in R:

### Beispiel 1: Einfache Mittelwertberechnung
```R
werte <- c(1, 2, 3, 4, 5)
mittelwert <- mean(werte)
print(mittelwert)  # Ausgabe: 3
```

### Beispiel 2: Mittelwert mit fehlenden Werten
```R
werte_mit_na <- c(1, 2, NA, 4, 5)
mittelwert_mit_na <- mean(werte_mit_na, na.rm = TRUE)
print(mittelwert_mit_na)  # Ausgabe: 3
```

### Beispiel 3: Getrimmter Mittelwert
```R
werte_getrimmt <- c(1, 2, 3, 4, 5, 100)
getrimmter_mittelwert <- mean(werte_getrimmt, trim = 0.2)
print(getrimmter_mittelwert)  # Ausgabe: 3
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von `mean()` ist die Handhabung von NA-Werten. Wenn NA-Werte im Vektor enthalten sind und `na.rm = FALSE` (Standardwert) verwendet wird, wird das Ergebnis ebenfalls NA sein. Um dies zu vermeiden, sollten Benutzer sicherstellen, dass sie `na.rm = TRUE` verwenden, wenn sie mit unvollständigen Daten arbeiten. Ein weiterer Punkt ist die Bedeutung des Parameters `trim`, der bei der Berechnung des Mittelwerts helfen kann, Ausreißer zu reduzieren. 

## Ein-Satz-Zusammenfassung
Die `mean()`-Funktion in R berechnet den arithmetischen Mittelwert eines numerischen Vektors und bietet Optionen zur Handhabung von NA-Werten sowie zur Trimmung von Ausreißern.