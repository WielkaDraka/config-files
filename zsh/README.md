# ZSH

check if zsh is installed
```bash
cat /etc/shells
```

install Zsh Shell (for ubuntu)
```bash
sudo apt update
sudo apt install zsh
```

check zsh --version
```bash
zsh --version
```

make zsh your default terminal
```bash
chsh -s $(which zsh)
```

installing Oh My Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

installing plugins
```bash
cd ~/.oh-my-zsh/custom/plugins
git clone https://github.com/zsh-users/zsh-autosuggestions.git
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
```

and edit ~/.zshrc
```bash
plugins=(
    git
    zsh-autosuggestions
    zsh-syntax-highlighting
)
```

restart zsh
```bash
source ~/.zshrc
```

install powerlevel10k
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

then, add powerlevel10k to ~/.zshrc
```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

to add conda:
```bash
# go to conda directory. Change here your username
cd /home/username/miniconda3/bin

# To initialize other shells, use
# conda init <shell>
./conda init zsh
```



