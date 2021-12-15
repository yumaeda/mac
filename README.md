# Setting up Mac
## 1. Install command line tools for Xcode
```zsh
xcode-select --install
```

## 2. Install Homebrew
```zsh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew update
```

## 3. Install NVM
```zsh
brew install nvm
mkdir ~/.nvm
echo "export NVM_DIR=~/.nvm\nsource $(brew --prefix nvm)/nvm.sh" > ~/.zshrc
source ~/.zshrc
nvm install node
nvm install 14
```

## 4. Install Visual Studio
```zsh
brew install --cask visual-studio-code
```

## 5. Install Docker
```zsh
brew install --cask docker
```

## 6. Install AWS Cli
```zsh
brew install awscli
```

## 7. Configure Git
```zsh
git config --global pull.rebase false
```
