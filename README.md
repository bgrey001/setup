## setup

### mac


install brew first

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

```
touch ~/.zshrc
echo "" > ~/.zshrc
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

generate SSH key

```
ssh-keygen -t ed25519-sk -C "<email>"
```

if invalid format error:

```
ssh-keygen -t rsa -b 4096 -C "<email>"
```

add SSH to profle



clone repo


```
git clone <repo>
```


