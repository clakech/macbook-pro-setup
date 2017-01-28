# My MacBook Pro setup
#NodeJS #Docker #iTerm2 #Atom #WebStorm #ZSH

Setup your brand new macbook pro like a pro

## Mostly Follow [http://sourabhbajaj.com/mac-setup/index.html](http://sourabhbajaj.com/mac-setup/index.html)

## The End 😎

> OK... let's share a quick reminder!

## Install Xcode, *on macOS, you can't dev without Xcode*

```bash
 xcode-select --install
```

## Install HomeBrew, *a tool to install CLI tools without copy/paste*

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Install Homebrew Cask, *a tool to install UI tools without monkey clicking*

```bash
brew tap caskroom/cask
```

## Install tools for devs, *a short must have list*

```bash
#what else?
brew install git

#customizable terminal
brew cask install iterm2

#customizable editor
brew cask install atom

#IDE for web dev
brew cask install webstorm

#to keep in touch with your team
brew cask install slack

#best web dev browser ^^
brew cask install google-chrome 
```

## Install ZSH & co, *the best shell for devs [#mustHave](https://github.com/robbyrussell/oh-my-zsh/wiki/Cheatsheet)*

```bash
brew install zsh zsh-completions

#install oh-my-zsh, a zsh configuration helper
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## Configure your ZSH on steroids, *add these lines to your ~/.zshrc*

```bash
plugins=(git colored-man colorize github jira vagrant virtualenv pip python brew osx zsh-syntax-highlighting)

ZSH_THEME="agnoster"
DEFAULT_USER="yourusername"
```

## Configure shell to use zsh, *type this line in your iTerm2 shell*

```bash
chsh -s /bin/zsh
```

### Restart iTerm2

## Configure iTerm2

Install font Meslo LG M Regular for Powerline
 
```zsh
git clone https://github.com/powerline/fonts.git ~/tempFonts

~/tempFonts/install.sh
```
  
Go to ~/Library/Fonts and install font Meslo LG M Regular for Powerline

Go to iTerm2 / Preferences / Profiles / Text / Change Font / Meslo LG M Regular for Powerline

Go to iTerm2 / Preferences / Profiles / Colors / Colors presets / Solarized Dark

Delete ~/tempFonts/

```zsh
rm -Rf ~/tempFonts
```

## Tada 🎉

![](iTerm2zshAgnoster.png?raw=true)

## Configure your editor, *add these lines to your ~/.zshrc*

```zsh
export EDITOR="atom -w"
alias edit="atom -nw"
```

## Configure git

```zsh
git config --global user.name "Your Name Here"
git config --global user.email "your_email@youremail.com"

git config --global credential.helper osxkeychain

git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status
```

## Install NodeJS

### Install NVM, *to manage multiple NodeJS versions*

```zsh
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
```
 
### Restart iTerm2, *or `touch ~/.zshrc`*

### Install NodeJS LTS, *latest long term supported version*
 
```zsh
nvm install --lts
```

## Configure Docker *using HyperKit (xhyve)*

```zsh
brew cask install Docker

docker run hello-world
```

**or**

## Configure Docker *using virtualbox*

```zsh
brew cask install virtualbox

brew install docker docker-machine docker-compose

docker-machine create -d virtualbox default

eval "$(docker-machine env default)"

docker run hello-world
```

Please contribute to improve this and share it to the world if you like it 😉

/me on twitter [@cyril_lakech](https://twitter.com/cyril_lakech)
