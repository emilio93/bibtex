# Bibtex

Este repositorio cuenta con un archivo importante: `main.bib` el cual tiene una
lista de documentos(libros, articulos, etc) para su inclusión en archivos latex.

## Uso
Sea que se tenga la siguiente estructura:

```
+ mi-archivo.tex
+ bibtex\
  + LICENSE
  + main.bib
```

### Uso Básico

El archivo `mi-archivo.tex` puede usar la lista de documentos de la siguiente
manera:

```tex
\documentclass{article}

\usepackage{cite}
\usepackage{hyperref}

\begin{document}

  ``El muestreo es el proceso de seleccionar sistemáticamente elementos
  representativos de una población.'' \cite{kendall2012}.

  \bibliographystyle{plain}
  \bibliography{bibtex/main}

\end{document}
```

Si bien el paquete [hyperref](https://www.ctan.org/pkg/hyperref) no es
necesario, este crea enlaces accesibles en las versiones digitales del archivo
pdf que se crea.


### Usando APA con apacite

Para citar según el [estilo APA](http://www.apastyle.org/index.aspx),
se utiliza el paquete [apacite](https://www.ctan.org/pkg/apacite)
(`\usepackage{apacite}`), y se cambia el estilo de
bibliografía(`\bibliographystyle{apacite}`).

```tex
\documentclass{article}

\usepackage{cite}
\usepackage{apacite}
\usepackage{hyperref}

\begin{document}

  ``El muestreo es el proceso de seleccionar sistemáticamente elementos
  representativos de una población.'' \cite{kendall2012}.

  \bibliographystyle{apacite}
  \bibliography{bibtex/main}

\end{document}
```

### Compilando

Para compilar se deben correr los siguientes (4) comandos:
```
pdflatex mi-archivo
bibtex mi-archivo
pdflatex mi-archivo
pdflatex mi-archivo
```

### Más Información

Para más información sobre el uso visitar [LaTeX/Bibliography Management - Wikibooks, open books for an open world](https://en.wikibooks.org/wiki/LaTeX/Bibliography_Management).
