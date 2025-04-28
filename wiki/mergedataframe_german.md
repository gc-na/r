<!--
Meta Description: # merge.data.frame: Datenrahmen in R zusammenführen ## Synopsis Die Funktion `merge.data.frame` in R ermöglicht das Zusammenführen von zwei oder mehr ...
Meta Keywords: die, data, frame, merge, datenrahmen
-->

# merge.data.frame: Datenrahmen in R zusammenführen

## Synopsis
Die Funktion `merge.data.frame` in R ermöglicht das Zusammenführen von zwei oder mehr Datenrahmen auf Basis gemeinsamer Variablen, was sie zu einem unverzichtbaren Werkzeug für Datenanalysten und Statistiker macht.

## Dokumentation
Die Funktion `merge.data.frame` wird verwendet, um Datenrahmen in R zu kombinieren, basierend auf gemeinsamen Spalten oder Zeilen. Diese Funktion ist besonders nützlich beim Arbeiten mit relationalen Daten, wo Informationen in mehreren Datenrahmen verteilt sind. 

### Zweck
Der Hauptzweck von `merge.data.frame` besteht darin, zwei Datenrahmen zusammenzuführen, um eine umfassendere Datensatzansicht zu erhalten.

### Verwendung
Die grundlegende Syntax für die Verwendung von `merge.data.frame` ist wie folgt:

```R
merge(x, y, by = NULL, by.x = NULL, by.y = NULL, all = FALSE, all.x = FALSE, all.y = FALSE, sort = TRUE, suffixes = c(".x", ".y"), ...)
```

#### Parameter
- `x`: Der erste Datenrahmen.
- `y`: Der zweite Datenrahmen.
- `by`: Ein Vektor von Spaltennamen, die in beiden Datenrahmen übereinstimmen müssen.
- `by.x`: Ein Vektor von Spaltennamen in `x`, wenn diese anders benannt sind als in `y`.
- `by.y`: Ein Vektor von Spaltennamen in `y`, wenn diese anders benannt sind als in `x`.
- `all`: Wenn `TRUE`, werden alle Zeilen aus beiden Datenrahmen angezeigt, auch wenn keine Übereinstimmung vorliegt.
- `all.x`: Wenn `TRUE`, werden alle Zeilen aus `x` angezeigt, auch wenn keine Übereinstimmung in `y` vorliegt.
- `all.y`: Wenn `TRUE`, werden alle Zeilen aus `y` angezeigt, auch wenn keine Übereinstimmung in `x` vorliegt.
- `sort`: Wenn `TRUE`, werden die Ergebnisse nach dem Zusammenführungs-Schlüssel sortiert.
- `suffixes`: Ein Vektor von Suffixen, der zu den Spaltennamen hinzugefügt wird, wenn Namenskonflikte auftreten.

## Beispiele
Hier sind einige grundlegende Beispiele zur Verwendung von `merge.data.frame`:

### Beispiel 1: Einfaches Zusammenführen
```R
df1 <- data.frame(ID = 1:3, Name = c("Alice", "Bob", "Charlie"))
df2 <- data.frame(ID = 2:4, Alter = c(25, 30, 35))
result <- merge(df1, df2, by = "ID")
print(result)
```
**Ergebnis:**
```
  ID     Name Alter
1  2      Bob    25
2  3  Charlie    30
3  4    <NA>    35
```

### Beispiel 2: Zusammenführen ohne Übereinstimmungen
```R
df1 <- data.frame(ID = 1:3, Name = c("Alice", "Bob", "Charlie"))
df2 <- data.frame(ID = 4:5, Alter = c(30, 35))
result <- merge(df1, df2, by = "ID", all = TRUE)
print(result)
```
**Ergebnis:**
```
  ID     Name Alter
1  1    Alice <NA>
2  2      Bob <NA>
3  3  Charlie <NA>
4  4    <NA>    30
5  5    <NA>    35
```

## Erklärung
Ein häufiges Missverständnis bei der Verwendung von `merge.data.frame` ist die Annahme, dass es nur die Zeilen anzeigt, die in beiden Datenrahmen vorhanden sind. Wenn keine Übereinstimmungen vorhanden sind, müssen die Parameter `all`, `all.x` oder `all.y` entsprechend gesetzt werden, um alle Zeilen anzuzeigen. Es ist auch wichtig, die Spaltennamen sorgfältig zu überprüfen, da Namenskonflikte entstehen können. Um diese zu vermeiden, können die Suffixe angepasst werden.

## Ein-Satz-Zusammenfassung
Die Funktion `merge.data.frame` in R ermöglicht das effiziente Zusammenführen von Datenrahmen basierend auf gemeinsamen Variablen, was für die Analyse relationaler Daten unerlässlich ist.