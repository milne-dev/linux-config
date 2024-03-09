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

### Other useful aliases

```bash
alias ll='ls -la'
```

### Colours & git branch in command prompt

```bash
function parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}

export PS1="\u@\h \[\e[32m\]\w \[\e[91m\]\$(parse_git_branch)\[\e[00m\]$ "
```

## Drivers

### Nvidia

The current driver that is not currently broken is `535.129.03` as of March 9, 2024.
