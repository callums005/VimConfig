# VimConfig

```vim
:set number
:set autoindent
:set tabstop=4
:set shiftwidth=4
:set smarttab
:set softtabstop=4
:set mouse=a

call plug#begin()

Plug 'https://github.com/vim-airline/vim-airline'
Plug 'https://github.com/preservim/nerdtree'
Plug 'https://github.com/tpope/vim-surround'
Plug 'https://github.com/tpope/vim-commentary'
Plug 'https://github.com/ap/vim-css-color'
Plug 'https://github.com/drewtempelmeyer/palenight.vim'
Plug 'https://github.com/ryanoasis/vim-devicons'
Plug 'https://github.com/tc50cal/vim-terminal'
Plug 'https://github.com/terryma/vim-multiple-cursors'
Plug 'https://github.com/preservim/tagbar'
Plug 'https://github.com/luochen1990/rainbow'
Plug 'https://github.com/neoclide/coc.nvim'

call plug#end()

:colorscheme palenight

nnoremap <c-z> <nop>

:set nobackup
:set nowritebackup

nnoremap <C-f> :NERDTreeFocus<CR>
nnoremap <C-n> :NERDTree<CR>
nnoremap <C-e> :NERDTreeToggle<CR>
nnoremap <C-t> :TerminalSplit bash<CR>
nnoremap <C-d> :CocList diagnostics<CR>
nnoremap <F7> :CocList outline<CR>
nmap <F8> :TagbarToggle<CR>

:set completeopt -=preview
inoremap <expr> <Tab> pumvisible() ? coc#_select_confirm() : "<Tab>"
```
