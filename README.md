# Mac Setup instructions

So configuring a new Mac is a right pain and a time consuming task at that, having done this several times over the past few months, I thought id write down the important content.  It will be useful for myself but hopefully some else too.

##  Core Applications

* Google Chrome - [install instructions](https://www.google.co.uk/chrome/browser/features.html)
  * This is an obvious one, Safari just doesn't cut-it,
* Atom - [install instructions](https://atom.io/)
  * Universal text editor and simple IDE
* Day-0 - [install instructions](https://shauninman.com/archive/2016/10/20/day_o_2_mac_menu_bar_clock)
  * A simple calendar widget, which allows you to view days of week from tool bar.
* Iterm - [install instructions](https://www.iterm2.com/downloads.html)
  * Replacement Terminal for MacOSX.
* Docker (Install)[https://docs.docker.com/docker-for-mac/install/]
  * Container development environment of choice, remember to increase default memory size for containers.
* xCode command-line tools, needed for many apps.
  * If you plan to use XCode as an IDE you may aswell download that as it will install the command-line tools, but if you install thenm independantly. `xcode-select --install`
* HomeBrew [Install Instructions](https://brew.sh/)
  * The missing Package manager for OS, think `apt-get` or `yum` but for osx.
  * do some updates `brew tap caskroom/versions` & `brew update`

## Homebrew

Java Latest JDK - installing java via brew is more convenient, the install puts java in the following location:  `/Library/Java/JavaVirtualMachines/jdkXXX.jdk/Contents/Home/bin/java`

* `brew cask install java`

Other useful tools:

* bash-completion - `brew install bash-completion`
* git - `brew install git`
* SBT - `brew install sbt`
* Scala - `brew install scala`
* Maven - `brew install maven`
* awscli - `brew install awscli`
* npm - `brew install npm`

## Generate Github SSH key

Generate a new SSh key for the Machine
https://help.github.com/enterprise/2.13/user/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/

Add the Public key to Github
https://help.github.com/enterprise/2.13/user/articles/adding-a-new-ssh-key-to-your-github-account/

## GitConfig

Lets setup some useful config and sortcuts for using Git from the terminal, lets start with the base config.

Copy the .gitconfig in this repo to your home directory

```
> cp .gitconfig ~/.gitconfig
```

Then edit the `.gitconfig` file and replace the name & email values.

```
> atom ~/.gitconfig
```

## Shell Config

If your like me and use lots frameworks and build tools, its sometimes difficult to remember all the commands to tidy up or debug.  Lets add them to a shell functions file so we can access them when needed.

Copy shell functions folder `.shell` in this repo into your home directory.

`cp -R .shell ~/.shell`

Ok so now lets pimp your shell, zsh offers great auto complete and other great features not to mention it looks great too.

install oh my ZSH - [install instructions](http://ohmyz.sh/)

lets add some extra functionality.

* `brew install zsh-autosuggestions`
* `brew install zsh-completions`

Compare the `.zshrc` config file in this repo with the one in your home directory. There are a few tweaks and settings.


credits:
 https://justin.abrah.ms/dotfiles/zsh.html
