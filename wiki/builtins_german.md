<!--
Meta Description: # Builtins in R: Eingebaute Funktionen und deren Verwendung ## Synopsis In R beziehen sich "Built-ins" auf eine Sammlung von integrierten Funktionen, ...
Meta Keywords: die, built, ins, funktionen, von
-->

# Builtins in R: Eingebaute Funktionen und deren Verwendung 

## Synopsis
In R beziehen sich "Built-ins" auf eine Sammlung von integrierten Funktionen, die sofort verfügbar sind, ohne dass zusätzliche Pakete geladen werden müssen. Diese Funktionen sind essenziell für die Datenanalyse und -manipulation.

## Documentation
Die Builtins in R sind vordefinierte Funktionen, die in der Basisinstallation von R enthalten sind. Sie decken eine breite Palette von Operationen ab, von mathematischen Berechnungen über Datenmanipulation bis hin zu statistischen Analysen. Zu den bekanntesten Built-ins gehören Funktionen wie `sum()`, `mean()`, `sd()`, `lm()`, und `plot()`. 

### Zweck
Die Built-ins dienen dazu, häufig verwendete Operationen effizient und benutzerfreundlich anzubieten. Sie ermöglichen es Benutzern, komplexe Berechnungen in wenigen Zeilen Code durchzuführen.

### Verwendung
Die Verwendung einer Built-in-Funktion erfolgt in der Regel durch den Aufruf des Funktionsnamens, gefolgt von Klammern, die die Argumente enthalten. Zum Beispiel:

```R
mean(c(1, 2, 3, 4, 5))
```

Diese Zeile berechnet den Durchschnitt der angegebenen Zahlen.

## Examples
Hier sind einige grundlegende Beispiele für die Verwendung von Built-ins in R:

1. **Summe berechnen**
   ```R
   result <- sum(c(1, 2, 3, 4, 5))
   print(result)  # Ausgabe: 15
   ```

2. **Durchschnitt berechnen**
   ```R
   avg <- mean(c(10, 20, 30))
   print(avg)  # Ausgabe: 20
   ```

3. **Lineare Regression**
   ```R
   model <- lm(mpg ~ wt, data = mtcars)
   summary(model)
   ```

4. **Daten visualisieren**
   ```R
   plot(mtcars$wt, mtcars$mpg)
   ```

## Explanation
Obwohl Built-ins in R sehr nützlich sind, gibt es einige häufige Fallstricke. 

- **Typen von Argumenten**: Viele Built-ins erwarten bestimmte Argumenttypen. Zum Beispiel kann die Funktion `mean()` nicht auf nicht-numerische Daten angewendet werden, ohne einen Fehler auszulösen.

- **Fehlende Werte**: Einige Funktionen, wie `sum()`, geben bei fehlenden Werten (`NA`) möglicherweise unerwartete Ergebnisse zurück. Um dies zu vermeiden, sollten Sie `na.rm = TRUE` verwenden:

  ```R
  sum(c(1, 2, NA), na.rm = TRUE)  # Ausgabe: 3
  ```

- **Rückgabewerte**: Beachten Sie, dass nicht alle Built-ins einen Wert zurückgeben, den Sie direkt verwenden können. Einige, wie `plot()`, erzeugen nur eine grafische Ausgabe.

## One Line Summary
Built-ins in R sind integrierte Funktionen, die grundlegende Datenmanipulation und Analyse ohne zusätzliche Pakete ermöglichen.