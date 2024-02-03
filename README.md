# natex

A custom LaTeX package focused on consistent notation for engineering and physics applications.

## Installation

I use a system-wide installation of MiKTeX, so that's the installation process I'll be demonstrating. Create a new TEXMF root directory and add an appropriate TeX directory structure. The example I use is `C:\mytexmf\tex\latex\natex`. After placing the `.sty` file in the `natex` folder, open the MiKTeX admin console, go to the `Directories` tab under `Settings`, and add `C:\mytexmf` as a TEXMF root directory.

### Other Systems

For Linux, MacOS, etc. look [here](https://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-or-cls-files-to-make-them-available-to-all-my-te). See [this page](https://miktex.org/kb/texmf-roots) for more details on MiKTeX specific implementations.

## deriv

This is a direct fork of [`derivative`](https://github.com/sjelatex/derivative) by sjelatex. I really like the macros and style of this package, but I really *don't* like writing `order=n` each time I want a higher-order derivative. For now, the official package doesn't support implicit ordering, so I implemented a crude fix suggested by sjelatex themselves in [this](https://github.com/sjelatex/derivative/issues/10) issue. Since I don't use the more advanced features of the package, nothing has broken for me yet and this fix is worth the saved keystrokes. Until implicit ordering is added to `derivative`, I'll keep this here.
