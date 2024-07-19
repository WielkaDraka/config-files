# VIM

Update your ubuntu version
```bash
sudo apt-get update
sudo apt-get install vim
```

Create directories
```bash
mkdir -p ~/.vim ~/.vim/autoload ~/.vim/backup ~/.vim/colors ~/.vim/plugged
```

Create a.vimrc file in home directory
```bash
touch ~/.vimrc
```

Copy [config file](.vimrc) into your home directory.

## Adding plugs

Install the vim-plug plugin:
```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

adn call plug#begin('~/.vim/plugged') and call plug#end() 
```bash
" PLUGINS ---------------------------------------------------------------- {{{

call plug#begin('~/.vim/plugged')




call plug#end()

" }}}
```

Now add your plugs
```bash
" PLUGINS ---------------------------------------------------------------- {{{

call plug#begin('~/.vim/plugged')


  Plug 'dense-analysis/ale'

  Plug 'preservim/nerdtree'


call plug#end()

" }}}
```

Adding color scheme
```bash
cd ~/.vim/colors

curl -o molokai.vim https://raw.githubusercontent.com/tomasr/molokai/master/colors/molokai.vim
```
Save file using **:w**
In vim use commands:
```bash
:source ~/.vimrc

:PlugInstall
```
## Solving problem with curl

```bash
sudo snap remove curl
sudo apt install curl
```
