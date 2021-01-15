# openscad.nvim

Simple openscad cheatsheet/help written in lean Lua

OpenSCAD help system and syntax highlighting in Neovim.
This plugin was first created as a companion to [the original openscad syntax highlighting](https://github.com/sirtaj/vim-openscad).
But it now contains a modified and updated version. In addition a `openscad-help` filetype and syntax is implemented.

In the future maybe lsp, error checking, hints and completion will exist here. 

Note that some features of this plugin is `*NIX` only

## Requirements

Nvim >= 0.5 (nightly)

## Dependencies

Run `:checkhealth` to see if you fulfill the dependencies and requirements.

    - [zathura](https://github.com/pwmt/zathura)
    - [skim](https://github/lotabout/skim.vim) or [fzf](https://github.com/junegunn/fzf.vim)
    - [htop](https://htop.dev)

## Install

* To install using packer.nvim
    1. Add this to your plugins.lua:
    ```lua
    use {
        'salkinmada/openscad.nvim',
            config = function ()
                require('openscad')
                end
    }
    ```
    2. run `:PackerInstall` or `:PackerSync` and compile lazy-loaders

* To install using vim-plug
    1. Add this to your init.vim / .vimrc:
    `Plug 'salkinmada/openscad.nvim'`
    2. do a `:PlugInstall`
    3. add `lua require('openscad')` to your `init.vim`
    ```vimscript
    lua require('openscad.nvim')
    ```

## Available mappings

`<Enter>`/`<C-m>` in normal mode
Toggle cheatsheet window
![cheatsheet](https://oddodd.org/lib/openscad.nvim/cheatsheet.gif)

`<A-h>` in normal mode
Fuzzy find help resource
![help](https://oddodd.org/lib/openscad.nvim/help.gif)

`<A-m>` in normal mode
Open offline openscad manual in pdf via `zathura`
![manual](https://oddodd.org/lib/openscad.nvim/manual.gif)

`<A-o>` in normal mode
Open file in OpenSCAD
![execute](https://oddodd.org/lib/openscad.nvim/execute.gif)

`<A-c>` in normal mode
toggle `htop` filtered for openscad processes
![execute](https://oddodd.org/lib/openscad.nvim/htop.gif)

## Options

Options may be defined in either lua or vimscript.
```lua
vim.g.openscad_cheatsheet_toggle_key = '<Enter>'
vim.g.openscad_cheatsheet_window_blend = 15
vim.g.openscad_help_trig_key = '<A-h>'
vim.g.openscad_help_manual_trig_key = '<A-m>'
vim.g.openscad_exec_openscad_trig_key = '<A-o>'
-- should the openscad project automatically be opened on startup
vim.g.openscad_open_on = '!' -- comment out line to disable
```
```vimscript
let g:openscad_cheatsheet_toggle_key = '<Enter>'
let g:openscad_cheatsheet_window_blend = 15
let g:openscad_help_trig_key = '<A-h>'
let g:openscad_help_manual_trig_key = '<A-m>'
let g:openscad_exec_openscad_trig_key = '<A-o>'
" should the openscad project automatically be opened on startup
let g:openscad_open_on = '!' " comment out line to disable
```
