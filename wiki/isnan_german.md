<!--
Meta Description: # is.nan: Überprüfung auf NaN-Werte in R ## Synopsis Die Funktion `is.nan` in R wird verwendet, um zu überprüfen, ob ein Wert oder ein Vektor NaN (Not...
Meta Keywords: nan, werte, ein, die, false
-->

# is.nan: Überprüfung auf NaN-Werte in R

## Synopsis
Die Funktion `is.nan` in R wird verwendet, um zu überprüfen, ob ein Wert oder ein Vektor NaN (Not a Number) ist. Dies ist besonders nützlich in der Datenanalyse, um ungültige oder nicht definierte Werte zu identifizieren.

## Dokumentation
Die Funktion `is.nan` gehört zur Basis-R-Programmiersprache und dient dazu, festzustellen, ob die Elemente eines Vektors oder einer Matrix NaN-Werte sind. NaN ist ein spezieller Wert in R, der häufig auftritt, wenn mathematische Operationen wie 0/0 durchgeführt werden.

### Verwendung
Die grundlegende Syntax der Funktion lautet:

```R
is.nan(x)
```

**Parameter:**
- `x`: Ein numerischer Vektor, eine Matrix oder ein Datenrahmen, dessen Elemente überprüft werden sollen.

**Rückgabewert:**
Die Funktion gibt einen logischen Vektor zurück, der für jedes Element von `x` angibt, ob es sich um einen NaN-Wert handelt (`TRUE`) oder nicht (`FALSE`).

### Details
- `is.nan` erkennt nur NaN-Werte und nicht andere fehlende Werte wie NA (Not Available).
- NaN wird oft verwendet, um das Ergebnis ungültiger mathematischer Berechnungen darzustellen.

## Beispiele
Hier sind einige grundlegende Beispiele zur Verwendung von `is.nan`:

```R
# Beispiel 1: Überprüfung eines einzelnen Wertes
value <- 0/0
is.nan(value)  # Gibt TRUE zurück, da value NaN ist

# Beispiel 2: Überprüfung eines Vektors
vec <- c(1, 2, NaN, 4, 0/0)
is.nan(vec)  # Gibt FALSE FALSE TRUE FALSE TRUE zurück

# Beispiel 3: Überprüfung einer Matrix
mat <- matrix(c(1, NaN, 3, 4), nrow = 2)
is.nan(mat)  # Gibt ein logisches Matrix zurück: FALSE TRUE FALSE FALSE
```

## Erklärung
Ein häufiges Missverständnis ist, dass `is.nan` und `is.na` oft verwechselt werden. Während `is.nan` ausschließlich NaN-Werte identifiziert, erkennt `is.na` sowohl NA- als auch NaN-Werte. Ein weiteres häufiges Problem tritt auf, wenn NaN-Werte nicht ordnungsgemäß behandelt werden, was zu unerwarteten Ergebnissen in Berechnungen führen kann.

Es ist wichtig zu beachten, dass NaN-Werte in Berechnungen propagiert werden. Das bedeutet, wenn Sie einen NaN-Wert in eine mathematische Operation einbeziehen, wird das Ergebnis ebenfalls NaN sein.

## Einzeiliger Überblick
Die Funktion `is.nan` in R identifiziert NaN-Werte in numerischen Vektoren und Matrizen und gibt einen logischen Vektor zurück, der angibt, ob die Elemente NaN sind.