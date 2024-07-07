# Apple Computer Setup

Steps to set up a new personal Apple machine.

## Install Applications and Tools

```sh
****************************************************************************************************
* Install Applications and Tools
****************************************************************************************************

# Install homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install iTerm2
brew install --cask iterm2

# Install Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# Install git
brew install git

# Install tmux
brew install tmux

# Install 1password
brew install --cask 1password

# Install Google Chrome
brew install --cask google-chrome

# Install Firefox
brew install --cask firefox

# Install Spotify
brew install --cask spotify

# Install Monodraw
brew install --cask monodraw

# Install JetBrains Toolbox
brew install --cask jetbrains-toolbox

# Install AeroSpace
brew install --cask nikitabobko/tap/aerospace
```

## Download Source Code

```sh
****************************************************************************************************
* Download Source Code
****************************************************************************************************

# Make directory for source code
cd ~
mkdir Development
mkdir Development/opensource

# Download Afia
cd ~/Development
mkdir afia-all
cd afia-all
git clone git@github.com:afia/afia.git afia           #  <--- for writing code
git clone git@github.com:afia/afia.git code-review    #  <--- for reviewing other peoples' code
git clone git@github.com:afia/afia.git documentation  #  <--- for writing documentation

# Download Knowledge
cd ~/Development
git clone git@github.com:chinedufn/knowledge.git
```

## Setup Applications

### Aerospace

```sh
cp ~/Development/knowledge/afia/apple-computer-setup/aerospace.toml ~/.aerospace.toml
```
