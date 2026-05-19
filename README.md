# Setting up Mac
## 1. Install Homebrew
```zsh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Command line tools for Xcode is also installed

```zsh
echo >> ~/.zprofile
```

```zsh
echo 'eval "$(/opt/homebrew/bin/brew shellenv zsh)"' >> ~/.zprofile
```

```zsh
eval "$(/opt/homebrew/bin/brew shellenv zsh)"
```

# Old Steps
## 3. Install Node.js
- `16.15.1 LTS`
```zsh
brew install node@16

echo 'export PATH="/opt/homebrew/opt/node@16/bin:$PATH"' >> ~/.zshrc
```

## 4. Install Visual Studio
```zsh
brew install --cask visual-studio-code
```

## 5. Install Docker
```zsh
brew install --cask docker

open /Applications/Docker.app
```

## 6. Install direnv
```zsh
brew install direnv
```

## 7. Install jq
```zsh
brew install jq
```

## 8. Install AWS Cli
```zsh
brew install awscli
```

## 9. Configure Git
```zsh
git config --global pull.rebase false
```

&nbsp;

# Misc
## Install NVM
```zsh
brew install nvm
mkdir ~/.nvm
echo "export NVM_DIR=~/.nvm\nsource $(brew --prefix nvm)/nvm.sh" > ~/.zshrc
source ~/.zshrc
nvm install node
nvm install 14
```
