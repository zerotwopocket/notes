## Manage dot files
[referece](https://www.atlassian.com/git/tutorials/dotfiles)

```
    git init --bare $HOME/.cfg
    alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
    config config --local status.showUntrackedFiles no
    echo "alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'" >> $HOME/.bashrc
```

## Migrate dot files
- make sure to add the alias first in .bashrc or .zshrc
```
    alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
```
- ignore folder where it will be cloned (to avoid recursion problems)
```
    echo ".cfg" >> .gitignore
```
- clone to bare repo
```
    git clone --bare <git-repo-url> $HOME/.cfg
```
- define alias
```
    alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
```
- checkout actual content
```
    config checkout
```
