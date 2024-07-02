Das LaTeX-Dokument generiert die Druckversion der Ersti-Info-Vorlage.
Um die digitale Variante der Ersti-Info-Vorlage zu erstellen, empfiehlt es sich, die folgenden Befehle in einem Linux-Terminal auszuführen:
```
gs -o cropped.pdf -sDEVICE=pdfwrite -dAutoRotatePages=/None -c "[/CropBox [8.5 8.5 428 603.7]" -c " /PAGES pdfmark" -f main.pdf
```
```
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/prepress -dEmbedAllFonts=true -dAutoRotatePages=/None -dNOPAUSE -dQUIET -dBATCH -sOutputFile=Ersti-Info23.pdf cropped.pdf
```

Der als gestrichelte Linie angezeigte Rahmen dient als Orientierung, wo im Druck die Seiten ungefähr abgeschnitten werden.
Dieser lässt sich ausblenden, in dem man in der `commands.tex` die zweite Definition des Druckrands entkommentiert.