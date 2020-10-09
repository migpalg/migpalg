call plug#begin('~/.vim/plugged')
  " Plugin section

  Plug 'dracula/vim'
  Plug 'scrooloose/nerdtree'
  Plug 'ryanoasis/vim-devicons'

  Plug 'neoclide/coc.nvim', {'branch': 'release'}
  let g:coc_global_extensions = ['coc-emmet', 'coc-css', 'coc-html', 'coc-json', 'coc-prettier', 'coc-tsserver']

  Plug 'leafgarland/typescript-vim'
  Plug 'peitalin/vim-jsx-typescript'

  Plug 'Shougo/deoplete.nvim', { 'do': ':UpdateRemotePlugins' }
  Plug 'mattn/emmet-vim'
call plug#end()

" Config section

syntax enable
colorscheme dracula
set number tabstop=2 shiftwidth=2 expandtab
set encoding=UTF-8
set nowrap

" Config for file explorer 
let g:NERDTreeShowHidden = 1
let g:NERDTreeMinimalUI = 1
let g:NERDTreeIgnore = []
let g:NERDTreeStatusline = ''
" Automaticaly close nvim if NERDTree is only thing left open
autocmd bufenter * if (winnr("$") == 1 && exists("b:NERDTree") && b:NERDTree.isTabTree()) | q | endif
" Toggle
nnoremap <silent> <C-b> :NERDTreeToggle<CR>

" open new split panes to right and below
set splitright
set splitbelow
" turn terminal to normal mode with escape
tnoremap <Esc> <C-\><C-n>
" start terminal in insert mode
au BufEnter * if &buftype == 'terminal' | :startinsert | endif
" open terminal on ctrl+n
function! OpenTerminal()
  split term://zsh
  resize 10
  set nonumber
endfunction
nnoremap <c-n> :call OpenTerminal()<CR>

" emmet config
let g:user_emmet_leader_key=','

