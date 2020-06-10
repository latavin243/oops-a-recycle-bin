```bash
# fzf
git clone --depth 1 https://github.com/junegunn/fzf.git $HOME/.fzf; $HOME/.fzf/install

# tmux
cd; git clone https://github.com/gpakosz/.tmux.git; ln -s -f .tmux/.tmux.conf; cp .tmux/.tmux.conf.local .
# then vim $HOME/.tmux.conf.local to enable mouse and change prefix, e.g. C-q
# add `map <c-q> <nop>` to $HOME/.vimrc
```
