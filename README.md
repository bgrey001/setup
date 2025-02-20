## setup

### mac


install brew first

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

```
touch ~/.zshrc
echo "export PATH=/opt/homebrew/bin:$PATH" > ~/.zshrc
```

install git

```
brew install git
```


### debian

```
sudo apt install git-all
```


set git config

```
git config --global user.name "<name>"
```

```
git config --global user.email "<email>"
```

generate SSH key (add SSH to GitHub profle)

```
ssh-keygen -t ed25519-sk -C "<email>"
```

if invalid format error:

```
ssh-keygen -t rsa -b 4096 -C "<email>"
```


install oh my zsh

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

theme (add to .zshrc)

if you want P10k, install here:

```
https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh
```

```
ZSH_THEME="powerlevel10k/powerlevel10k"
```

install plugins for oh my zsh

```
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

```
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting
```

```
git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git $ZSH_CUSTOM/plugins/zsh-autocomplete
```

add to .zshrc

```
export PATH=/opt/homebrew/bin:$PATH
```

```
plugins=(git zsh-autosuggestions zsh-syntax-highlighting fast-syntax-highlighting zsh-autocomplete)
```


install pyenv

```
brew install pyenv
```

install dedicated python version with pyenv (e.g. 3.11.10)

```
pyenv install 3.11.10
```


```
pyenv local 3.11.10
```

or 

```
pyenv global 3.11.10
```

poetry set to use this version (in directory with pyproject.toml)

```
poetry env use $(pyenv which python)
```
