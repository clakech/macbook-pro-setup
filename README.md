# macbook-pro-setup
Setup your brand new macbook pro

* Mostly Follow http://sourabhbajaj.com/mac-setup/index.html

* The End :-)

OK...

* Install Xcode
```
 xcode-select --install
```
* Install HomeBrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
* Install Homebrew Cask
```
brew tap caskroom/cask
```
* Install UI stuff
```
brew cask install iterm2
brew cask install atom
brew cask install webstorm
brew cask install slack
brew cask install virtualbox
brew cask install google-chrome
brew cask install java
brew cask install squirrelsql
```
* Install CLI stuff
```
brew install git
brew install zsh zsh-completions
brew install docker docker-machine docker-compose
brew install cntlm
```
* Install oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
* Set zsh theme to agnoster
```
ZSH_THEME="agnoster"
DEFAULT_USER="username"
```
* Switch shell to zsh
```
chsh -s /bin/zsh
```
* Configure iTerm2
Install font Meslo LG M Regular for Powerline
```
git clone https://github.com/powerline/fonts.git ~/tempFonts
~/tempFonts/install.sh
Go to ~/Library/Fonts and install font Meslo LG M Regular for Powerline
```
Go to Preferences / Profiles / Text / Change Font / Meslo LG M Regular for Powerline
Go to Preferences / Profiles / Colors / Colors presets / Solarized Dark
