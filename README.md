# Vorlage verwenden
Pflichtangaben und einigen weitere Einstellungen können in `einstellungen.tex` geändert werden. Kapitel werden in `content` nach dem Schema `<nn>kapitel.tex` abgespeichert, wobei <nn> eine mindestens zweistellige Zahl sein muss.

## Bauen
Entweder über latexmk:
* Bauen: `latexmk`
* Aufräumen: `latexmk -c`

Oder über das makefile (verwendet latexmk):
* Bauen: `make`
* Aufräumen:
  * `make clean` (entfernt output/, dokumentation.pdf und dokumentation.synctex.gz)
  * `make cleanup` (gleich wie latexmk -c)

# Ordnerstruktur
* ads/ - enthält die notwendigen Seiten, z.B. Abstract, Deckblatt etc., sowie einige Interna
* content/ - enthält pro Kapitel eine Datei (Schema: `<nn>kapitel.tex`
* dokumentation.tex - die Hauptdatei, die alles andere einbindet
* latexmkrc - die Regeln, nach denen latexmk das Dokument baut
* images/
* einstellungen.tex - hier werden z.B. die Pflichtangaben auf dem Deckblatt geändert

# Nur Deckblatt verwenden
```
\usepackage{pdfpages}
% .....
\includepdf[pages=1]{../latexVorlage/output/dokumentation.pdf}
```
