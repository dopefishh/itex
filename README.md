# itex
(Semi)Automatic package installing for \*TeX

## Requirements
- `expect` (http://expect.sourceforge.net/)
- `bash` (https://www.gnu.org/software/bash/)
- `texlive` (https://tug.org/texlive/)

You can install this on a debian-like system with the following command:

    # apt-get install expect bash

For texlive, you need at least the infrastructure (`tlmgr`). No packages are
required.

## Usage
### `tlmgri`
Usage: `tlmgri [TLMGROPTS] FILENAME`

This will search for a package containing exactly `FILENAME`. If there is only
one it will be installed. If there are multiple a select is given. `TLMGROPTS`
are applied on the `tlmgr install` command. Thus, you can do something like:
`tlmgri --dry-run booktabs.sty`.

### `itex`
Usage: 

    itex [ITEXOPTS] TEXCOMMAND [TEXOPTS]

e.g.:

    itex -b -l pkgs.log pdflatex -no-shell-escape document.tex

Prepend your \*TeX command with `itex`. When the command starts to complain
about missing packages it automatically launches `tlmgri` to install the
package.

## Installation
Just move or link both `itex` and `tlmgri` somewhere in your `$PATH` (e.g.
/usr/local/bin)

## Author
Mart Lubbers

## License
See `LICENCE`
