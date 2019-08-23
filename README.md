# vim-setup
## .vimrc

````vim
" Pa que se vean los numeros en las lineas
set nu
set tabstop=4
set backspace=indent,eol,start
" Para que se vea mejor el markdown
set linebreak
" para que funcione clipboard
set clipboard=unnamed


set nocompatible              " be iMproved, required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required
Plugin 'VundleVim/Vundle.vim'

" Plugins:
Plugin 'scrooloose/nerdtree'
Plugin 'flazz/vim-colorschemes'
" Plugin 'jistr/vim-nerdtree-tabs'
Plugin 'Lokaltog/powerline', {'rtp': 'powerline/bindings/vim/'}
Plugin 'whatyouhide/vim-gotham'
Plugin 'Yggdroot/indentLine'
Plugin 'vim-python/python-syntax'
" Para el markdown
Plugin 'godlygeek/tabular'
Plugin 'plasticboy/vim-markdown'

" All of your Plugins must be added before the following line
call vundle#end()            " required
filetype plugin indent on    " required
" To ignore plugin indent changes, instead use:
"filetype plugin on
"
" Brief help
" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
"
" see :h vundle for more details or wiki for FAQ
" Put your non-Plugin stuff after this line


:au BufNewFile,BufRead *.py
    \ set tabstop=4 |
    \ set softtabstop=4 |
    \ set shiftwidth=4 |
    \ set textwidth=79 |
    \ set expandtab |
    \ set autoindent |
    \ set fileformat=unix 

syntax on
let g:python_highlight_all = 1
set t_Co=256
colorscheme gotham

" let g:indentLine_color_gui = '#195466'
" let g:indentLine_setColors = 0
let g:indentLine_char = '▏'
````
## .tmux.conf
`````
set -g status-right %H:%M
``````
## .bash_profile
`````
# para quitar username y eso
export PS1="\W \$ "
`````
