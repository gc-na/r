<!--
Meta Description: # Datei umbenennen in R: Die Funktion file.rename ## Synopsis Die Funktion `file.rename` in R ermöglicht das Umbenennen von Dateien oder Verzeichnisse...
Meta Keywords: die, umbenennen, file, rename, oder
-->

# Datei umbenennen in R: Die Funktion file.rename

## Synopsis
Die Funktion `file.rename` in R ermöglicht das Umbenennen von Dateien oder Verzeichnissen im Dateisystem. Diese Funktion ist einfach zu nutzen und spielt eine wichtige Rolle beim Dateimanagement in R.

## Dokumentation
### Zweck
Die Funktion `file.rename` wird verwendet, um eine oder mehrere Dateien oder Verzeichnisse in R umzubenennen. Sie ist besonders nützlich für die Organisation von Daten und die Verwaltung von Dateinamen in Skripten.

### Verwendung
Die grundlegende Syntax der Funktion lautet:

```R
file.rename(from, to)
```

#### Parameter
- **from**: Ein Vektor von Dateipfaden, der die aktuellen Namen der Dateien oder Verzeichnisse enthält.
- **to**: Ein Vektor von Dateipfaden, der die neuen Namen der Dateien oder Verzeichnisse enthält.

Beide Parameter müssen die gleiche Länge haben, da jeder Name im `from`-Vektor einem entsprechenden Namen im `to`-Vektor zugeordnet werden muss.

### Details
- Die Funktion gibt einen logischen Vektor zurück, der angibt, ob das Umbenennen für jede angegebene Datei oder jedes Verzeichnis erfolgreich war.
- Falls eine Datei oder ein Verzeichnis nicht existiert oder der Benutzer keine Berechtigung hat, wird `FALSE` zurückgegeben.
- `file.rename` kann sowohl für Dateien als auch für Verzeichnisse verwendet werden.

## Beispiele
### Beispiel 1: Einzelnes Umbenennen
```R
# Umbenennen einer einzelnen Datei
file.rename("alte_datei.txt", "neue_datei.txt")
```

### Beispiel 2: Mehrfaches Umbenennen
```R
# Umbenennen mehrerer Dateien
alte_namen <- c("alte_datei1.txt", "alte_datei2.txt")
neue_namen <- c("neue_datei1.txt", "neue_datei2.txt")
file.rename(alte_namen, neue_namen)
```

### Beispiel 3: Umbenennen eines Verzeichnisses
```R
# Umbenennen eines Verzeichnisses
file.rename("altes_verzeichnis", "neues_verzeichnis")
```

## Erklärung
Ein häufiges Problem bei der Verwendung von `file.rename` ist, dass der Pfad zur Datei nicht korrekt angegeben wird. Stellen Sie sicher, dass Sie die vollständigen Pfade verwenden, insbesondere wenn sich die Dateien nicht im aktuellen Arbeitsverzeichnis befinden.

Ein weiterer Fall ist, dass das Ziel bereits existiert. In diesem Fall wird die Funktion nicht erfolgreich sein. Achten Sie darauf, dass die neuen Namen noch nicht vergeben sind, um Konflikte zu vermeiden.

Falls Sie eine Datei umbenennen möchten, die von einem R-Skript verwendet wird, stellen Sie sicher, dass sie nicht geöffnet ist oder von einem anderen Prozess blockiert wird.

## Einzeiliger Überblick
Die Funktion `file.rename` in R bietet eine einfache Möglichkeit, Dateien und Verzeichnisse im Dateisystem umzubenennen.