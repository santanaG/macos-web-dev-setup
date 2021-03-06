Development environment setup after a clean Mac OS install
===================

This is what is use as a playground. I mainly do full stack js with react / meteor / raw node and sometimes ember. Rarely python or ruby and some PHP legacy code.

At first, check updates via the appstore.

> To add a directory to the PATH : export PATH="/usr/local/...:$PATH"

Display hidden folders :
* `defaults write com.apple.finder AppleShowAllFiles YES`
* `killall Finder`

## Basic settings

In the system preferences

* general
	* icon size > small
	* Use dark menu bar and dock
* desktop > choose a nice wall paper !
* dock
	* small size, small magnifiying
	* bottom
	* hide automatically
* mouse / trackpad
	* desactivate natural way
	* tap to click and two tap to right clic
* security
	* allow application from anywhere

## Get your terminal ready

1. Install iterm 2 <http://www.iterm2.com/>
2. Uncheck "User Lion-style Fullscreen"
3. Add ctrl + esc as hotkey to make it appear
4. Go full screen
5. Get the [cobalt theme](https://github.com/wesbos/Cobalt2-iterm)
6. Make it Launch on startup in the global mac os preferences
7. Make it default
8. Add 20% transparency
9. Install oh-my-zsh : `curl -L http://install.ohmyz.sh | sh` and restart the terminal
10. Download and install the patched version of inconsolata from [powerline fonts](https://github.com/powerline/fonts)
11. Set it as default font for ascii and non ascii characters (13pt)
12. Install [agnosterzak](https://github.com/zakaziko99/agnosterzak-ohmyzsh-theme) and set  `ZSH_THEME="agnosterzak"` in `~/.zshrc`
13. Install Xcode from the appStore and then the Xcode dev tools with `xcode-select --install`
14. Install Mac port to get the linux commands : https://www.macports.org/

## Get the /usr/local ownership

  sudo chown -R $USER /usr/local

> This will make you owner of your /usr/local folder. [Important for npm use.](http://foohack.com/2010/08/intro-to-npm/#what_no_sudo)

## Install broswers

Get chrome, canary and firefox. Add some extensions to chrome :

* adblock plus
* adobe edge inspect
* advanced rest client
* ember inspector
* livereload
* markdown here
* page speed

## Install a package manager

Get homebrew :

	ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

Install a few packages :

* git
* wget
* svn
* mysql
* node
* mongo

## Install some web packages

* Install compass and sass : `gem install compass` => even if you use libsass most of the time
* Install gulp `npm i -g gulp`
* Install grunt `npm i -g grunt`
* Install bower `npm i -g bower`
* Install webpack `npm i -g webpack`
* Install yeoman : `npm i -g yo`
* Install meteor `curl https://install.meteor.com/ | sh`

## Install source control

Get the base git and svn. Then install source tree for Git, the github client and cornerstone for svn.

Configure your git credentials :

    git config --global user.name "fabien"
    git config --global user.email "fabien.huet@gmail.com"

Create SSH key :

    ssh-keygen -t rsa -b 4096 -C "fabien.huet@gmail.com"

Then copy it with :

    pbcopy < ~/.ssh/id_rsa.pub

Then add it to gothub and bitbucket account

## Install MAMP

Because sometimes, you will need PHP. <http://www.mamp.info/en/downloads/>

## Get your editor ready

Get sublime text : <http://www.sublimetext.com/3>, install the package control packages : <https://sublime.wbond.net/installation> and then some packages :

* advanced new file
* bracket highligther
* emmet
* find++
* handlebars
* HTML prettify
* html5
* javascript snippets
* babel
* jquery
* meteor snippets
* scss
* scss snipets
* DocBlockr
* sidebad enhancements
* sublime linter
* sublime linter jsxhint
* theme material https://packagecontrol.io/packages/Material%20Theme

Ad sublime command to your path
ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/sublime

> install the npm module for eslint

Tweak the user settings :

	{
		"color_scheme": "Packages/Material Theme/schemes/Material-Theme-Palenight.tmTheme",
		"folder_exclude_patterns":
		[
			".meteor",
			".git",
			".hg",
			".svn"
		],
		"ignored_packages":
		[
			"Vintage"
		],
		"indent_to_bracket": true,
		"material_theme_accent_pink": true,
		"material_theme_accent_scrollbars": true,
		"material_theme_bullet_tree_indicator": true,
		"material_theme_compact_sidebar": true,
		"material_theme_contrast_mode": true,
		"material_theme_small_statusbar": true,
		"material_theme_tabs_autowidth": true,
		"material_theme_tabs_separator": true,
		"scroll_past_end": true,
		"tab_size": 4,
		"theme": "Material-Theme-Palenight.sublime-theme",
		"translate_tabs_to_spaces": false,
		"trim_trailing_white_space_on_save": true,
		"word_wrap": "true"
	}

## Install other applications

### Utilities

1. **Alfred**. Big improvement to spotlight : <https://itunes.apple.com/fr/app/alfred/id405843582?mt=12>
2. **Dropbox** & **Google drive** To keep your datas safe. <https://itunes.apple.com/fr/app/xcode/id497799835?mt=12>, <https://drive.google.com>
3. **Mu torrent** You know what this is for <http://www.utorrent.com/>
4. **VLC** Best video player <http://www.videolan.org/vlc/>
7. **onyx** to manage mac os preferences <http://www.titanium.free.fr/downloadonyx.php>
8. **disk inventory x** <http://www.derlien.com/>
9. **Transmit** for FTP <https://panic.com/transmit/>
10. **Mou** to edit markdown <http://mouapp.com/>
12. **keepingyouawake** to prevent your mac from going to sleep <https://github.com/newmarcel/KeepingYouAwake> install with `brew cask install keepingyouawake`
13. **SourceTree** for your git client
14. **Robomongo** : http://robomongo.org/ to manage distant database
15. **little snitch** : https://www.obdev.at/products/littlesnitch/index.html => manage in and out connections
16. **slack** : https://slack.com/is
17. **lightshot** : https://app.prntscr.com/en/

### Graphic / design softwares

The one I use

1. **Photoshop** & **aperture** for pictures
2. **Illustrator** to design elements
3. **Indesign** for documents
4. **Sketch** for interface
5. **Final cut** for video
6. **Audition** & **logic** for sound
7. **jpeg mini** to optimize jpeg
8. **img optim** to optimize the other images
9. **skyfont** to get google webfonts on my computer
10. **Font prep** to build font sets to inject
11. **axure** to build wireframe

### xcode

What you want is not excatly xcode. What you want is the ios devices simulator. From far the best way to preview a design on an iphone or an ipad. <https://itunes.apple.com/fr/app/xcode/id497799835?mt=12>. There are many problem you will just never encounter in chrome that you need to adress. The simulator is perfect for that.

