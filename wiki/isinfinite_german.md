<!--
Meta Description: # is.infinite: Überprüfung auf unendliche Werte in R ## Synopsis Die Funktion `is.infinite` in R dient dazu, zu überprüfen, ob ein gegebener numerisch...
Meta Keywords: infinite, werte, die, funktion, false
-->

# is.infinite: Überprüfung auf unendliche Werte in R

## Synopsis
Die Funktion `is.infinite` in R dient dazu, zu überprüfen, ob ein gegebener numerischer Wert unendlich ist. Diese Funktion ist besonders nützlich, um unendliche Werte in Datenanalysen zu identifizieren und zu behandeln.

## Documentation
Die `is.infinite` Funktion gehört zur Basis-R-Bibliothek und hat das folgende Format:

```R
is.infinite(x)
```

### Zweck
Die Funktion wird verwendet, um festzustellen, ob die Elemente eines Vektors oder einer Matrix unendliche Werte (positive oder negative Unendlichkeit) sind. Dies ist wichtig, um bei Berechnungen oder Analysen mit unendlichen Werten umzugehen.

### Nutzung
- **Parameter:**
  - `x`: Ein numerischer Vektor, eine Matrix oder ein Array, dessen Elemente überprüft werden sollen.
  
- **Rückgabewert:**
  - `is.infinite` gibt einen logischen Vektor zurück, der `TRUE` für unendliche Werte und `FALSE` für alle anderen Werte enthält.

### Details
Die Funktion unterscheidet zwischen positiver und negativer Unendlichkeit. In R werden unendliche Werte durch `Inf` (positive Unendlichkeit) und `-Inf` (negative Unendlichkeit) repräsentiert. Die Funktion kann auch in Kombination mit anderen Funktionen verwendet werden, um Daten zu bereinigen oder spezifische Analysen durchzuführen.

## Examples
Hier sind einige grundlegende Beispiele zur Verwendung von `is.infinite`:

```R
# Beispiel 1: Überprüfung eines einzelnen Wertes
is.infinite(Inf)      # TRUE
is.infinite(-Inf)     # TRUE
is.infinite(10)       # FALSE

# Beispiel 2: Überprüfung eines Vektors
vec <- c(1, 2, Inf, -Inf, NA)
is.infinite(vec)      # FALSE FALSE TRUE TRUE FALSE

# Beispiel 3: Überprüfung einer Matrix
mat <- matrix(c(1, 2, Inf, -Inf), nrow = 2)
is.infinite(mat)      # FALSE FALSE TRUE TRUE
```

## Explanation
Ein häufiges Missverständnis besteht darin, dass `is.infinite` nur positive Werte überprüft. Tatsächlich erkennt die Funktion sowohl positive als auch negative unendliche Werte. Ein weiterer Punkt ist, dass `NA` (nicht verfügbar) nicht als unendlich betrachtet wird, weshalb `is.infinite(NA)` `FALSE` ergibt. Bei der Arbeit mit großen Datensätzen ist es wichtig, diese Funktion zu verwenden, um unendliche Werte zu identifizieren, die zu unerwarteten Ergebnissen führen können.

## One Line Summary
Die Funktion `is.infinite` in R ermöglicht die Überprüfung, ob numerische Werte unendlich sind, und ist somit ein wichtiges Werkzeug zur Datenbereinigung und -analyse.