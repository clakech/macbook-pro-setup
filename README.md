# macbook-pro-setup #NodeJS #Docker #iTerm2 #Atom #WebStorm #ZSH
Setup your brand new macbook pro

* Mostly Follow http://sourabhbajaj.com/mac-setup/index.html
* The End :-)

OK... Quick reminder!

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
```
* Install CLI stuff
```
brew install git
brew install zsh zsh-completions
brew install docker docker-machine docker-compose
```
* Install oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
* Set zsh theme to agnoster in .zshrc
```
ZSH_THEME="agnoster"
DEFAULT_USER="yourusername"
```
* Switch shell to zsh
```
chsh -s /bin/zsh
```
* Configure iTerm2
 * Install font Meslo LG M Regular for Powerline
  ```
  git clone https://github.com/powerline/fonts.git ~/tempFonts
  ~/tempFonts/install.sh #delete it one day ;)
  ```
 * Go to ~/Library/Fonts and install font Meslo LG M Regular for Powerline
 * Go to iTerm2 / Preferences / Profiles / Text / Change Font / Meslo LG M Regular for Powerline
 * Go to iTerm2 / Preferences / Profiles / Colors / Colors presets / Solarized Dark
* Configure your EDITOR
```
export EDITOR="atom -w"
alias edit="atom -nw"
```
* Configure git
```
git config --global user.name "Your Name Here"
git config --global user.email "your_email@youremail.com"

git config --global credential.helper osxkeychain

git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status
```
* Install NodeJS
 * Install NVM
 ```
 curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
 ```
 * Restart iTerm2
 * Install Node LTS
 ```
 nvm install --lts
 ```
* Configure Docker
```
docker-machine create -d virtualbox default
```
