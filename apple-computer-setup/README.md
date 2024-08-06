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

# Bash Profile

```
# Git
alias gs="git status"
alias gpoh="git push origin head"
alias gpch="git push cfn head"
alias gpm="git pull origin master"
alias gb="git branch"
alias gc="git commit"
# Print out the commits made since the tip of the master branch. (gnc stands for -> git new commits)
alias gnc="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr)%Creset' --abbrev-commit --date=relative master..head"
# Prevent git checkout from auto-completing branches on origin because it's almost never what I'm intending
export GIT_COMPLETION_CHECKOUT_NO_GUESS=1
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

## Setting up Git

#### Git user configuration
```sh
git config --global user.name "Chinedu Francis Nwafili"
git config --global user.email "frankie.nwafili@gmail.com"
git config --global user.username "chinedufn"
```

#### Git GPG key

Follow instructions in `gpg.md` for setting up a GPG key

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

```

## Setup Applications

### Aerospace

```sh
cp ~/Development/knowledge/afia/apple-computer-setup/aerospace.toml ~/.aerospace.toml
```
