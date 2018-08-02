# macOS Development Environment Config

I am a Frontend Developer and I use the MacBook Pro as my development computer. So here I just record my development environment for the future if I buy a new Mac.

## Editors

I choose these two as my main development editors, both are light and beautify. But you have to install many plugins to make it near an "IDE". For a frontend developer, it's already perfect.

[Sublime Text][1]

> More details please see [sublime-config][101]

[Visual Studio Code][2]

> More details please see [vscode-config][201]

## Browser

[Google Chrome][3] must be the most recommend browser for develop. As the version upgrade, the UI becomes more beautify and you can see more Material Design in it. Also you can install many plugins as you want to make your development more easily.

Here are my installed plugins:

- [ExpressVPN for Chrome][301]
- [The Great Suspender][302]
- [Adblock Plus][303]
- [Vue.js devtools][304]
- [Vimium][305]
- [EditThisCookie][306]
- [Sizzy][307]
- [Simple QR Generator][308]
- [Blank New Tab Page][309]
- [Awesome Autocomplete for GitHub][310]
- [Isometric Contributions][311]
- [JSONView][312]
- [Octotree][313]

## Terminal

I use [iTerm2][4] plus [tmux][5]. They are prefect partners if you use them well. But I think I am not that guy, just a simple user who use this to show off. Just kidding, I am learning this how to use it better.

You can check my tmux config [here][7].

## Productivity

I use [Alfred][6] to replace the Spotlight Search, it has a workflows thing, like plugins to make it self stronger more a search tool.

Here are my installed [workflows][600]:

- BetterZip
- [Can I Use][601]
- [Colors][602]
- [Emoji][603]
- [Encode/Decode][604]
- Express Inquiry
- [IP Address][606]
- [Kill Process][607]
- [Uninstall with CleanMyMac 3][608]
- [Wunderlist][609]
- 人民币金额大写

> It already provides many useful commands to make search efficiently, but you still can add more and make it stronger.

## Other Tools

I also use other tools more than like packages, but really useful.

### Homebrew

Install:

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Daily using commands:

```bash
# Check the system if it is OK
brew doctor

# Check the update
brew update

# Upgrade the outdated packages
brew upgrade

# Cleanup the outdated packages
brew cleanup

# Install packages
brew install [package_name]

# Search the package if existed
brew search [package_name]

# List the detail of one package
brew info [package_name]
```

Using cask to install macOS applications, first of all, you should add this tap:

```bash
brew tap caskroom/cask
```

then you can install with this:

```bash
brew cask install [application_name]
```

### nvm

This is Node.js version manager, it is useful when you have multiple versions of Node.js. And the commands are easy, only remember those:

```bash
# List local node verion and using detail
nvm ls

# List remote LTS node version
nvm ls-remote [--lts]

# Install LTS version
nvm install v6.11.2

# Use a version
nvm use v6.11.2

# Use system version
nvm default alias system
nvm use system
```

### zsh/oh-my-zsh

Default shell env in Mac is bash, but it is not good at all. When you checkout to [zsh][8] and pluse [oh-my-zsh][9], it's really amazing. This is the terminal should suppose to be.

```bash
# Change the default shell
chsh -s /bin/zsh

# Via curl
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

# Via wget
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

### Git

As we all know, it is a popular code version control tool. When I install it, my first thing is to config it in global. Then I can think it is mine now.

```bash
# Config global user
git config --global user.name "Barry Chen"
git config --global user.email "funnychen@outlook.com"

# Store password when pull and push
# See https://git-scm.com/docs/git-credential-store
git config credential help.store
```

### Nginx

I use this as my local server when developing simple H5 or other things. Just see the details [here][10].

### Vim

An acient editor and exists as a legend, I can use it a little. Just see the details [here][11].

### System Commands

```bash
# Cancel the delay after hover to the edge of dock side
defaults write com.apple.dock autohide-delay -float 0; killall Dock

# Disable chrome two-finger back/forward navigation
defaults write com.google.Chrome AppleEnableSwipeNavigateWithScrolls -bool FALSE
```

<!-- URLs -->

[1]: https://www.sublimetext.com/
[101]: https://github.com/Chen38/sublime-config

[2]: https://code.visualstudio.com/
[201]: https://github.com/Chen38/vscode-config

[3]: https://www.google.com/chrome/browser/desktop/index.html
[301]: https://www.expressvpn.com/
[302]: https://github.com/deanoemcke/thegreatsuspender
[303]: https://adblockplus.org/
[304]: https://github.com/vuejs/vue-devtools
[305]: http://vimium.github.io/
[306]: http://www.editthiscookie.com/
[307]: https://kitze.io/
[308]: https://github.com/feelinglucky/chrome-plugin-simple-qr-generator
[309]: https://www.h3xed.com/web-and-internet/how-to-get-a-blank-new-tab-page-in-chrome
[310]: https://www.algolia.com/
[311]: https://github.com/jasonlong/isometric-contributions
[312]: https://github.com/gildas-lormeau/JSONView-for-Chrome
[313]: https://github.com/buunguyen/octotree/

[4]: https://www.iterm2.com/
[5]: https://github.com/tmux/tmux

[6]: https://www.alfredapp.com/
[600]: https://github.com/Chen38/mac-dev-config/tree/master/AlfredWorkflows
[601]: https://github.com/willfarrell/alfred-caniuse-workflow
[602]: http://www.packal.org/workflow/colors
[603]: https://github.com/carlosgaldino/alfred-emoji-workflow
[604]: https://github.com/willfarrell/alfred-encode-decode-workflow
[606]: http://dferg.us/ip-address-workflow/
[607]: https://github.com/ngreenstein/alfred-process-killer
[608]: http://www.packal.org/workflow/uninstall-cleanmymac-3
[609]: http://www.packal.org/workflow/wunderlist-workflow-alfred

[7]: https://github.com/Chen38/mac-dev-config/blob/master/.tmux-conf
[8]: https://github.com/zsh-users/zsh
[9]: https://github.com/robbyrussell/oh-my-zsh
[10]: https://github.com/Chen38/mac-dev-config/blob/master/nginx.conf
[11]: https://github.com/Chen38/mac-dev-config/blob/master/.vimrc
