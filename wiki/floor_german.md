<!--
Meta Description: # R-Befehl "floor": Runden von Zahlen auf die nächste ganze Zahl ## Synopsis Der `floor`-Befehl in R wird verwendet, um eine Zahl auf die nächstniedri...
Meta Keywords: die, floor, ist, zahl, der
-->

# R-Befehl "floor": Runden von Zahlen auf die nächste ganze Zahl

## Synopsis
Der `floor`-Befehl in R wird verwendet, um eine Zahl auf die nächstniedrigere ganze Zahl zu runden. Dies ist besonders nützlich in statistischen Berechnungen und Datenanalysen, wo die Umwandlung von Fließkommazahlen in ganze Zahlen erforderlich ist.

## Dokumentation
### Zweck
Der `floor`-Befehl ist eine Funktion in R, die alle Elemente eines numerischen Vektors auf die nächstniedrigere ganze Zahl abrundet. 

### Nutzung
Die grundlegende Syntax lautet:
```R
floor(x)
```
Hierbei ist `x` ein numerischer Vektor oder ein einzelner numerischer Wert, den Sie runden möchten.

### Details
- Der `floor`-Befehl gibt einen Vektor zurück, der die gerundeten Werte enthält.
- Es können Vektoren, Matrizen oder Arrays übergeben werden, und die Funktion wird auf jedes Element angewendet.
- Der Rückgabewert hat denselben Typ wie das Eingangsargument.

## Beispiele
```R
# Beispiel 1: Runden einer einzelnen Zahl
result1 <- floor(3.7)
print(result1)  # Ausgabe: 3

# Beispiel 2: Runden eines Vektors
result2 <- floor(c(1.2, 3.5, 4.8, 6.1))
print(result2)  # Ausgabe: 1 3 4 6

# Beispiel 3: Runden einer Matrix
matrix_input <- matrix(c(1.2, 3.5, 4.8, 6.1), nrow = 2)
result3 <- floor(matrix_input)
print(result3)
# Ausgabe:
#      [,1] [,2]
# [1,]    1    4
# [2,]    3    6
```

## Erklärung
Ein häufiger Fehler beim Einsatz von `floor` ist die Annahme, dass die Funktion mit nicht-numerischen Daten funktioniert. Wenn der Eingabewert kein numerischer Vektor ist, führt dies zu einem Fehler. Ein weiterer Punkt ist, dass `floor` immer auf die nächstniedrigere ganze Zahl rundet, auch wenn die Eingabe bereits eine ganze Zahl ist. In diesem Fall bleibt der Wert unverändert.

Zusätzlich ist es wichtig zu beachten, dass `floor` negative Zahlen ebenfalls abrundet. Beispielsweise wird `floor(-2.3` zu `-3`, was manchmal zu Verwirrung führen kann.

## Ein-Satz-Zusammenfassung
Der `floor`-Befehl in R rundet Zahlen auf die nächstniedrigere ganze Zahl und ist hilfreich für die Verarbeitung von numerischen Daten.