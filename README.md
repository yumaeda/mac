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

## 6. Ollama
### Install
```zsh
brew install ollama
```

### Start Ollama
```zsh
brew services start ollama
```

### Get Process
```zsh
ollama ps
```

### Stop Ollama
```zsh
brew services stop ollama
```

### Pull Manifests
```zsh
ollama pull batiai/qwen3.6-35b:q4
ollama pull qwen3.6:35b-a3b-coding-nvfp4
```

### List all downloaded models
```zsh
ollama list
```

### Launch the model locally
```zsh
ollama run $MODEL
```

### Unload the Model from Mac
```zsh
ollama stop $MODEL
```

## Claude Code
### Install
```zsh
brew install --cask claude-code
```

### Configure .zshrc
```zsh
echo 'export CLAUDE_CODE_PACKAGE_MANAGER_AUTO_UPDATE=1' >> ~/.zshrc
echo 'export OLLAMA_CONTEXT_LENGTH=32768' >> ~/.zshrc
echo 'export ANTHROPIC_BASE_URL="http://localhost:11434/v1"' >> ~/.zshrc
echo 'export ANTHROPIC_AUTH_TOKEN="ollama"' >> ~/.zshrc

source ~/.zshrc
```

### Launch
```zsh
ollama launch claude --model $MODEL
```
