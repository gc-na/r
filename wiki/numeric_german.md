<!--
Meta Description: # Numerische Daten in R: Ein umfassender Überblick über den Datentyp "numeric" ## Synopsis Der Datentyp "numeric" in R ist der Standarddatentyp für nu...
Meta Keywords: numeric, der, und, die, ein
-->

# Numerische Daten in R: Ein umfassender Überblick über den Datentyp "numeric"

## Synopsis
Der Datentyp "numeric" in R ist der Standarddatentyp für numerische Werte und ermöglicht die Durchführung von mathematischen Berechnungen und statistischen Analysen.

## Dokumentation
Der "numeric"-Datentyp in R wird verwendet, um Gleitkommazahlen (d.h. reelle Zahlen) darzustellen. In R ist es wichtig, zwischen verschiedenen Datentypen zu unterscheiden, da sie unterschiedliche Eigenschaften und Verhaltensweisen aufweisen. Der "numeric"-Datentyp wird häufig in mathematischen Berechnungen, statistischen Modellierungen und Datenauswertungen verwendet.

### Verwendung
Um einen numerischen Vektor in R zu erstellen, kann die Funktion `c()` (combine) verwendet werden. Ein Beispiel für die Erstellung eines numerischen Vektors:

```R
zahlen <- c(1.5, 2.3, 3.7)
```

In diesem Beispiel wird ein numerischer Vektor mit drei Gleitkommazahlen erstellt. R unterstützt sowohl Ganzzahlen als auch Gleitkommazahlen innerhalb des "numeric"-Datentyps. Ganzzahlen können auch explizit als solche deklariert werden, indem man ein "L" an die Zahl anfügt:

```R
ganzzahlen <- c(1L, 2L, 3L)
```

### Details
- **Standardwert**: Der Standardwert für numerische Werte in R ist Gleitkommazahl (double precision).
- **Präzision**: Die numerische Präzision in R kann von der Plattform abhängen, jedoch werden Gleitkommazahlen in der Regel mit 15 bis 16 Dezimalstellen gespeichert.
- **Arithmetische Operationen**: Numerische Vektoren unterstützen eine Vielzahl von arithmetischen Operationen wie Addition, Subtraktion, Multiplikation und Division.

## Beispiele
Hier sind einige grundlegende Beispiele zur Verwendung des "numeric"-Datentyps in R:

```R
# Erstellen eines numerischen Vektors
numerischer_vektor <- c(10.5, 20.3, 30.1)

# Arithmetische Operationen
summe <- sum(numerischer_vektor) # Summe
produkt <- prod(numerischer_vektor) # Produkt

# Ausgabe
print(summe)    # Ausgabe: 61.0
print(produkt)  # Ausgabe: 6361.515
```

## Erklärung
Ein häufiger Fehler, den Anfänger machen, ist die Verwechslung von "numeric" und "integer". Während "numeric" Gleitkommazahlen beinhaltet, sind "integer" nur Ganzzahlen. Um sicherzustellen, dass Sie den gewünschten Datentyp verwenden, überprüfen Sie immer den Typ mit der `class()` Funktion:

```R
class(numerischer_vektor) # Gibt "numeric" zurück
```

Die Verwendung von numerischen Werten in R kann auch zu Rundungsfehlern führen, insbesondere bei sehr großen oder sehr kleinen Zahlen. Es ist wichtig, diese Faktoren bei der Durchführung präziser Berechnungen zu berücksichtigen.

## Ein-Satz-Zusammenfassung
Der "numeric"-Datentyp in R ist essenziell für die Verarbeitung von reellen Zahlen und bietet umfangreiche Möglichkeiten für mathematische und statistische Operationen.