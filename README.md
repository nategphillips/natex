# natex

A collection of commands focused on consistent notation for mathematics, physics, and engineering.

## Aside

Does anyone know what the hell happened to GitHub's $\LaTeX$ rendering inside Markdown files? Seriously, look at what I just typed—it looks terrible. The font is terrible, the spacing is terrible, it's all bad. What I don't understand is that it looked perfectly fine about a year ago, but I can't find any information about them changing something on the backend. From what I've read, they've been using MathJax since the beginning which makes it even more baffling that it's changed so drastically. I've viewed it on multiple browsers as well, so it's certainly not a problem on my end. Not a good look when static site generators have significantly better markup than a company owned by Microsoft. Can't say I'm surprised.

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
> I don't intend for anyone to actually use this package themselves since notation is an extremely subjective topic. Hopefully the information contained here can still prove useful for those wanting to create their own package, however.

### Windows

I use a system-wide installation of MiKTeX on Windows, so that's the installation process I'll elaborate on here.

1. Create a new TEXMF root directory and add an appropriate $\TeX$ directory structure. The directory structure I use is `C:\mytexmf\tex\latex\natex`.
2. Place the `natex.sty` file inside the `natex` directory.
3. Open the MiKTeX admin console, go to the `Directories` tab under `Settings`, and add `C:\mytexmf` as a TEXMF root directory.

You can now import the `natex` package inside your `.tex` files just as you would with any other package.

### Other Systems

For Linux and macOS look [here](https://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-or-cls-files-to-make-them-available-to-all-my-te). See [this page](https://miktex.org/kb/texmf-roots) for more details on MiKTeX specific implementations.
