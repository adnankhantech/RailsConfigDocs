# Ruby on Rails Setup for Desktop and Server(Ubuntu 12.04)

## Install basic packages for Ubuntu

```
sudo apt-get install build-essential
sudo apt-get install zlib1g-dev
sudo apt-get install libssl-dev
sudo apt-get install gcc autoconf
sudo apt-get install libreadline-gplv2-dev
sudo apt-get install libxml2-dev
sudo apt-get install libxslt1-dev
```
## Required at the time of nginx installation
```
sudo apt-get install libcurl4-openssl-dev
```

## Setup Git Server
```
sudo apt-get install git-core
nano .gitconfig
---
[color]
branch = auto
diff = auto
interactive = auto
status = auto
[user]
name = firstname.lastname
email = first.last@icicletech.com
[merge]
tool = diffmerge
----
```

## Add following lines in .gemrc file
```
nano .gemrc
gem: --no-ri --no-rdoc
```

## Setup Sublime Text Editor
```
sudo apt-get remove sublime-text
sudo add-apt-repository ppa:webupd8team/sublime-text-2
sudo apt-get update
sudo apt-get install sublime-text-dev
```

## Setup RVM

## Installing RVM Pre-Requisites
```
sudo apt-get install curl
```
### Install RVM
```
\curl -L https://get.rvm.io | bash -s stable
```
### Reload RVM
```
source ~/.rvm/scripts/rvm
```
### Install RVM dependancies
```
rvm requirements
```
## Install Ruby
```
rvm install ruby
```
## Install RubyGems
```
rvm rubygems current
```
## Install Rails
```
gem install rails
```