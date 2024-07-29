# Neovim

## Windows

### [Install Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl/install)

### [Follow Linux with APT installation instructions](#Linux-with-APT)

## Mac (TODO)

## Linux with APT

You can do the installation by copy/pasting the following script and running it in the WSL terminal:

```bash
### Make sure APT is up to date

sudo apt update --fix-missing
sudo apt-get update --fix-missing

### Install Basic Utils

sudo apt install -y git make unzip gcc

### Install Ripgrep

sudo apt install ripgrep

### Install clipboard stuff

sudo apt install xclip xsel

### Install Neovim

sudo apt install neovim

### Install Kickstart

#### Make sure install directory exists and is empty

[ -z ${XDG_CONFIG_HOME} ] && XDG_CONFIG_HOME="$HOME/.config"
rm -rf $XDG_CONFIG_HOME/nvim
mkdir -p $XDG_CONFIG_HOME/nvim

#### Make sure config directory is empty or does not exist

rm -rf $HOME/.local/share/nvim/

#### Clone the Kickstart Repository

git clone https://github.com/dam9000/kickstart-modular.nvim $XDG_CONFIG_HOME/nvim
```

### Run Neovim

```bash
nvim
```

The first time you run Kickstart, and whenever you modify your configuration, you will see the modifications take place. After that, you can do a tutorial by typing `:Tutor`. Alternatively, you can quit with `:q`, or force-quit with `:q!`

