# CV

LaTeX source files and generated PDF versions of my CV.

## PDF

- [English CV](en/en_cv.pdf)
- [Russian CV](ru/ru_cv.pdf)

## Structure

```text
en/
  en_cv.tex
  en_cv.pdf
ru/
  ru_cv.tex
  ru_cv.pdf
```

## Build

Requirements:

- MiKTeX or TeX Live
- `latexmk`
- XeLaTeX for the Russian version
- Libertinus fonts for the Russian version

Build the English CV:

```powershell
latexmk -pdf -interaction=nonstopmode -file-line-error -outdir=en -auxdir=en en/en_cv.tex
```

Build the Russian CV:

```powershell
latexmk -xelatex -interaction=nonstopmode -file-line-error -outdir=ru -auxdir=ru ru/ru_cv.tex
```

Generated LaTeX auxiliary files are ignored by Git.
