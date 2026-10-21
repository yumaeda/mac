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

## 2. Install Chrome
```zsh
brew install --cask google-chrome
```

## 3. Install Docker
```zsh
brew install --cask docker

```

## 4. GitHub CLI
### Install
```zsh
brew install gh
```

### Login
```zsh
gh auth login
```

### Configure
```zsh
git config user.name "Your Name"
git config user.email "your-email.com"
```

## 5. Install Visual Studio
```zsh
brew install --cask visual-studio-code
```

## 6. Install herdr
```zsh
brew install herdr
```

## 7. Install Claude Code
```zsh
brew install --cask claude-code
```

## 8. oMLX
### Install
```zsh
brew tap jundot/omlx https://github.com/jundot/omlx
brew install omlx
```

### Start oMLX
```zsh
brew services start omlx
```

### Download Models
Open admin dashboard
```zsh
open http://localhost:8000/admin
```
Download a model

### Configure .zshrc
```zsh
echo 'export CLAUDE_CODE_ATTRIBUTION_HEADER="0"' >> ~/.zshrc
echo 'export ANTHROPIC_BASE_URL="http://localhost:8000/v1"' >> ~/.zshrc
echo 'export ANTHROPIC_AUTH_TOKEN="local"' >> ~/.zshrc
echo 'export ANTHROPIC_API_KEY="local"' >> ~/.zshrc
echo 'export ANTHROPIC_DEFAULT_SONNET_MODEL="mlx-community/Qwen3.8-27B-mxfp4"' >> ~/.zshrc
echo 'export ANTHROPIC_DEFAULT_OPUS_MODEL="mlx-community/Qwen3.8-27B-mxfp4"' >> ~/.zshrc
source ~/.zshrc
```

### Launch Claude
```zsh
omlx launch claude
```

### Stop oMLX
```zsh
brew services stop omlx
```
