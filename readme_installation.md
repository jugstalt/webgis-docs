# Installation

Die Installation wird für die Einrichtung der Dokumentationsplattform mit Visual Studio Code (VSCode) beschreiben. VSCode ist das Werkzeug der Wahl, da es Syntax Highlighting und GIT Versionierung einfach ermöglicht.

Weitere notwendige Komponenten sind:

-   GIT (falls nicht schon mit VSCode mitgeliefert)
-   Python (getestet wurde mit Version 3.7)
-   Sphinx: Python Programm, dass aus ReST Dateien HTML erzeugt
-   Optionale Erweiterungen für VSCode (reStructuredText, German - Code Spell Checker)

## Visual Studio Code

Eine Setup Datei befindet sich unter https://code.visualstudio.com/Download

## Python

## Visual Studio Code Erweiterungen

Um Erweiterungen in VSCode zu installierten muss man auf das Extensions Symbol klicken. Über ein Suchfeld kann die richtige Erweiterung gefunden werden:

Screenshot

Es wird empfohlen die Python Erweiterung von Microsoft zu installieren.

Weitere nützliche Erweiterungen

-   **reStructuredText:** Syntax Highlighting für ReST Dateien (rudimentäre Vorschau)

-   **German - Code Spell Checker:** Rechtschreibprüfung. Falls beide gemeinsam genutzt werden, dann die reStructuredText deaktiviert werden, da sonst zu viel „Untersteichung“ im Text vorkommen kann.

Wie die einzelnen Erweiterungen aktiviert werden, kann in der jeweiligen Beschreibung nachgelesen werden. Dazu klickt man wieder auf das Extensions Werkzeug und danach auf eine der angezeigten installierten Erweiterungen

## Sphinx

Dient der Umwandlung von ReST Dateien in HTML.

Sphinx ist ein Python Programm und kann über die Python Package Manager (pip) installiert werden. Dazu ist in der Eingabeaufforderung folgender Befehl auszuführen.

```
pip install -U sphinx sphinx-autobuild
```

**_BEMERKUNG:_** Aus Eingabeaufforderung kann grundsätzlich die Eingabeaufforderung oder Powershell von Windows verwendet werden. Es besteht aber auch die Möglichkeit innerhalb von VSCode eine Eingabeaufforderung zu öffnen. Das erfolgt mit der Tastenkombination `Ctrl + ö`

Falls pip nicht gefunden wird, fehlt eventuell noch ein Verweise auf die Python Installation (und Python/Scripts) in der Umgebungsvariable `PATH`

Nach der Installation muss noch die Umgebungsvariable ``SPHINXBUILD`` auf die sphinx-build.exe gesetzt werden.
Der Installationspfad wird nach dem installieren von *sphinx* über *pip* angezeigt.

Weiters ist noch das entsprechende Layout für die Hilfe zu installieren. Das ist derzeit:

```
pip install piccolo-theme
```
und 
```
pip install sphinx_rtd_theme
```

## GIT

Ob die GIT Kommandozeilentools bereits funktioniern, kann überprüft werden, indem man `git` in ein Terminal Fenster eingibt. Ist Git noch nicht am Rechner vorhanden, findet man eine Setup Programm
auf der GIT Homepage

