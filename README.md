# My MacBook Pro setup [https://clakech.github.io/macbook-pro-setup/](https://clakech.github.io/macbook-pro-setup/)

\#NodeJS #Docker #iTerm2 #Atom #WebStorm #ZSH

Setup your brand new macbook pro like a pro

## Mostly Follow [http://sourabhbajaj.com/mac-setup/index.html](http://sourabhbajaj.com/mac-setup/index.html)

## The End 😎

> OK... let's share a quick reminder!

## Install Xcode, *on macOS, you can't dev without Xcode*

```bash
 xcode-select --install
```

## Install [HomeBrew](http://brew.sh/), *a tool to install CLI tools without copy/paste*

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Install [Homebrew Cask](https://caskroom.github.io/), *a tool to install UI tools without [monkey clicking](https://github.com/caskroom/homebrew-cask/blob/master/USAGE.md)*

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

#replace spotlight with alfred
brew cask install alfred

#manage windows with keyboard shortcuts
brew cask install spectacle

#type emoticons easily everywhere
brew cask install rocket
```

## Install ZSH & co, *the best shell suite for devs [#mustHave](https://github.com/robbyrussell/oh-my-zsh/wiki/Cheatsheet)*

```bash
brew install zsh zsh-completions

#install oh-my-zsh, a zsh configuration helper
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

#install auto suggestions plugin
git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

```

## Configure your ZSH on steroids, *add these lines to your ~/.zshrc*

```bash
plugins=(git colored-man colorize github jira vagrant virtualenv pip python brew osx zsh-syntax-highlighting zsh-autosuggestions)

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

Go to iTerm2 / Preferences / Profiles / Text / Change Font / Meslo LG M Regular for Powerline.
Make sure the option `Use a different font for non-ASCII character` is **not** checked.

Go to iTerm2 / Preferences / Profiles / Colors / Colors presets / Solarized Dark

Go to iTerm2 / Preferences / Profiles / Windows / Transparency + Blur

Delete downloaded font files

```zsh
rm -Rf ~/tempFonts
```

## Tada 🎉

![](iTerm2zsh.png?raw=true)

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
#see all default oh-my-zsh git aliases https://github.com/robbyrussell/oh-my-zsh/wiki/Cheatsheet#git
```

## Install NodeJS

### Install [NVM](https://github.com/creationix/nvm), *to manage multiple NodeJS versions*

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

## Manage your dotFiles using git, *[because you may want to review history one day](http://dotfiles.github.io/)*

```zsh
#goto your home dir, using zsh no need to cd ~ 
cd

#create a git repo ignoring all files to avoid sharing sensistive stuff
git init
echo "*" > .gitignore

#git force add file you WANT to manage
ga -f .zshrc
...

#git commit all added files, gca = git commit -v -a thanks to oh-my-zsh
gca

#optional but recommanded, if you setup a git remote to backup your files using github for instance
git push origin master
```

## update (most of) your dev tools, *in (almost) 1 line*

```zsh
brew update && brew upgrade
```

## have fun 

```zsh
sudo gem install lolcat

brew install cowsay ponysay fortune

#add a combinaison of nawak at the end of .zshrc or .zlogin
fortune | ponysay
#or
fortune | cowsay | lolcat
```

🎉
![](ponysay.png?raw=true)

Please contribute to improve this and share it to the world if you like it 😉

/me on twitter [@cyril_lakech](https://twitter.com/cyril_lakech)
