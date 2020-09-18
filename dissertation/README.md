# Dissertation

Source files and figures for the dissertation. The PDF is built using
[LaTeX](https://en.wikipedia.org/wiki/LaTeX) from the `.tex` source file.

Learn more about LaTeX and how to use it to write documents from the [Overleaf
tutorial](https://www.overleaf.com/learn/latex/Main_Page).

## Installing LaTeX

### Linux

Install the `texlive` package from your system's package manager.

### Windows

Download and install [MikTex](https://miktex.org/).

## Building the PDF

To generate a PDF from the LaTeX source files, run the following in a terminal
(or Git Bash on Windows):

```
latexmk -pv -pdf dissertation.tex
```
