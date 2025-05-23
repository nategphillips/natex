# natex

A collection of commands focused on consistent notation for mathematics, physics, and engineering.

## General Information

### Motivation

This package exists as my personal replacement for the [`physics`](https://www.ctan.org/pkg/physics) package. You can read about why you might *not* want to use `physics` [in this thread](https://tex.stackexchange.com/questions/471532/alternatives-to-the-physics-package). In general, the commands defined here exist because I've found myself writing them out the long way multiple times. Naturally, I spent far more time creating this package than would be required to just write the commands themselves. Touché.

Throughout, I make extensive use of `DeclarePairedDelimiter` and `DeclarePairedDelimiterX`, both of which belong to [`mathtools`](https://www.ctan.org/pkg/mathtools). These commands are great because they produce fixed-size delimiters by default, but also allow for auto-expanding delimiter pairs using their starred variants.

### Vector Notation

I prefer the clean look of bold vectors, $\boldsymbol{x}$, over the traditional $\LaTeX$ style, $\vec{x}$. Vector notation is aimed at being as explicit as possible, with all vector operators being bolded for clarity.

### Dirac Notation

The [`braket`](https://www.ctan.org/pkg/braket) package is perfectly fine, but there are some small formatting issues that bug me (particularly with how whitespace is handled in front of `\ket`s). I also prefer to define my own shorthand for expectation values, inner products, outer products, and matrix elements.

### Set Notation

I'm not a mathematician, but I have included shorthand for all the common sets of numbers. A convenient set-builder notation is also included since it's quite nice to have around.

### Matrix Notation

The matrix shorthand is primarily useful if you're creating row or column vectors, although it's arguably worse than the default `\begin{pmatrix}...\end{pmatrix}` syntax in terms of formatting larger matrices. I'm still not sure how I feel about including this feature, so it may change in the future.

### Linear Operators

These commands just serve as an easier way to denote linear maps when working with the Dirac formalism in quantum mechanics.

### Trigonometric Functions

Some of the more obscure trig functions that aren't included in base $\LaTeX$ or `mathtools` have been defined here for convenience.

### Other

I've redefined the `\Re` and `\Im` commands since I find the Fraktur symbols $\Re$ and $\Im$ to be ambiguous and visually unappealing. Although there's no universal symbol for defining a variable, I've seen $\coloneqq$ around enough to warrant its use. Finally, there are a pair of upright subscript and upright superscript macros.

## Installation

> [!NOTE]
> I don't intend for anyone to actually use this package themselves since notation is an extremely subjective topic. Hopefully the information contained here can still prove useful for those wanting to create their own package, however. If you do end up using `natex`, thanks!

### Windows

I use a system-wide installation of MiKTeX on Windows, so that's the installation process I'll elaborate on here.

1. Create a new TEXMF root directory and add an appropriate $\TeX$ directory structure. The directory structure I use is `C:\mytexmf\tex\latex\natex`.
2. Place the `natex.sty` file inside the `natex` directory.
3. Open the MiKTeX admin console, go to the `Directories` tab under `Settings`, and add `C:\mytexmf` as a TEXMF root directory.

You can now import the `natex` package inside your `.tex` files just as you would with any other package.

### Other Systems

For Linux and macOS look [here](https://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-or-cls-files-to-make-them-available-to-all-my-te). See [this page](https://miktex.org/kb/texmf-roots) for more details on MiKTeX specific implementations.

## License and Copyright

Copyright 2025 Nathan G. Phillips

This work may be distributed and/or modified under the conditions of the LaTeX Project Public License, either version 1.3 of this license or (at your option) any later version. The latest version of this license is in <https://www.latex-project.org/lppl.txt> and version 1.3c or later is part of all distributions of LaTeX version 2008 or later.

This work has the LPPL maintenance status `maintained`.

The Current Maintainer of this work is Nathan G. Phillips.

The bundle contains the files:

    README.md   This file.
    natex.sty   The package itself.
    natex.pdf   The package documentation in PDF format.
    natex.tex   The master file that produced natex.pdf.
