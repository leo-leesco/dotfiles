# Dotfile management

The purpose of this repository is to centralize all configuration files and make them easily replicable on another computer.

## Usage

### Dependencies

You will need [stow](https://www.gnu.org/software/stow/). As I use a Mac, I install it via [Homebrew](https://brew.sh/) :
```shell
brew install stow
```

### Setup

```shell
cd
git clone git@github.com:leo-leesco/dotfiles.git
cd dotfiles
git submodule update --init --recursive
stow .
```

### Daily maintenance

Whenever you update your configuration (more precisely, when there is a chance a new dotfile has been created), you should always move it, including folders, add it to `dotfiles` in order to version it and run `stow .` from the repository `dotfiles`.

## Additional dependencies

All dependencies listed here can be installed using `brew install <program>` :
- `neovim`
- `fish`
- `tmux`

### `clangd`

To integrate `brew` installs of `C` dependencies, run the following script :
```fish
mkdir ~/Library/Preferences/clangd
echo "CompileFlags:
  Add: [-I$(brew --prefix)/include, -L$(brew --prefix)/lib]" > ~/Library/Preferences/clangd/config.yaml
```
