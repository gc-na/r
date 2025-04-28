<!--
Meta Description: # R dir.create: Verzeichnis erstellen in R ## Synopsis Der Befehl `dir.create` in R wird verwendet, um neue Verzeichnisse (Ordner) im Dateisystem zu e...
Meta Keywords: verzeichnis, dir, create, ein, der
-->

# R dir.create: Verzeichnis erstellen in R

## Synopsis
Der Befehl `dir.create` in R wird verwendet, um neue Verzeichnisse (Ordner) im Dateisystem zu erstellen. Er ist besonders nützlich für das Organisieren von Projekten und Daten.

## Dokumentation
### Zweck
Der Befehl `dir.create` ermöglicht es Benutzern, ein neues Verzeichnis zu erstellen, wenn es noch nicht existiert. Dies ist nützlich, um eine strukturierte Ordnerhierarchie für Datenanalysen und Skripte zu schaffen.

### Verwendung
Die grundlegende Syntax des Befehls lautet:

```R
dir.create(path, showWarnings = TRUE, recursive = FALSE, mode = "0777")
```

#### Parameter
- **path**: Ein Zeichenvektor, der den Pfad des zu erstellenden Verzeichnisses angibt.
- **showWarnings**: Ein logischer Wert (TRUE/FALSE), der angibt, ob Warnungen angezeigt werden sollen, wenn das Verzeichnis bereits existiert.
- **recursive**: Ein logischer Wert (TRUE/FALSE), der angibt, ob alle übergeordneten Verzeichnisse, die möglicherweise nicht existieren, ebenfalls erstellt werden sollen.
- **mode**: Ein Zeichen, das die Berechtigungen für das neue Verzeichnis festlegt (Standard ist "0777").

### Details
Der Befehl `dir.create` gibt TRUE zurück, wenn das Verzeichnis erfolgreich erstellt wurde, und FALSE, wenn nicht. Es ist wichtig zu beachten, dass bei aktivierter `recursive`-Option auch alle übergeordneten Verzeichnisse erstellt werden, falls sie nicht existieren. 

## Beispiele
### Einfaches Verzeichnis erstellen
```R
dir.create("mein_verzeichnis")
```
Dieses Beispiel erstellt ein Verzeichnis mit dem Namen "mein_verzeichnis" im aktuellen Arbeitsverzeichnis.

### Verzeichnis mit Warnungen
```R
dir.create("mein_verzeichnis", showWarnings = TRUE)
```
Hier wird ein Verzeichnis erstellt, und es werden Warnungen angezeigt, wenn das Verzeichnis bereits existiert.

### Rekursive Verzeichnisstruktur erstellen
```R
dir.create("hauptordner/unterordner", recursive = TRUE)
```
In diesem Beispiel wird sowohl "hauptordner" als auch "unterordner" erstellt, wenn sie nicht existieren.

### Berechtigungen festlegen
```R
dir.create("sicherer_ordner", mode = "0755")
```
Dies erstellt ein Verzeichnis mit spezifischen Berechtigungen.

## Erklärung
Beim Arbeiten mit `dir.create` können einige häufige Fallstricke auftreten:

- **Existierendes Verzeichnis**: Wenn ein Verzeichnis mit dem angegebenen Namen bereits existiert und `showWarnings` auf TRUE gesetzt ist, wird eine Warnmeldung angezeigt. Ansonsten wird keine Aktion durchgeführt.
- **Berechtigungen**: Das Festlegen von Berechtigungen funktioniert möglicherweise nicht wie erwartet, abhängig vom Betriebssystem und den Benutzerberechtigungen.
- **Falscher Pfad**: Bei der Angabe eines relativen Pfades sollte darauf geachtet werden, dass der aktuelle Arbeitsordner korrekt gesetzt ist. Andernfalls wird das Verzeichnis möglicherweise an einem unerwarteten Ort erstellt.

## Ein-Satz-Zusammenfassung
Der Befehl `dir.create` in R wird verwendet, um neue Verzeichnisse zu erstellen, wobei Benutzer die Möglichkeit haben, Warnungen anzuzeigen und rekursive Strukturen zu erstellen.