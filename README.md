# Totitle.vim

Totitle.vim is a plugin that adds an operator to title-case your text. 

*This project was inspired by Chris Toomley's [vim-title-case](https://github.com/christoomey/vim-title-case) plugin, with some added improvements.*

# Usage

Vim comes with three case operators: uppercase (`gU`), lowercase (`gu`), and toggle-case (`g~`). Totitle introduces the `gt` operator. Being an operator, it accepts motions (including text objects). It can also be repeated with the dot command (`.`).

```
[s]now white and the seven dwarves
```

Suppose that your cursor is on the letter s as shown above:
- To title-case the innerword, run `gtiw`. It will title-case it to "Snow".
- To title-case the next two words, run `gt2w`. It will title-case them to "Snow White".
- To title-case the current line, run `gtt`. It will title-case it to "Snow White and the Seven Dwarves".

# Key Bindings

The default key binding is `gt`. It overwrites Vim's `:tabn` command. If you want to map it to a different key binding, like `gz`, add this in your vimrc:

```
let g:totitle_default_keys = 0

nnoremap <expr> gz ToTitle()
xnoremap <expr> gz ToTitle()
nnoremap <expr> gzz ToTitle() .. '_'
```


# License

Same as Vim license (from Vim, run `:h license`).

