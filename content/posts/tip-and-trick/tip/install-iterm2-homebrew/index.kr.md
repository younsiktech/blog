---
title: "Iterm2 & Homebrew 설치"
date: 2022-04-23T23:00:45+09:00
description: Iterm2 installation on Mac
menu:
  sidebar:
    name: Iterm2 & Homebrew 설치
    identifier: tip-install-homebrew-iterm2
    parent: tip
    weight: 10
hero: images/forest.jpg
tags: ["Iterm2","Mac","M1","Intel","Homebrew"]
categories: ["Basic"]
---

## NOTICE
2022.04.06. 기준으로 M1 Mac & Intel Mac 설치 과정이 동일함

## Iterm2 설치

### 1. 다음 [공식 사이트](https://iterm2.com)에 접속해서 최신 버전을 다운로드 받습니다

### 2. DMG 파일을 설치합니다

### 3. Iterm2 Preference 세팅을 합니다 (선택 & 원하는 값으로 변경)

#### 1) 제목 표시줄 스타일 변경
```text
Appearance > Theme: Minimal 
```

#### 2) 제목 표시줄 아래 1px 라인 제거
```text
Appearance > Windows > Show line under title bar when the tab bar is not visible: Don't Check
```

#### 3) Text 관련 세팅 (폰트, 자간 etc.)
```text
Profiles > Text : Mostly font size
```

#### 4) 여백 변경
```text
Appearance > Panes > Side margins: 12
Appearance > Panes > Top & bottom margins: 10
```

#### 5) 탭 선 제거
```text
Advanced > In minimal theme, how prominent should the tab outline be?: 0
```

#### 6) Unicode 설정 (한글 깨짐 이슈 해결)
````text
Profiles > Text > Unicode normalization form: NFC
````

#### 7) 상태바 활성화
```text
Preferences > Profiles > Session > Status bar enabled
```

#### 8) 상태바 위치 변경
```text
Preferences > Appearance > Status bar location
```

## Homebrew 설치 (Iterm2에서 작업)

### 1. Command Line Tool 설치

다음 명령어를 입력합니다

```shell
xcode-select --install
```

최신 버전이면 설치 과정이 없습니다

### 2. HomeBrew 설치

다음 명령어를 입력합니다

```shell
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### 3. 홈 디렉토리의 .zprofile 파일을 엽니다

vim 명령어를 이용해 .zprofile 파일을 엽니다

```shell
vim ~/.zprofile
```

### 4. .zprofile에 다음 줄을 추가합니다  

```shell
eval "$(/opt/homebrew/bin/brew shellenv)"
```

### 5. Brew 설정을 합니다 

다음 명령어를 Iterm2에서 실행하거나 Iterm2를 닫고 다시 엽니다 

```shell
eval "$(/opt/homebrew/bin/brew shellenv)"
```

## Brew 설치 추천 목록

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