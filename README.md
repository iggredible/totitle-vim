# Totitle.vim

Totitle.vim is a plugin that adds an operator to titlecase your text.

*This project was inspired by Chris Toomley's [vim-titlecase](https://github.com/christoomey/vim-titlecase) plugin, with some added improvements.*

# Usage

Vim comes with three case operators: uppercase (`gU`), lowercase (`gu`), and toggle-case (`g~`). Totitle introduces the `gt` operator. Being an operator, it accepts motions (including text objects). It can also be repeated with the dot command (`.`).

```
[s]now white and the seven dwarves
```

Suppose that your cursor is on the letter s as shown above:
- To titlecase the innerword, run `gtiw`. It will titlecase it to "Snow".
- To titlecase the next two words, run `gt2w`. It will titlecase them to "Snow White".
- To titlecase the current line, run `gtt`. It will titlecase it to "Snow White and the Seven Dwarves".

# Key Bindings

The default key binding is `gt`. It overwrites Vim's `:tabn` command. If you want to map it to a different key binding, like `gz`, add this in your vimrc:

```
let g:totitle_default_keys = 0

nnoremap <expr> gz ToTitle()
xnoremap <expr> gz ToTitle()
nnoremap <expr> gzz ToTitle() .. '_'
```

# Installation

For example, if you use [vim-plug](https://github.com/junegunn/vim-plug):

```
call plug#begin('~/.vim/plugged')
  Plug 'iggredible/totitle-vim'
call plug#end()
```

Restart Vim / source your vimrc, then run `:PlugInstall`.

It should work with other plugin managers too.

If you use packages (`:h packages`):

```
git clone https://github.com/iggredible/totitle-vim.git ~/.vim/pack/vendor/start/totitle-vim
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/totitle-vim/doc/" -c q
```

# License

Same as Vim license (`:h license`).
