# hausarbeit-jura
```
----------------------------------------------------------------------------
hausarbeit-jura -- A LaTeX class for writing “juristische Hausarbeiten” at German universities.

(c) 2012–2020 Martin Sievers
Version:    2.1.0
Maintainer: Martin Sievers
Email:      martin.sievers@schoenerpublizieren.de
License:    Released under the LaTeX Project Public License v1.3c or later
See:        http://www.latex-project.org/lppl.txt
----------------------------------------------------------------------------

This is the current version of the class “hausarbeit-jura” for
writing “juristische Hausarbeiten” at German universities. It
was originally developed for a workshop at Trier University.

The idea is to make the usage of LaTeX easier as only a few macros and
environments are needed.

The documentation is in German only.

Stable versions are always uploaded to CTAN. You'll find the most recent developer version on GitHub.
```

https://github.com/sieversMartin/hausarbeit-jura


## Changelog

### Changes from the forked version

Die .bib-Datei ist von [biblatex-jura2](https://ctan.org/pkg/biblatex-jura2)
übernommen, zusammen in der .tex-Datei mit den Beispielzitierungen aus der
Dokumentation. Die Originaldateien sind unter dem angegebenen Link zu finden.
Dies ersetzt nicht biblatex-jura2, es soll zeigen, wie dieser biblatex-Style mit
der Dokumentklasse hausarbeit-jura2 eingesetzt werden kann.

`Microtype` wird in der .tex-Datei gesetzt, damit man auch mit XeTeX kompilieren
kann, ohne die Klasse lokal zu ändern. Das muss noch manuell auskommentiert
werden, wenn XeTex benutzt werden soll, es ist noch nicht automatisiert.

In die .tex-Datei sind viele Änderungsmöglichkeiten in die Präambel eingepflegt,
die es vor allem Anfängern ermöglichen sollen, einen einfacheren Zugang zu LaTeX
zu finden und das Dokument ihren Anforderungen gemäß anzupassen. 

Probleme:
* Für LuaLaTex muss die Klasse `jurabook` lokal an vier Stellen geändert werden.
    * In `jurabook.cls` jeweils inkompatibles Zeichen mit `§` ersetzen, Zeilen:
	    * 1087
	    * 1097
	    * 1692
	    * 1705
    * Eigentlich ist es auch ein §, wird aber nicht als solches erkannt.
    * Die Datei muss danach gespeichert werden.
* Die Änderung des Zeilenabstandes funktioniert, ist aber nicht schön umgesetzt.
  Es wäre schön, wenn sich das besser umsetzen ließe, vor allem auch, wenn für
  das Inhaltsverzeichnis und die Bibliographie und den Hauptteil ein
  unterschiedlicher Zeilenabstand gewählt werden könnte.
* Wenn die Bibliographie vor den Hauptteil gesetzt wird, muss die Seitenzahl
  noch manuell gesetzt werden.



### [2.1.0] -- 2020-08-06

* Resolve issue with `latexrelease` and `textcomp`

### [2.0.0]

* Made class compatible to latest LaTeX versions
* Added new options `10bp`, `11bp` and `12bp` for Word-compatible font sizes
* Added new options `10pt`, `11pt` and `12pt` for LaTeX-compatible font sizes
* Made `12bp` the new standard font size

### [1.5.0]

* Added ``\sectionbefore`` and ``\sectionafter`` to ``\section`` as well
* Added macros ``\setspacebeforechapter``, ``\setspaceafterchapter``, ``\setspacebeforesection`` and ``\setspaceaftersection``
* Added option ``noautomatter`` to deactivate automatic usage of ``\frontmatter`` and ``\mainmatter``

### [1.4.0]

* Added macros to change paper size used in frontmatter and mainmatter (suggested by Adi Sander)
* Added definition for ``\subsubsection``
* Modifed ``microtype`` options

### [1.3.0]

* Fixed a bug (missing ``\fi``)
* Added option ``headlinetitlepageleft``
* Added package ``ellipsis``

### [1.2.0]

* Added option ``headline`` (thanks to Tobias Hirning) to add information to the header
* TeX Gyre Fonts are now the standard fonts; added new option ``oldfonts`` for compatibility
* added support for XeLaTeX and LuaLaTeX
* rearranged package (not only) for GitHub
* code cleaning and improvement

### [1.1.0]

* added a documentation
* modified demo file

### [1.0.1]

* dtx now extracts “README.txt” instead of “README”.
* code cleaning of the dtx file

### [1.0.0]

* First “official” version, still without documentation
