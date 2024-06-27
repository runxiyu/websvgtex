# websvgtex

`websvgtex` is a simple script that converts standalone LaTeX components (such as formulae) into SVG.

## How it works
1. Wrap the input in a standard template that uses the "standalone" document class with the "preview" option and includes some math-related packages
2. Calls `latex m.dvi` to produce a DVI file
3. Calls `dvips m.ps` to produce a PS file
4. Calls `inkscape m.ps --export-plain-svg --export-filename=m.svg` to produce an SVG file
