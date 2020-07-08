Always `sudo apt update` first!!!

# VIM

## neovim

Install neovim as a lightweight, extensible alternative to vim.

`sudo apt install neovim`

Useful shortcuts and basic cheat sheet [here](https://yannesposito.com/Scratch/en/blog/Learn-Vim-Progressively/)

## Vim Bootstrap: Basic theme with arsenal of plugins

[Vim Bootstrap](https://vim-bootstrap.com/) generates a sensible `~/.vimrc` (or `~/.config/nvim/init.vim`) as a base. Current init.vim file was built using this (neovim, Python, C) with a few small modifications. No need to use this directly since the repo `init.vim` file can be downloaded, this is just for reference.

## NERDTree

For navigating directories, adds the left pane tree in NeoVim. 

- <kbd>Ctrl</kbd> + <kbd>n</kbd> to toggle tree
- Currently configured to autoload upon oepning nvim with a directory. 
- Git plugin installed, marks git statuses for files when tree is open

## CommandT 

Follow all instructions https://github.com/wincent/command-t!!! Requires more additional steps!!!

1. Install ruby `sudo apt-get install ruby-full`
2. Compile neovim with ruby support `gem install neovim`
3. Compile Command T using the following commands.

```
cd ~/.config/nvim/plugged/command-t/ruby/command-t/ext/command-t
ruby extconf.rb
make
```

5. Usage: `<leader> + t` (<leader> is "," for this config) and then perform fuzzy searching from the current directory! `C - c` to cancel prompt.

# Window manager

## dwm

Yet to try!!!

# Terminal stuff

## Oh my zsh

No explanation required. Install using

1. Main oh my zsh program `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
2. Powerline fonts for agnoster theme `sudo apt-get install fonts-powerline`
3. Set `ZSH_THEME="agnoster"` in `~/.zshrc`.

### Packages

- zsh-suggestions: See [link](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md) under "Oh My Zsh".
- zsh-syntax-highlighting See [link](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)
- advanced tab completion (not a package per se): Add the following to `~/.zshrc`
```
autoload -U compinit
compinit
```

## fzf

Fuzzy finder within the shell. 

- While in the shell hit <kbd>Ctrl</kbd> + <kbd>t</kbd> to open the fuzzy finer and type away to search within current directory (and all children). 
- Select using arrow keys and enter to autocomplete from current cursor position.
- You can also hit <kbd>Tab</kbd> while searching in cd and add more than one item for autocompletion.
- <kbd>Ctrl</kbd> + <kbd>r</kbd> allows fuzzy finding in command history.
- Installation: `sudo apt-get install fzf`. Add the following to your `~/.zshrc` to complete the installation.
```
[ -f ~/.fzf.zsh ] && source ~/.fzf.zsh
export FZF_DEFAULT_OPS="--extended"
```

## Neofetch

Displays system information nicely with a single command `neofetch`. Install using `sudo apt install neofetch`

## tmux 

- Install using `sudo apt install tmux`
- [Theme](https://github.com/gpakosz/.tmux): Allows <kbd>Ctrl</kbd> + <kbd>b</kbd> or <kbd>a</kbd> to enable tmux prompt. Then use vim navigation keys to change panes. 
- tmux session manager [doc](http://tmuxp.git-pull.com/en/latest/quickstart.html) `pip install tmuxp`. Can load and save configurations for fast setup!
