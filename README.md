安装 ：
1. 在Linux中配置，将vim-configure目录拷贝到~/目录下，并且将文件名修改成.vim 。
2. 将.vimrc文件拷贝到~/目录下。

配置日志：
1. NERDTree install

commit : 目录树

url : https://github.com/scrooloose/nerdtree.git

cmd : 
	mkdir bundle
	cd ~/.vim/bundle
	git clone https://github.com/scrooloose/nerdtree.git

install : 
	cp * ../../

config -- .vimrc

map <C-l> :tabn<cr>             " 下一个tab
map <C-h> :tabp<cr>             " 上一个tab
map <C-n> :tabnew<cr>           " 新tab
map <C-k> :bn<cr>               " 下一个文件
map <C-j> :bp<cr>               " 上一个文件

2. NERDTree-Tabs install

commit : 目录树

url : https://github.com/jistr/vim-nerdtree-tabs.git

cmd : 
	mkdir bundle
	cd ~/.vim/bundle
	git clone https://github.com/jistr/vim-nerdtree-tabs.git

install : 
	cp * ../../

config -- .vimrc

let g:nerdtree_tabs_open_on_console_startup=1       	" 设置打开vim的时候默认打开目录树
map <F3> :NERDTreeTabsToggle <CR>         		" 设置打开目录树的快捷键
imap <F3> :NERDTreeTabsToggle <CR>         		" 设置关闭目录树的快捷键

3. vimcdoc install

commit : 中文帮助文档

url : http://sourceforge.net/projects/vimcdoc/files/vimcdoc/1.8.0/vimcdoc-1.8.0.tar.gz

cmd : 
	mkdir bundle
	cd ~/.vim/bundle
	wget http://sourceforge.net/projects/vimcdoc/files/vimcdoc/1.8.0/vimcdoc-1.8.0.tar.gz

install : 
	./vimcdoc.sh -i

config -- .vimrc

set helplang=cn			" setting zh_cn
set helplang=en			" setting en_us
set encoding=utf-8

4. ctags install

commit : 方法/函数索引

url : *

cmd : 
	ctags -R *

install : 
	sudo apt-get install ctags

config -- .vimrc

set tags=tags  		" 设置tags  
set autochdir 

5. ctags install

url : *

cmd : 
	ctags -R *

install : 
	sudo apt-get install ctags

config -- .vimrc

set tags=tags  		" 设置tags  
set autochdir 

6. taglist install

url : http://www.vim.org/scripts/script.php?script_id=273

cmd : 
	*

install : 
	cp -r * ../../

config -- .vimrc

nnoremap <silent> <F8> :TlistToggle<CR><CR>	" 按F8按钮，在窗口的左侧出现taglist的窗口, 像vc的左侧的workpace
" :Tlist              				" 调用TagList
let Tlist_Auto_Open=0 				" 默认打开Taglist 
let Tlist_Ctags_Cmd = '/usr/bin/ctags'  
let Tlist_Show_One_File=1                    	" 只显示当前文件的tags
let Tlist_Exit_OnlyWindow=1                  	" 如果Taglist窗口是最后一个窗口则退出Vim
let Tlist_Use_Right_Window=1                 	" 在右侧窗口中显示taglist窗口
let Tlist_File_Fold_Auto_Close=1             	" 自动折叠

7. bufexplorer install

commit : 插件 bufexplorer 是一款可以让你更加轻松的在各个 buffer 之间进行切换。

url : http://www.vim.org/scripts/script.php?script_id=42

cmd : 
	*

install : 
	cp -r * ../../

config -- .vimrc

map <F6> :BufExplorer<CR>

8. Minibuffer install

commit : 

url : http://www.vim.org/scripts/script.php?script_id=159

cmd : 
	*

install : 
	cp -r * ../../

config -- .vimrc

let g:miniBufExplModSelTarget = 1
let g:miniBufExplorerMoreThanOne = 2
let g:miniBufExplUseSingleClick = 1
let g:miniBufExplMapWindowNavVim = 1
let g:miniBufExplVSplit = 25
let g:miniBufExplSplitBelow=1

let g:bufExplorerSortBy = "name"

let g:miniBufExplMapWindowNavArrows = 1
let g:miniBufExplMapCTabSwitchBufs = 1
let g:miniBufExplModSelTarget = 1 

autocmd BufRead,BufNew :call UMiniBufExplorer

map <leader>u :TMiniBufExplorer<cr>

hi MBEChanged guibg=darkblue ctermbg=darkblue 
"" termbg=darkblue

9. Spell Check install

commit : Vim 自带的拼写检查(Spell Check)

url : https://github.com/vim-scripts/SpellCheck

cmd : 
	*

install : 
	

config -- .vimrc

"Pressing ,ss will toggle and untoggle spell checking
map <leader>ss :setlocal spell!<cr>

"Shortcuts using <leader>
map <leader>sn ]s
map <leader>sp [s
map <leader>sa zg
map <leader>s? z=

10. Pydiction install

commit : pydiction 用来实现代码补全和语法提示功能

url : https://github.com/rkulla/pydiction.git 

cmd : 
	*

install : 
	* Linux/Unix系统：将python_pydiction.vim文件复制到 ~/.vim/after/ftplugin 目录下。如果该目录不存在，则创建它，vim会自动在此目录下搜索。

　　	* Windows系统：将python_pydiction.vim文件复制到 C:\vim\vimfiles\ftplugin 目录下（假设你的Vim安装路径为C:\vim）

　　	* 除此之外的另两个文件complete-dict和pydiction.py可以放置到任何你想放置的位置，但在ftplugin目录下最好只存放python_pydiction.vim而不应该还有其他文件。
	进入解压后的pydiction目录

	$ cp after/ftplugin/python_pydiction.vim ~/.vim/after/ftplugin
	$ cp complete-dict ~/.vim
	$ cp pydiction.py ~/.vim

config -- .vimrc


