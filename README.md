1.VIM 配置
首先在~/.bashrc 中加入stty -ixon  便于之后Ctrl+S保存等操作
add "stty -ixon" in ~/.bashrc first


1.1 ==========================.vimrc 配置：

set nu
set mouse=a

"========================================自定义快捷键(~/.bashrc需添加stty -ixon)==============
"在可视化模式下 Ctrl+C拷贝至剪切板"
vmap <c-c> "+y

inoremap ( ()<ESC>i
		inoremap { {}<ESC>i
		inoremap ' ''<ESC>i
		inoremap " ""<ESC>i

		""插入模式,Ctrl+J 跳下一格""
		inoremap <C-j> <Esc>o
		"往右移动"
		inoremap <C-l> <Right>
		""Ctrl+i 替代ESC"
		map <C-S> :w!<CR>i
		inoremap <C-S> <Esc>:w!<CR>i
		"保存并退出"
		map <C-Q> :wq<CR>
		inoremap <C-Q> <Esc>:wq<CR>
		"退出不保存
		map <C-X> <Esc>:q<CR>
		inoremap <C-X> <Esc>:q<CR>
		map <C-Z> <Esc>u<CR>i
		"撤销 redo"
		inoremap <C-Z> <Esc>u<CR>i
		inoremap <C-R> <Esc><C-R><CR>i

		inoremap <C-Space> <Esc>



		"""""""""""""""""""""""""""""            和自动补全一起用
		"enable this plugin for filetypes, '*' for all files.
		let g:apc_enable_ft = {'*':2,'''py':1,'python':1, 'text':1, 'markdown':1,'php':1}
		" source for dictionary, current or other loaded buffers, see ':help cpt'
			set cpt=.,k,w,b
			""don't select the first item.
			set completeopt=menu,menuone,noselect
			" suppress annoy messages.
			set shortmess+=c
			""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
			"=======================显示空格和tab"
			set list
			set listchars=tab:-->,space:·
			""=========================一般设置======================================= 
			set nocompatible          "vim比vi支持更多的功能，如showcmd，避免冲突和副作用，最好关闭兼容 
			set encoding=utf-8  "使用utf-8编码 
			set number                "显示行号 
			set showcmd               "显示输入命令 
			set cursorline            "显示当前行 
			set hlsearch              "显示高亮搜索 
			set incsearch 
			set history=100           "默认指令记录是20 
			set ruler                 "显示行号和列号（默认打开) 
			set pastetoggle=<F3>      "F3快捷键于paste模式与否之间转化，防止自动缩进 
			set helplang=cn           "设置为中文帮助文档,需下载并配置之后才生效 
			"===========================文本格式排版================================ 
			set tabstop=4
			set softtabstop=4
			set shiftwidth=4
			set cindent
			set smartindent            "改进版的cindent,自动识别以#开头的注释，不进行换行 
			set autoindent              "autoindent配合下面一条命令根据不同语言类型进行不同的缩进操
			"=====================主题插件
			filetype plugin indent on 
			set nowrap
			let g:rehash256 = 1 
			let g:molokai_original = 1 
			highlight NonText guibg=#060606 
			highlight Folded  guibg=#0A0A0A guifg=#9090D0 
			set t_Co=256 
			set background=dark 
			colorscheme  molokai 




			1.3 =================================插件安装


			1. Tmux 配置
			▪▪▪▪▪▪▪














			"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""'""''"''''''''''''''}''"""""""""""""""""""""""""""""""""""""""""""""""'''}}))""")"""
