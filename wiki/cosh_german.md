<!--
Meta Description: # cosh in R: Hyperbolische Kosinusfunktion ## Synopsis Die Funktion `cosh` in R berechnet den hyperbolischen Kosinus eines gegebenen Wertes oder eines...
Meta Keywords: cosh, der, kosinus, funktion, von
-->

# cosh in R: Hyperbolische Kosinusfunktion

## Synopsis
Die Funktion `cosh` in R berechnet den hyperbolischen Kosinus eines gegebenen Wertes oder eines Vektors von Werten. Sie ist Teil der Basisfunktionen für mathematische Berechnungen in R und wird häufig in der Analyse von hyperbolischen Funktionen verwendet.

## Dokumentation
Die Funktion `cosh` wird verwendet, um den hyperbolischen Kosinus eines Wertes zu berechnen. Der hyperbolische Kosinus wird definiert als:

\[
\cosh(x) = \frac{e^x + e^{-x}}{2}
\]

### Verwendung
```R
cosh(x)
```

### Parameter
- `x`: Ein numerischer Wert oder ein Vektor von Werten, für den der hyperbolische Kosinus berechnet werden soll.

### Rückgabewert
Die Funktion gibt den hyperbolischen Kosinus von `x` zurück, der als numerischer Wert oder Vektor formatiert ist, abhängig von der Eingabe.

## Beispiele
Hier sind einige grundlegende Anwendungsbeispiele für die Funktion `cosh`:

```R
# Einzelner Wert
result_single <- cosh(0)
print(result_single)  # Ausgabe: 1

# Vektor von Werten
values <- c(0, 1, 2, 3)
result_vector <- cosh(values)
print(result_vector)  # Ausgabe: [1] 1.000000 1.543081 3.762198 10.067662
```

## Erklärung
Ein häufiges Missverständnis bei der Verwendung der `cosh`-Funktion ist, dass sie mit der klassischen Kosinusfunktion `cos` verwechselt wird. Es ist wichtig zu beachten, dass `cosh` den hyperbolischen Kosinus berechnet, der andere mathematische Eigenschaften aufweist als der trigonometrische Kosinus.

Ein weiterer Punkt ist, dass die Eingaben für `cosh` sowohl positive als auch negative Werte annehmen können, da der hyperbolische Kosinus eine gerade Funktion ist, d.h. `cosh(-x) = cosh(x)`.

## Einzeiliger Überblick
Die Funktion `cosh` in R berechnet den hyperbolischen Kosinus eines Wertes oder Vektors von Werten.