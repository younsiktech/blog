---
title: "Install Iterm2 & Homebrew"
date: 2022-04-23T23:00:45+09:00
description: Iterm2 installation on Mac
menu:
  sidebar:
    name: Install Iterm2 & Homebrew
    identifier: tip-install-homebrew-iterm2
    parent: tip
    weight: 10
hero: images/forest.jpg
tags: ["Iterm2","Mac","M1","Intel","Homebrew"]
categories: ["Basic"]
---

## NOTICE 
M1 Mac & Intel Mac have same steps at 2022.04.06.

## Install Iterm2

### 1. Move to [official site](https://iterm2.com) and download current version

### 2. Install downloaded DMG

### 3. Iterm2 Preference Setting (Optional & Choice your prefer)

#### 1) Title bar style
```text
Appearance > Theme: Minimal 
```

#### 2) 1px line remove under the Title bar
```text
Appearance > Windows > Show line under title bar when the tab bar is not visible: Don't Check
```

#### 3) Change Text Settings
```text
Profiles > Text : Mostly font size
```

#### 4) Change Margin
```text
Appearance > Panes > Side margins: 12
Appearance > Panes > Top & bottom margins: 10
```

#### 5) Remove Tab outline
```text
Advanced > In minimal theme, how prominent should the tab outline be?: 0
```

#### 6) Set Unicode
````text
Profiles > Text > Unicode normalization form: NFC
````

#### 7) Enable Status Bar
```text
Preferences > Profiles > Session > Status bar enabled
```

#### 8) Set Status bar location
```text
Preferences > Appearance > Status bar location
```

## Install Homebrew at Iterm2

### 1. Install Command Line Tool

Type this command

```shell
xcode-select --install
```

If you have current version, will not install.

### 2. Install HomeBrew

Type this command

```shell
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### 3. Open your .zprofile file at Home directory

Open your .zprofile file using vim

```shell
vim ~/.zprofile
```

### 4. add this line at your .zprofile file

```shell
eval "$(/opt/homebrew/bin/brew shellenv)"
```

### 5. Adjust brew

Type this command at Iterm2 or Close your Iterm2 and reopen

```shell
eval "$(/opt/homebrew/bin/brew shellenv)"
```

## Favorite Brew Install List

```shell
# font
brew install homebrew/cask-fonts/font-d2coding
brew install homebrew/cask-fonts/font-jetbrains-mono

# iterm
brew install neofetch
brew install jq
brew install rg
brew install lsd
brew install tree
brew install fasd
```