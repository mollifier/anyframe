# anyframe

## Synopsis

## How to set up

First of all, you need to install [peco](https://github.com/peco/peco), [percol](https://github.com/mooz/percol), or [fzf](https://github.com/junegunn/fzf)

### Manually install

Put all files somewhere in your $fpath, and add the following lines to your .zshrc:

```
autoload -Uz anyframe-init
anyframe-init
```

#### For example

```
# download all files
% cd /path/to/dir
% git clone https://github.com/mollifier/anyframe
```

And add the following lines to your .zshrc:

```
fpath=(/path/to/dir/anyframe(N-/) $fpath)

autoload -Uz anyframe-init
anyframe-init
```

### Installing using Antigen
If you use [Antigen](https://github.com/zsh-users/antigen), add the following line to your .zshrc:

```
antigen bundle mollifier/anyframe
```

### keybind
You can map anyframe widgets to whatever key you like.

For example, add the following lines to your .zshrc:

```
bindkey '^xb' anyframe-widget-cdr
bindkey '^x^b' anyframe-widget-checkout-git-branch

bindkey '^xr' anyframe-widget-execute-history
bindkey '^x^r' anyframe-widget-execute-history

bindkey '^xi' anyframe-widget-put-history
bindkey '^x^i' anyframe-widget-put-history

bindkey '^xg' anyframe-widget-cd-ghq-repository
bindkey '^x^g' anyframe-widget-cd-ghq-repository

bindkey '^xk' anyframe-widget-kill
bindkey '^x^k' anyframe-widget-kill

bindkey '^xe' anyframe-widget-insert-git-branch
bindkey '^x^e' anyframe-widget-insert-git-branch
```

## Requirement

Some widgets requires external commands.

### anyframe-widget-cdr
require cdr

To use cdr, add the following line to your .zshrc:

```
autoload -Uz chpwd_recent_dirs cdr add-zsh-hook
add-zsh-hook chpwd chpwd_recent_dirs
```

for more information, see REMEMBERING RECENT DIRECTORIES section in man zshcontrib(1)

### anyframe-widget-cd-ghq-repository
require [ghq](https://github.com/motemen/ghq)


## Usage

## Configurations

```
# expressly specify to use peco
zstyle ":anyframe:selector:" use peco
# expressly specify to use percol
zstyle ":anyframe:selector:" use percol
# expressly specify to use fzf
zstyle ":anyframe:selector:" use fzf

# specify path and options for peco, percol, or fzf
zstyle ":anyframe:selector:peco:" command 'peco --no-ignore-case'
zstyle ":anyframe:selector:percol:" command 'percol --case-sensitive'
zstyle ":anyframe:selector:fzf:" command 'fzf --extended'
```

## Examples


