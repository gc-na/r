<!--
Meta Description: # R-Befehl: list.files – Dateien in einem Verzeichnis auflisten ## Synopsis Der Befehl `list.files` in R ermöglicht es Benutzern, eine Liste von Datei...
Meta Keywords: der, dateien, die, files, list
-->

# R-Befehl: list.files – Dateien in einem Verzeichnis auflisten

## Synopsis
Der Befehl `list.files` in R ermöglicht es Benutzern, eine Liste von Dateien in einem bestimmten Verzeichnis abzurufen. Dies ist besonders nützlich für die Datenanalyse und -verarbeitung, da es eine einfache Möglichkeit bietet, auf Dateiinhalte zuzugreifen.

## Dokumentation
### Zweck
Der Befehl `list.files` wird verwendet, um die Namen der Dateien in einem angegebenen Verzeichnis zurückzugeben. Benutzer können zusätzliche Parameter angeben, um die Suche einzuschränken und spezifische Dateitypen oder Muster zu filtern.

### Nutzung
Die grundlegende Syntax des Befehls lautet:

```R
list.files(path = ".", pattern = NULL, all.files = FALSE, full.names = FALSE, recursive = FALSE, ignore.case = FALSE, include.dirs = FALSE, no.. = FALSE)
```

#### Parameter
- `path`: Der Pfad des Verzeichnisses, aus dem die Dateien aufgelistet werden sollen. Standardmäßig ist dies das aktuelle Arbeitsverzeichnis (`"."`).
- `pattern`: Ein regulärer Ausdruck, der verwendet wird, um die zurückgegebenen Dateinamen zu filtern. Nur Dateien, deren Namen dem Muster entsprechen, werden aufgelistet.
- `all.files`: Ein logischer Wert (TRUE oder FALSE), der angibt, ob alle Dateien (einschließlich versteckter Dateien) zurückgegeben werden sollen. Standardmäßig ist dies FALSE.
- `full.names`: Ein logischer Wert, der angibt, ob der vollständige Pfad der Dateien zurückgegeben werden soll (TRUE) oder nur die Dateinamen (FALSE).
- `recursive`: Ein logischer Wert, der angibt, ob die Suche auch in Unterverzeichnissen erfolgen soll. Standardmäßig ist dies FALSE.
- `ignore.case`: Ein logischer Wert, der angibt, ob die Groß-/Kleinschreibung bei der Mustererkennung ignoriert werden soll.
- `include.dirs`: Ein logischer Wert, der angibt, ob Verzeichnisse in die Auflistung einbezogen werden sollen.
- `no..`: Ein logischer Wert, der angibt, ob die Verzeichniseinträge "." und ".." ausgeschlossen werden sollen.

## Beispiele
Hier sind einige grundlegende Beispiele zur Verwendung von `list.files`:

1. **Auflisten aller Dateien im aktuellen Verzeichnis:**
   ```R
   list.files()
   ```

2. **Auflisten aller .csv-Dateien im aktuellen Verzeichnis:**
   ```R
   list.files(pattern = "\\.csv$")
   ```

3. **Auflisten aller Dateien im Verzeichnis `/home/user/data` mit vollständigen Pfadangaben:**
   ```R
   list.files(path = "/home/user/data", full.names = TRUE)
   ```

4. **Auflisten aller Dateien in Unterverzeichnissen:**
   ```R
   list.files(recursive = TRUE)
   ```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von `list.files` ist die Unsicherheit über den richtigen regulären Ausdruck im `pattern`-Parameter. Benutzer sollten sicherstellen, dass sie den regulären Ausdruck korrekt formulieren, um die gewünschten Dateien zu filtern. Zudem kann die Verwendung von `full.names = TRUE` nützlich sein, wenn der Speicherort der Dateien für die weitere Verarbeitung benötigt wird. 

Ein weiterer Punkt ist, dass versteckte Dateien (z. B. Dateien, die mit einem Punkt beginnen) nicht angezeigt werden, es sei denn, `all.files` ist auf TRUE gesetzt. Benutzer sollten auch beachten, dass bei der Verwendung von `recursive = TRUE` eine große Anzahl von Dateien zurückgegeben werden kann, was die Verarbeitung verlangsamen kann.

## Ein Satz Zusammenfassung
Der Befehl `list.files` in R ist ein leistungsfähiges Werkzeug, um gezielt Dateien aus einem Verzeichnis zu listen und zu filtern.