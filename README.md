# Setting up Mac
## 1. Install command line tools for Xcode
```bash
xcode-select --install
```

## 2. Install Homebrew
```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## 3. Install Chrome
```bash
brew cask install google-chrome
```

## 4. Install Git by Homebrew
```bash
brew install git
```

## 5. Add git bin to the $PATH
```bash
echo 'export PATH="/usr/local/Cellar/git/2.5.0/bin:$PATH"' >> ~/.bash_profile
```

## 6. Install Node
```bash
brew install node
```

## 7. Install Git Flow
```bash
brew install git-flow
```
