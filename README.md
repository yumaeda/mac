# Setting up Mac
## 1. Install command line tools for Xcode
```zsh
xcode-select --install
```

## 2. Install Homebrew
```zsh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 3. Install nvm
```zsh
brew install nvm
echo 'export NVM_DIR=~/.nvm' >> ~/.zshrc
source $(brew --prefix nvm)/nvm.sh
```

## 4. Install Chrome
```zsh
brew cask install google-chrome
```

## 5. Install Git by Homebrew
```zsh
brew install git
```

## 6. Add git bin to the $PATH
```zsh
echo 'export PATH="/usr/local/Cellar/git/2.5.0/bin:$PATH"' >> ~/.bash_profile
```
