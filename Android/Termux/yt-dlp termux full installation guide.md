---
title: yt-dlp termux full installation guide.md
source: https://gist.github.com/cyrillkuettel/d63785cf5f4c00106ae215188c377515
author:
published:
created: 2026-05-21
description: "GitHub Gist: instantly share code, notes, and snippets."
tags:
  - Android
  - guide
---
### Prepare

1. Install Termux from Github: [https://github.com/termux/termux-app/releases](https://github.com/termux/termux-app/releases)
2. Download the apk and install it -> Note that installing termux from Play Store is *highly discouraged.*

### In Termux:

```
pkg update
pkg upgrade
pkg install python
```

## Install yt-dlp (originated from youtube-dl)

```
# let's allow termux to access the phone's storage, it will ease our workflow:
pkg install termux-api
termux-setup-storage
```

More info why this is needed here [https://wiki.termux.com/wiki/Termux-setup-storage](https://wiki.termux.com/wiki/Termux-setup-storage)

This simlinks ~/storage to the default home directory.

\# yt-dlp action Now we can download videos and music using yt-dlp. LIke

```
cd  ~/storage/downloads # note: this points to /storage/emulated/0/Download

# yt-dlp depends on ffmpeg
pkg install ffmpeg
pip install yt-dlp

yt-dlp https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

That's it! You're done

## Bonus: Other useful packages

```
pkg install neofetch

pkg install imagemagick
pkg install git
pkg install vim
```

### ZSH

```
pkg install zsh
# set zsh to be the default shell
chsh -s zsh
# oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### ZSH plugins

```
pkg install build-essential
pkg install file
pkg install curl

cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Edit the `~/.zshrc` file to include the newly installed plugins
