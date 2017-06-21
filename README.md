# itex
(Semi)Automatic package installing for \*TeX

## Requirements
- `expect`
- `bash`

## Usage
### `tlmgri`
Usage: `tlmgr [TLMGROPTS] FILENAME`

This will search for a package containing exactly `FILENAME`. If there is only
one it will be installed. If there are multiple a select is given. `TLMGROPTS`
are applied on the `tlmgr install` command. Thus, you can do something like:
`tlmgri --dry-run booktabs.sty`.

### `itex`
Usage: `itex *tex [TEXOPTS]`

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
