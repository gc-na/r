<!--
Meta Description: # ifelse in R: Bedingte Logik einfach umgesetzt ## Synopsis Die Funktion `ifelse` in R ermöglicht die Durchführung von bedingten Abfragen und die Rück...
Meta Keywords: die, ifelse, der, ist, funktion
-->

# ifelse in R: Bedingte Logik einfach umgesetzt

## Synopsis
Die Funktion `ifelse` in R ermöglicht die Durchführung von bedingten Abfragen und die Rückgabe von Werten basierend auf dem Ergebnis dieser Abfragen. Sie ist besonders nützlich, um vektorisierte Operationen durchzuführen, die eine schnelle Verarbeitung großer Datenmengen ermöglichen.

## Dokumentation
### Zweck
Die `ifelse`-Funktion wird verwendet, um Bedingungen zu überprüfen und unterschiedliche Werte zurückzugeben, abhängig davon, ob die Bedingung wahr oder falsch ist. Sie ist eine vektorisierte Alternative zu den klassischen `if`-Bedingungen, die in R verwendet werden.

### Verwendung
Die allgemeine Syntax der `ifelse`-Funktion lautet:

```R
ifelse(test, yes, no)
```

- **test**: Ein logischer Vektor, der angibt, welche Bedingungen wahr sind.
- **yes**: Der Wert, der zurückgegeben wird, wenn die Bedingung wahr ist.
- **no**: Der Wert, der zurückgegeben wird, wenn die Bedingung falsch ist.

### Details
Die `ifelse`-Funktion ist sehr effizient, da sie die Operationen auf alle Elemente eines Vektors gleichzeitig anwendet. Dies ist besonders wichtig in Datenanalysen, wo große Datenmengen verarbeitet werden müssen. Die Funktion gibt einen Vektor zurück, der die gleiche Länge wie der Eingangstest hat.

## Beispiele
### Einfaches Beispiel
```R
x <- c(5, 10, 15, 20)
result <- ifelse(x > 10, "größer als 10", "10 oder kleiner")
print(result)
```

### Beispiel mit NA-Werten
```R
y <- c(1, 2, NA, 4)
result_na <- ifelse(is.na(y), "NA gefunden", y)
print(result_na)
```

### Beispiel mit numerischen Rückgaben
```R
z <- c(3, -2, 0, 4)
result_numeric <- ifelse(z > 0, z * 2, z - 2)
print(result_numeric)
```

## Erklärung
Ein häufiges Problem bei der Verwendung von `ifelse` ist der Umgang mit NA-Werten. Wenn der Test NA zurückgibt, wird auch der gesamte Rückgabewert NA sein. Es ist wichtig, sicherzustellen, dass die Tests korrekt durchgeführt werden, um unerwartete Ergebnisse zu vermeiden.

Ein weiterer Aspekt ist die Leistung: Bei sehr großen Vektoren kann `ifelse` schneller sein als verschachtelte `if`-Anweisungen, da es die Vektorisierung nutzt. Dennoch sollte man bei komplexeren Bedingungen überlegen, ob eine andere Methode wie `dplyr::mutate` nicht sinnvoller wäre.

## Ein-Satz-Zusammenfassung
Die `ifelse`-Funktion in R ermöglicht eine effiziente und vektorisierte Auswertung von Bedingungen mit unterschiedlichen Rückgabewerten für wahre und falsche Ergebnisse.