<!--
Meta Description: # commandArgs in R: Parameterübergabe an R-Skripte ## Synopsis Die Funktion `commandArgs` in R ermöglicht es Benutzern, Befehlszeilenargumente an ein ...
Meta Keywords: die, commandargs, von, ein, ist
-->

# commandArgs in R: Parameterübergabe an R-Skripte

## Synopsis
Die Funktion `commandArgs` in R ermöglicht es Benutzern, Befehlszeilenargumente an ein R-Skript zu übergeben, was besonders nützlich für die Automatisierung von Skripten in der Datenanalyse und beim Erstellen von Programmen ist.

## Dokumentation
### Zweck
`commandArgs` wird verwendet, um Argumente, die beim Starten eines R-Skripts über die Befehlszeile übergeben wurden, zu erfassen. Dies ist besonders hilfreich, wenn Skripte in Batch-Prozessen oder von anderen Programmen aus aufgerufen werden, die spezifische Parameter benötigen.

### Verwendung
Die Funktion hat die Syntax:
```R
commandArgs(trailingOnly = FALSE)
```
- `trailingOnly`: Ein logischer Parameter, der angibt, ob nur die Argumente nach dem Skriptnamen zurückgegeben werden sollen (`TRUE`) oder alle Argumente einschließlich des Skriptnamens (`FALSE`). Standardwert ist `FALSE`.

### Details
- Die Rückgabe von `commandArgs` ist ein Vektor von Zeichenfolgen, der die übergebenen Argumente enthält.
- Bei Verwendung in RStudio oder interaktiven R-Sitzungen wird oft nur ein leeres Argument zurückgegeben, da die Standardumgebung keine Befehlszeilenargumente unterstützt.

## Beispiele
### Beispiel 1: Abrufen von Befehlszeilenargumenten
```R
args <- commandArgs(trailingOnly = TRUE)
print(args)
```
Wenn das Skript mit `Rscript mein_script.R arg1 arg2` aufgerufen wird, gibt es die Ausgabe:
```
[1] "arg1" "arg2"
```

### Beispiel 2: Verwendung von Argumenten
```R
args <- commandArgs(trailingOnly = TRUE)
if (length(args) < 1) {
  stop("Bitte mindestens ein Argument angeben.")
}
input_file <- args[1]
print(paste("Eingabedatei:", input_file))
```
Beim Aufruf mit `Rscript mein_script.R daten.csv` wird ausgegeben:
```
[1] "Eingabedatei: daten.csv"
```

## Erklärung
Ein häufiges Problem beim Arbeiten mit `commandArgs` ist, dass bei der Ausführung in interaktiven R-Sitzungen keine Argumente verfügbar sind. Um diese Funktion effektiv zu nutzen, sollte das Skript über die Kommandozeile (z.B. mit `Rscript`) ausgeführt werden. Außerdem ist es wichtig, die Argumente ordnungsgemäß zu prüfen, um sicherzustellen, dass das Skript nicht mit unzureichenden Eingaben fehlschlägt.

## Zusammenfassung in einem Satz
Die `commandArgs`-Funktion in R ermöglicht die einfache Übergabe und Verarbeitung von Befehlszeilenargumenten in R-Skripten.