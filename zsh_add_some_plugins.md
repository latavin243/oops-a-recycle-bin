Just after installing `oh-my-zsh`, add `zsh-autosuggestions` and `zsh-syntax-highlighting`:
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
sed -i "s/^plugins=(git)$/plugins=\(git extract zsh-autosuggestions zsh-syntax-highlighting\)/" ~/.zshrc
source ~/.zshrc
```

To remove blank line and comment line:
```bash
sed -i -e "/^$/d" -e "/^#/d" ~/.zshrc
```
