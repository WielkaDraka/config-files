# config-files
This repository contains: Vim, zsh and tmux configurations

#install Guake
sudo apt install guake

## vim

Vim file is in folder vim

## zsh

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

## tmux

install tmux
```bash
sudo apt install tmux
```
run tmux
```bash
tmux new
```
install tpm to handle tmux plugins
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```
Edit ~/.tmux.conf and put this at the bottom
```bash
# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'git@github.com:user/plugin'
# set -g @plugin 'git@bitbucket.com:user/plugin'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
```

Reload tmux environment

```bash
# type this in terminal if tmux is already running
tmux source ~/.tmux.conf
```

Press <prefix> + I (capital i) to install it. The default <prefix> is ctrl + b, so press ctrl + b + I.
