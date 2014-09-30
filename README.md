��װ ��
1. ��Linux�����ã���vim-configureĿ¼������~/Ŀ¼�£����ҽ��ļ����޸ĳ�.vim ��
2. ��.vimrc�ļ�������~/Ŀ¼�¡�

������־��
1. NERDTree install

commit : Ŀ¼��

url : https://github.com/scrooloose/nerdtree.git

cmd : 
	mkdir bundle
	cd ~/.vim/bundle
	git clone https://github.com/scrooloose/nerdtree.git

install : 
	cp * ../../

config -- .vimrc

map <C-l> :tabn<cr>             " ��һ��tab
map <C-h> :tabp<cr>             " ��һ��tab
map <C-n> :tabnew<cr>           " ��tab
map <C-k> :bn<cr>               " ��һ���ļ�
map <C-j> :bp<cr>               " ��һ���ļ�

2. NERDTree-Tabs install

commit : Ŀ¼��

url : https://github.com/jistr/vim-nerdtree-tabs.git

cmd : 
	mkdir bundle
	cd ~/.vim/bundle
	git clone https://github.com/jistr/vim-nerdtree-tabs.git

install : 
	cp * ../../

config -- .vimrc

let g:nerdtree_tabs_open_on_console_startup=1       	" ���ô�vim��ʱ��Ĭ�ϴ�Ŀ¼��
map <F3> :NERDTreeTabsToggle <CR>         		" ���ô�Ŀ¼���Ŀ�ݼ�
imap <F3> :NERDTreeTabsToggle <CR>         		" ���ùر�Ŀ¼���Ŀ�ݼ�

3. vimcdoc install

commit : ���İ����ĵ�

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

commit : ����/��������

url : *

cmd : 
	ctags -R *

install : 
	sudo apt-get install ctags

config -- .vimrc

set tags=tags  		" ����tags  
set autochdir 

5. ctags install

url : *

cmd : 
	ctags -R *

install : 
	sudo apt-get install ctags

config -- .vimrc

set tags=tags  		" ����tags  
set autochdir 

6. taglist install

url : http://www.vim.org/scripts/script.php?script_id=273

cmd : 
	*

install : 
	cp -r * ../../

config -- .vimrc

nnoremap <silent> <F8> :TlistToggle<CR><CR>	" ��F8��ť���ڴ��ڵ�������taglist�Ĵ���, ��vc������workpace
" :Tlist              				" ����TagList
let Tlist_Auto_Open=0 				" Ĭ�ϴ�Taglist 
let Tlist_Ctags_Cmd = '/usr/bin/ctags'  
let Tlist_Show_One_File=1                    	" ֻ��ʾ��ǰ�ļ���tags
let Tlist_Exit_OnlyWindow=1                  	" ���Taglist���������һ���������˳�Vim
let Tlist_Use_Right_Window=1                 	" ���Ҳര������ʾtaglist����
let Tlist_File_Fold_Auto_Close=1             	" �Զ��۵�

7. bufexplorer install

commit : ��� bufexplorer ��һ���������������ɵ��ڸ��� buffer ֮������л���

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

commit : Vim �Դ���ƴд���(Spell Check)

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

commit : pydiction ����ʵ�ִ��벹ȫ���﷨��ʾ����

url : https://github.com/rkulla/pydiction.git 

cmd : 
	*

install : 
	* Linux/Unixϵͳ����python_pydiction.vim�ļ����Ƶ� ~/.vim/after/ftplugin Ŀ¼�¡������Ŀ¼�����ڣ��򴴽�����vim���Զ��ڴ�Ŀ¼��������

����	* Windowsϵͳ����python_pydiction.vim�ļ����Ƶ� C:\vim\vimfiles\ftplugin Ŀ¼�£��������Vim��װ·��ΪC:\vim��

����	* ����֮����������ļ�complete-dict��pydiction.py���Է��õ��κ�������õ�λ�ã�����ftpluginĿ¼�����ֻ���python_pydiction.vim����Ӧ�û��������ļ���
	�����ѹ���pydictionĿ¼

	$ cp after/ftplugin/python_pydiction.vim ~/.vim/after/ftplugin
	$ cp complete-dict ~/.vim
	$ cp pydiction.py ~/.vim

config -- .vimrc


