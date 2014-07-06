# anyframe

## Synopsis

## How to set up

### Manually install

Put files somewhere in your $fpath and add this line to your .zshrc:

```
autoload -Uz anyframe-init
anyframe-init
bindkey '^Y' anyframe-widget-search-history-put
bindkey '^O' anyframe-widget-search-history-execute
```

### Installing using Antigen
If you use [Antigen](https://github.com/zsh-users/antigen), add the following line to your .zshrc:

```
antigen bundle mollifier/anyframe
```

```
bindkey '^Y' anyframe-widget-search-history-put
bindkey '^O' anyframe-widget-search-history-execute
```



## Usage

## Variables

## Examples


