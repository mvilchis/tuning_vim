# tuning_vim

Commands to create a development environment.

**Install pathogen**
```
mkdir -p ~/.vim/autoload ~/.vim/bundle && \
curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim && \
echo "execute pathogen#infect()" >> ~/.vimrc
```

**Install slime**

```
mkdir ~/.vim/bundle && \
git clone git://github.com/jpalardy/vim-slime.git ~/.vim/bundle/vim-slime
```

**Install nerdtree**
```
git clone https://github.com/scrooloose/nerdtree.git ~/.vim/bundle/nerdtree
echo "autocmd vimenter * NERDTree ">> ~/.vimrc
echo "autocmd StdinReadPre * let s:std_in=1">> ~/.vimrc
echo "autocmd VimEnter * if argc() == 0 && !exists("s:std_in") | NERDTree | endif" >> ~/.vimrc
echo "map <C-n> :NERDTreeToggle<CR>" >> ~/.vimrc
echo "autocmd bufenter * if (winnr("$") == 1 && exists("b:NERDTree") && b:NERDTree.isTabTree()) | q | endif" >> ~/.vimrc
```
**Install templates**
```
git clone git://github.com/aperezdc/vim-template.git ~/.vim/bundle/vim-template
```
