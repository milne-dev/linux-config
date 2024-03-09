# linux-config

Personal config that should not be forgotten.

<img src="linux-penguin.jpg">

## git

### `git diff` tab size

This will set the tab size to 2 spaces (your current preference). Works with `gnome-terminal`.

```bash
git config --global core.pager 'less -x1,3'
```

## bash

### `~/Projects` alias

```bash
alias p='cd ~/Projects'
```

### git aliases

```bash
alias gd='git diff'
alias gs='git status'
alias gp='git push'
alias grs='git reset --hard HEAD'

function gc() {
  git commit -am "$*"
}
```
