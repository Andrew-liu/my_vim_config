##我的vimrc
    
```vim
set number
set helplang=cn
set ai      
set bs=2
set showmatch
set autoread
set autoindent

syntax on
set smartindent

"tab
set tabstop=4
set expandtab
set shiftwidth=4

" line
set cursorline

set hls

set nocompatible              " be iMproved, required
filetype off                  " required
set encoding=utf-8
set fillchars+=stl:\ ,stlnc:\

set rtp+=~/.vim/bundle/vundle/
call vundle#rc()

Bundle 'gmarik/vundle'
Bundle 'tpope/vim-rails.git'
Bundle 'git@github.com:scrooloose/nerdtree.git'
Bundle 'git@github.com:Raimondi/delimitMate.git'
Bundle 'hallison/vim-markdown'
Bundle 'git@github.com:kien/ctrlp.vim.git'
Bundle 'msanders/snipmate.vim'

" Powerline
let g:Powerline_symbols = 'fancy'

filetype plugin indent on     " required

" NEADTree
autocmd vimenter * if !argc() | NERDTree | endif
map <C-n> :NERDTreeToggle<CR>
autocmd bufenter * if (winnr("$") == 1 && exists("b:NERDTreeType") && b:NERDTreeType == "primary") | q | endif

" CtrlP
let g:ctrlp_map = '<c-p>'
let g:ctrlp_cmd = 'CtrlP'
set wildignore+=*/tmp/*,*.so,*.swp,*.zip     " MacOSX/Linux
let g:ctrlp_custom_ignore = '\v[\/]\.(git|hg|svn)$'

```

##使用方式

```shell
git clone https://github.com/guochy2012/vim.git ~/.vim

cp ~/.vim/vimrc ~/.vimrc
```
