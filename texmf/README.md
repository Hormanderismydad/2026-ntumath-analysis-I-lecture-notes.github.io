# Extra LaTeX files for the build

`tex/latex/ctex/ctexhook.sty` is an unmodified copy from the `ctex` package (TeX Live 2023, as in Ubuntu 24.04's `texlive-lang-chinese`), distributed under the LaTeX Project Public License 1.3c.
`xeCJK` needs it. Shipping this one 6 KB file lets the GitHub build skip installing the 50 MB `texlive-lang-chinese`.

The workflow sets `TEXMFHOME` to this folder. For a local PDF build, run:

```bash
TEXMFHOME=$PWD/texmf pretext build print
```
