## Mac Development Environment Config

I am a Frontend Developer and I use the MacBook Pro as my development computer.

So here I just record my development environment for the future.

### Install Homebrew

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### Use Homebrew to install packages

```bash
# Check the system
brew doctor

# Check the update
brew update

# Upgrade the packages
brew upgrade

# Cleanup the useless packages
brew cleanup

# Install packages
brew install ccat git mysql zsh nginx zsh-completions node@6 thefuck diff-so-fancy nvm tmux autojump macvim ruby wget catimg mongodb
```

### Use NVM to manage node.js

```bash
# List node verion
nvm ls

# List remote node version
nvm ls-remote [--lts]

# Install [lts] version
nvm install v6.11.2

# Use version
nvm use v6.11.2

# Use system version
nvm default alias system
nvm use system
```

### Use the zsh and install oh.my.zsh

```bash
# Change the default shell
chsh -s /bin/zsh

# via curl
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

# via wget
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

### Git config

```bash
# Config global user
git config --global user.name "Barry Chen"
git config --global user.email "funnychen38@gmail.com"

# Store pwd when pull and push
git config --global credential help.store
```

### Development tools

- [Sublime Text][1]
- [Visual Studio Code][2]
- [Google Chrome][3]
- [iTerm][4]
- [Postman][5]
- [Alfred][6]
- [Github Desktop][7]
- [PhotoShop CC][8]

<!-- Urls -->

[1]: https://www.sublimetext.com/
[2]: https://code.visualstudio.com/
[3]: https://www.google.com/chrome/browser/desktop/index.html
[4]: https://www.iterm2.com/
[5]: https://www.getpostman.com/postman
[6]: https://www.alfredapp.com/
[7]: https://desktop.github.com/
[8]: http://www.adobe.com/products/photoshop.html?promoid=PC1PQQ5T&mv=other
