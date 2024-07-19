# TMUX

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
Edit ~/.tmux.conf file. Copy file form [here](.tmux.conf)

Reload tmux environment

```bash
# type this in terminal if tmux is already running
tmux source ~/.tmux.conf
```

Press _prefix_ + I (capital i) to install it. The default _prefix_ is ctrl + b, so press ctrl + b + I.
