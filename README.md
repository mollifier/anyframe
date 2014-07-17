# anyframe

## Synopsis

## How to set up

### Manually install

Put all files somewhere in your $fpath, and add the following lines to your .zshrc:

```
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
bindkey '^x^r' anyframe-widget-execute-history
bindkey '^x^i' anyframe-widget-put-history
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

## Variables

## Examples


