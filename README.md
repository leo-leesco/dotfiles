# Dotfile management

The purpose of this repository is to centralize all configuration files and make them easily replicable on another computer.


## Dependencies

You will need [stow](https://www.gnu.org/software/stow/). As I use a Mac, I install it via [Homebrew](https://brew.sh/) :
```shell
brew install stow
```

## Setup

### Clone the current config files

```shell
cd
git clone git@github.com:leo-leesco/dotfiles.git
stow dotfiles/
```

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
