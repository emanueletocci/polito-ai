# Lab 1 report — LaTeX sources

Overleaf-ready sources for the Lab 1 project report. Nothing here has been
compiled: upload the folder and let Overleaf build it.

## Files

```
report/
├── main.tex            # the whole report, single file
├── figures/            # the 7 PNG figures included by main.tex
└── README.md
```

`main.tex` is self-contained apart from `figures/`. The logbook
(Appendix A) is a `longtable` inside `main.tex`; it is not an external file.

## Compile on Overleaf

1. Zip this folder (or just `main.tex` + `figures/`) and upload it with
   **New Project → Upload Project**.
2. Set the compiler to **pdfLaTeX** (Menu → Compiler → pdfLaTeX).
3. Click **Recompile**. No bibliography run is needed: there is no `.bib`
   file and no `\cite`.
4. The document is designed for A4 paper with 1-inch margins and must stay
   within 10 pages excluding the appendix, as required by the lab guidelines.

Local check with a full TeX Live installation:

```sh
pdflatex main.tex
pdflatex main.tex     # second pass to resolve cross-references
```

## Packages

Only packages from a standard TeX Live installation are used:
`extarticle`, `newtxtext`/`newtxmath`, `geometry`, `graphicx`, `booktabs`,
`longtable`, `array`, `amsmath`, `microtype`, `enumitem`, `caption`,
`titlesec`, `hyperref`. All of them are available on Overleaf by default.

## Conventions

- Font size 9 pt (`extarticle`), single column, 1-inch margins.
- Every question from the lab spec is typeset with the `\qa{}` macro, in
  italics, immediately before its answer.
- Runs are cited as `R1`–`R24` (macro `\run{}`), the same identifiers used in
  `Lab1.ipynb` and in `labs/lab01/logbook.md`.

## Placeholders to fill before submitting

The title block already has the four names (alphabetical by surname: Amendolara,
Bruno, Mercurelli, Tocci). Still to fill in:

- `Group [ID]`
- `s[matricola]` (four times), next to each name
