# Dotfile management

The purpose of this repository is to centralize all configuration files and make them easily replicable on another computer.

## Dependencies

You will need [stow](https://www.gnu.org/software/stow/). As I use a Mac, I install it via [Homebrew](https://brew.sh/) :
```shell
brew install stow
```

## Setup

### Quick setup

#### Clone the current config files

```shell
cd
git clone git@github.com:leo-leesco/dotfiles.git
stow dotfiles/
```

#### Install the tools configured by the corresponding dotfiles

So far, here are the tools I am using :

- [Neovim](https://neovim.io)
    - [Kickstart](https://github.com/nvim-lua/kickstart.nvim)
    - [Vim Tmux navigator](https://github.com/christoomey/vim-tmux-navigator)
- [Tmux](http://tmux.github.io/)
    - [Tmux Package Manager](https://github.com/tmux-plugins/tpm)
    - [Vim Tmux navigator](https://github.com/christoomey/vim-tmux-navigator)
- [zoxide](https://github.com/ajeetdsouza/zoxide)
- [LSDeluxe](https://github.com/lsd-rs/lsd.git)

### Setup from scratch

#### One-liner that moves ALL dotfiles (CAREFUL !)

Be careful with the following command as it will relocate all your files starting with a dot within your home directory !

```shell
cd
mv .* dotfiles
stow dotfiles/
```

#### Manual installation

Simply replace `mv .* dotfiles` by `mv <configFileName> dotfiles`.
