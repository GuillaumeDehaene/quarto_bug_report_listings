# Quarto bug report `Code listing does not format correctly`: example

This repository provides an example for the bug reported in [this issue](https://github.com/quarto-dev/quarto-cli/issues/7253).

To reproduce:

- render `example.qmd` with quarto:

    `quarto render example.qmd`
- or render `example.tex` with xelatex or another latex formatter (I've tested pdflatex and luatex):

    `xelatex example.tex`

As discussed in the issue, patching `example.tex` by modifying the definition of the `Shaded` environment by removing the `breakable` option fixes the issue.

- To reproduce, render `patched.tex` with xelatex:

    `xelatex patched.tex`
