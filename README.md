# A more orange variant of the srcery theme.

Originally a fork of [srcery-vim](https://github.com/srcery-colors/srcery-vim), I have done very little. All cred to my predecessors!


## Installation

### Manually
Put `srcery.vim` in `~/.vim/colors/` (on unix-like systems) or `%userprofile%\vimfiles\colors\` (on Windows).

### Vim 8

Vim 8 has native support for loading plugins. All you need to do to is to clone
this repository into `~/.vim/plug/default/opt`.

    git clone https://github.com/korsbo/srcery-vim ~/.vim/plug/default/opt

The same works for NeoVim, but you have to clone it into a path where NeoVim can
find it.

    git clone https://github.com/korsbo/srcery-vim ~/.config/nvim/plug/default/opt

### [dein.vim](https://github.com/Shougo/dein.vim)
```vim
call dein#add('korsbo/srcery-vim')
```

### [vim-pathogen](https://github.com/tpope/vim-pathogen)
```shell
cd ~/.vim/bundle
git clone https://github.com/korsbo/srcery-vim
```

### [vim-plug](https://github.com/junegunn/vim-plug)
```vim
Plug 'korsbo/srcery-vim'
```

## Configuration

Srcery includes a few toggles due to discrepancies in the various setups possible.
To change any of these you'd put something like this in your `.vimrc`

```viml
let g:srcery_italic = 1
```

Make sure that you set these variables before assigning `colorscheme`.

#### g:srcery_bold

Enables bold text.
default: 1

#### g:srcery_italic

Enables italic text.
default: gui 1, term 0

#### g:srcery_transparent_background

Removes the background color in terminal.
This is a bit of an experimental option, and it cause issues in certain terminals.
default: 0

#### g:srcery_underline

Enables underlined text.
default: 1

#### g:srcery_undercurl

Enables undercurled text.
default: 1

#### g:srcery_inverse

Enables inverse colors.
default: 1

#### g:srcery_inverse_matches

Enables inverse search matches.
default: 0

#### g:srcery_inverse_match_paren

When enabled will inverse matching delimiters.

Works best with [Rainbow parenthesis](https://github.com/kien/rainbow_parentheses.vim)

default: 0

#### g:srcery_dim_lisp_paren

Dims lisp dialects delimiters to a fairly dark gray (xgray5 specifically)

default: 0

## Usage
```
:color srcery
```

If you like what you see and decide to make srcery your default colorscheme, add the relevant line to your vimrc:
```vim
colorscheme srcery
```
## Screenshots
viml, bash
![viml_bash](assets/viml_bash.png)

clojure, elisp
![lisp](assets/lisp.png)

c, rust
![c_rust](assets/c_rust.png)

python, js
![py_js](assets/py_js.png)

git, terminal
![py_js](assets/git_term.png)


Typeface used in screenshots is [Iosevka](https://github.com/be5invis/Iosevka)

## Plugin support

### Lightline
![lightline](assets/lightline.png)

[Lightline](https://github.com/itchyny/lightline.vim) colorscheme.
To use it, include 'srcery' value in lightline configuration, like so:

```vim
let g:lightline = {
      \ 'colorscheme': 'srcery',
      \ }
```

### Airline
![airline](assets/airline.png)

Thanks to [MindTooth](https://github.com/MindTooth), Srcery now includes an [Airline](https://github.com/vim-airline/vim-airline) theme.

### Other

These don't require any additional configuration.

* [ale](https://github.com/w0rp/ale)
* [ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim)
* [vim-gitgutter](https://github.com/airblade/vim-gitgutter)
* [vim-indent-guides](https://github.com/nathanaelkane/vim-indent-guides)
* [vim-sneak](https://github.com/justinmk/vim-sneak)

Plugin support is still a work in progress and more will come, if there is
anything missing that you'd like to add please open an issue and let me know.

## Xterm colors
Srcery uses some [xterm 256
colors](https://en.wikipedia.org/wiki/Xterm#/media/File:Xterm_256color_chart.svg)
to pad out the color selection:

   TERMCOL   |  NR  |   HEX   |    RGB
------------ | ---- |  -------| ----------
orange       | 202  | #FF5F00 | 255, 95, 0
brightorange | 208  | #FF8700 | 255, 135, 0
hard_black   | 233  | #121212 | 18, 18, 18
xgrey1       | 235  | #262626 | 38, 38, 38
xgrey2       | 236  | #303030 | 48, 48, 48
xgrey3       | 237  | #3A3A3A | 58, 58, 58
xgrey4       | 238  | #444444 | 68, 68, 68
xgrey5       | 239  | #4E4E4E | 78, 78, 78

 
## Troubleshooting

### Colors don't look right

Ensure that 256 colors are enabled in vim by setting this option **before** setting the colorscheme.
```viml
set t_Co=256
```

### 24-bit color, tmux and Neovim

If you want to use GUI colors in terminal make sure that tmux pass
through 24-bit color codes. For example, if you use
[Termite](https://github.com/thestinger/termite) add it to the
terminal overrides setting:

```tmux
set -ga terminal-overrides ",xterm-termite:Tc"
```

For other terminals, replace `xterm-termite` with the relevant
terminal type. (stored in `$TERM`).

See [Arch wiki](https://wiki.archlinux.org/index.php/Tmux#24-bit_color)
and this [issue](https://github.com/korsbo/srcery-vim/issues/36).

## Contributors

 * [roosta](https://github.com/roosta)
 * [MindTooth](https://github.com/MindTooth)
 * [schtibe](https://github.com/schtibe)
 * [jswinarton](https://github.com/jswinarton)
 * [xfbs](https://github.com/xfbs)

## Extra

### Emacs

 Check out [srcery-emacs](https://github.com/korsbo/srcery-emacs)
