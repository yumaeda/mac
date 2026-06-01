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

## 3. GitHub CLI
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

## 4. Install Visual Studio
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
ollama pull gemma4:31b
ollama pull batiai/qwen3.6-35b:q4
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

## LiteLLM
### Install
```zsh
brew install uv
uv tool install --python 3.12 'litellm[proxy]' --force
echo 'export PATH="/Users/yumaeda/.local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

### Create the Config File (litellm_config.yaml) for Ollama in your workspace folder and paste below setup
```zsh
model_list:
  - model_name: "*" # This catches ALL model names sent by Claude Code
    litellm_params:
      model: openai/batiai/qwen3.6-35b:q4
      api_base: http://localhost:11434/v1
      enable_tool_choice: true

litellm_settings:
  drop_params: true  # This strips out 'context_management' automatically
  additional_drop_params: ["reasoning_effort", "reasoning.effort", "context_management"]
  success_callback: []
  failure_callback: []
```

### Run below command in a new Terminal
```zsh
litellm --config litellm_config.yaml --port 4000
```

## Claude Code
### Install
```zsh
brew install --cask claude-code
```

### Configure .zshrc
```zsh
echo 'export CLAUDE_CODE_PACKAGE_MANAGER_AUTO_UPDATE=1' > ~/.zshrc
echo 'export ANTHROPIC_BASE_URL="http://localhost:4000"' >> ~/.zshrc
echo 'export ANTHROPIC_AUTH_TOKEN="local"' >> ~/.zshrc
source ~/.zshrc
```

### Launch
```zsh
claude
```
