# Apple Computer Setup

Steps to set up a new personal Apple machine.

## System Settings

#### Trackpad Settigs

- `System Settings > Trackpad > Point & Click`
  - Enable `Tap to click`

- `System Settings > Trackpad > Scroll & Zoom`
  - Disable natural scrolling

#### Dock Settings

`System Settings > Desktop & Dock`

- Enable `Automatically hide and show the Dock`

#### Keyboard Settings

- `System Settings > Keyboard > Keyboard Shortcuts > Modifier Keys`
  - Map `Caps Lock` to `Escape`

#### Control Center

- Enable Show Bluetooth in Menu Bar

#### Notifications

- Disable notifications for:
  - `Messages`
  - `Screen Time`
  - `Tips`
  - `Facetime`

## Setup GitHub

Set the new computer up to have access to GitHub.

```sh
# Press `Enter` to store in the default location.
# Can skip when asked about generating a passphrase.
ssh-keygen -o -t rsa -C "frankie.nwafili@gmail.com"
```

- Log into GitHub on the new machine
- Go to settings
- Go to SSH and GPG keys
- Click `New SSH key`
- In the public key's name include the machine's model and any other information of note
- `cat ~/.ssh/id_rsa.pub`
- Paste the public key into GitHub

## Steup XCode command line developer tools

```
# Needed to use `git`
xcode-select --install
```

## Download Knowledge Repository

```sh
cd ~
mkdir Development
cd Development
git clone git@github.com:chinedufn/knowledge.git
cd knowledge
```

## Setup Vim

```sh
open https://github.com/chinedufn/vim
mkdir -p ~/Development/opensource
cd ~/Development/opensource

# Follow the instructions in the README
```

## .zshrc

```
setopt interactivecomments

# autojump
[ -f /opt/homebrew/etc/profile.d/autojump.sh ] && . /opt/homebrew/etc/profile.d/autojump.sh

# Shell Complations
autoload -U compinit
compinit -i
```

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

# Install autojump
brew install autojump

# Install GitHub CLI
brew install gh
```

## Set up Git

#### Git user configuration
```sh
git config --global user.name "Chinedu Francis Nwafili"
git config --global user.email "frankie.nwafili@gmail.com"
git config --global user.username "chinedufn"
```

#### Aliases

Set up the aliases in the `git.md` documentation.

#### Git GPG key

Follow instructions in `gpg.md` for setting up a GPG key

## Download Source Code

```sh
****************************************************************************************************
* Download Source Code
****************************************************************************************************

# Make directory for source code
cd ~
mkdir -p Development/opensource

# Download Afia
cd ~/Development
mkdir afia-all
cd afia-all
git clone git@github.com:afia/afia.git afia           #  <--- for writing code
git clone git@github.com:afia/afia.git code-review    #  <--- for reviewing other peoples' code
git clone git@github.com:afia/afia.git documentation  #  <--- for writing documentation

```

## Setup Applications

### Aerospace

```sh
cp ~/Development/knowledge/apple-computer-setup/aerospace.toml ~/.aerospace.toml
```
