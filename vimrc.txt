
" 语法高亮度显示
syntax on

"搜索匹配高亮
set hlsearch

set cuc
set cul
" 设置行号
set nu

"防止中文注释乱码
set fileencoding=utf-8
set fenc=utf-8
set fencs=utf-8,usc-bom,euc-jp,gb18030,gbk,gb2312,cp936,big－5                    
set enc=utf-8
let &termencoding=&encoding

"设置字体
set guifont=Monospace\ 13

" 设置tab4个空格
set tabstop=4
set expandtab

"程序自动缩进时候空格数
set shiftwidth=4

"退格键一次删除4个空格
set softtabstop=4
autocmd FileType make set noexpandtab

" 在编辑过程中，在右下角显示光标位置的状态行
set ruler

" 搜索忽略大小写 
set ignorecase 

" vim使用自动对起，也就是把当前行的对起格式应用到下一行
set autoindent

" 依据上面的对起格式，智能的选择对起方式，对于类似C语言编写上很有用
set smartindent

" 在状态列显示目前所执行的指令
set showcmd

" 设置颜色主题
colorscheme desert

set nocompatible
set backspace=indent,eol,start


" Module top note information
:map <F5> 1GO<ESC>ggi// *********************************************************************************<cr><ESC>0d$i// Project Name : ahb_sramc_sv<cr><ESC>0d$i// Author       : YC<cr><ESC>0d$i// Website      : no<cr><ESC>0d$i// Create Time  : <C-R>=strftime("%F")<CR><cr><ESC>0d$i// File Name    : .sv<cr><ESC>0d$i// Module Name  :<cr><ESC>0d$i// Called By    :<cr><ESC>0d$i// Abstract     :<cr><ESC>0d$i//<cr><ESC>0d$i// <cr><ESC>0d$i// *********************************************************************************<cr><ESC>0d$i// Modification History:<cr><ESC>0d$i// Date         By              Version                 Change Description<cr><ESC>0d$i// -----------------------------------------------------------------------<cr><ESC>0d$i// <C-R>=strftime("%F")<CR>    Macro           1.0                     Original<cr><ESC>0d$i//  <cr><ESC>0d$i// *********************************************************************************<cr><ESC>0d$i

"NERDTree 配置插件以及安装
set nocompatible
filetype off
map <C-n> :NERDTreeToggle<CR>
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
Plugin 'https://github.com/scrooloose/nerdtree.git'
call vundle#end()
filetype plugin indent on

"自动打开nerdtree,取消下面注释则开启
autocmd vimenter * NERDTree
"更改默认箭头图标
let g:NERDTreeDirArrowExpandable = '▸'
let g:NERDTreeDirArrowCollapsible = '▾'

"Ctrl + c关闭树形目录
map <C-c> :NERDTreeMirror<CR>

"Ctrl + c打开树形目录
map <C-c> :NERDTreeToggle<CR>

"下一个文件 Ctrl+k
map <C-k> :bn<cr>

"上一个文件 Ctrl+j
map <C-j> :bp<cr>

"让Tree把自己给装饰的多姿多彩漂亮点
let NERDChristmasTree=1