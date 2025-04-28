<!--
Meta Description: # Die Funktion `is.finite` in R: Überprüfen von endlichen Werten ## Synopsis Die Funktion `is.finite` in R dient dazu, zu überprüfen, ob ein numerisch...
Meta Keywords: finite, werte, die, der, funktion
-->

# Die Funktion `is.finite` in R: Überprüfen von endlichen Werten

## Synopsis
Die Funktion `is.finite` in R dient dazu, zu überprüfen, ob ein numerischer Wert endlich ist oder nicht. Sie ist besonders nützlich, um sicherzustellen, dass Datenanalysen nur mit gültigen Werten durchgeführt werden.

## Dokumentation
### Zweck
Die Funktion `is.finite` prüft, ob die übergebenen Werte endlich sind. Ein Wert wird als endlich angesehen, wenn er nicht `NA`, `NaN` (Not a Number) oder unendlich (`Inf` oder `-Inf`) ist.

### Verwendung
Die allgemeine Syntax der Funktion lautet:

```R
is.finite(x)
```

#### Parameter
- `x`: Ein numerischer Vektor, eine Matrix oder ein Array, dessen Werte überprüft werden sollen.

#### Rückgabewert
Die Funktion gibt einen logischen Vektor zurück, der für jeden Wert in `x` angibt, ob dieser endlich ist (`TRUE`) oder nicht (`FALSE`).

### Details
`is.finite` ist besonders nützlich in der Datenbereinigung und bei der Datenanalyse, um sicherzustellen, dass nur gültige, endliche Werte in Berechnungen einfließen. Es ist eine der grundlegenden Funktionen, die in der Datenvorverarbeitung in R verwendet werden.

## Beispiele
Hier sind einige grundlegende Beispiele zur Verwendung der Funktion `is.finite`:

```R
# Beispiel 1: Einfache Verwendung
werte <- c(1, 2, Inf, -Inf, NaN, NA)
is.finite(werte)
# Ausgabe: TRUE TRUE FALSE FALSE FALSE FALSE

# Beispiel 2: Überprüfung eines Vektors
vektor <- c(3.5, 0, -7, NaN, 1/0)
is.finite(vektor)
# Ausgabe: TRUE TRUE TRUE FALSE FALSE
```

## Erklärung
Es gibt einige häufige Missverständnisse bezüglich der Funktion `is.finite`. 

- **NA-Werte**: `is.finite` behandelt `NA` als nicht endlich. Dies kann in Dataframes oder großen Datensätzen zu unerwarteten Ergebnissen führen, wenn man nicht darauf achtet.
- **NaN-Werte**: Jeder `NaN`-Wert wird ebenfalls als nicht endlich betrachtet. Dies ist wichtig zu beachten, wenn man mit mathematischen Funktionen arbeitet, die `NaN`-Werte erzeugen können.
- **Inf-Werte**: Sowohl positive als auch negative unendliche Werte werden als nicht endlich angesehen. Dies kann bei Divisionen oder anderen Berechnungen auftreten.

Beim Einsatz von `is.finite` in Datenanalysen sollte man darauf achten, dass alle relevanten Werte überprüft werden, um Fehler und unerwartete Ergebnisse zu vermeiden.

## Einzeiliger Zusammenfassung
Die Funktion `is.finite` in R überprüft, ob Werte endlich sind, und gibt einen logischen Vektor zurück, der die Endlichkeit jedes Wertes angibt.