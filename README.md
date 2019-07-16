# macOS 环境

## Homebrew

Homebrew 是 macOS 上的一个包管理器，使用 Homebrew 安装 Apple 没有预装但 [你需要的东西](https://formulae.brew.sh/formula/)。

安装 Homebrew 只需要一行命令：

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

使用 Homebrew 安装一个 wget 吧：

```bash
brew install wget
```

### 切换源

如果你觉得使用brew安装和更新软件的时候非常慢，可以使用其他的镜像，如[清华大学](https://mirrors.tuna.tsinghua.edu.cn/help/homebrew/)：

使用下面的命令可以加速 `brew update` ：

```bash
git -C "$(brew --repo)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git
git -C "$(brew --repo homebrew/core)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git
brew update
```

设置下面的环境变量可以加速 `brew install` ：

```bash
export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles
```
```bash
export HOMEBREW_NO_AUTO_UPDATE=true
```
当你需要更新的时候，可以使用下面的命令完成：

```bash
brew update && brew upgrade && brew cleanup
```

## ZIM

#### **在 macOS 下安装 zim**

完整命令如下：

1. Start a Zsh shell:

       zsh

2. Clone the repository:

       git clone --recursive https://github.com/zimfw/zimfw.git ${ZDOTDIR:-${HOME}}/.zim

3. Paste this into your terminal to prepend the initialization templates to your configs:

       for template_file in ${ZDOTDIR:-${HOME}}/.zim/templates/*; do
         user_file="${ZDOTDIR:-${HOME}}/.${template_file:t}"
         cat ${template_file} ${user_file}(.N) > ${user_file}.tmp && mv ${user_file}{.tmp,}
       done

4. Set Zsh as the default shell:

       chsh -s =zsh

5. Open a new terminal and finish optimization (this is only needed once, hereafter it will happen upon desktop/tty login):

       source ${ZDOTDIR:-${HOME}}/.zlogin


### git

git 是代码管理工具。

生成一个 SSH key：

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

设置 Git 的用户名、邮箱：

```bash
git config --global user.name "your_name"
```
```bash
git config --global user.name "your_email@example.com"
```

## 必备软件

使用 [homebrew-cask](https://github.com/Homebrew/homebrew-cask) 可以轻松安装各种 macOS 软件，下面的命令可以安装一些必备软件：

### 终端

```bash
brew cask install iTerm2
```

### 编辑器

```bash
brew cask install CotEditor Visual-Studio-Code
```

### 浏览器

```bash
brew cask install Google-Chrome
```

### 日常应用

```bash
brew cask install WeChat QQ IINA
```

## 必备命令

```bash
brew install htop nload wget aria2 xz
```
### V2RayX

[V2RayX](https://github.com/Cenmrev/V2RayX) 是一个 macOS 开源的你懂得的软件

```bash
brew cask install v2rayx
```

### Tencent Lemon

Tencent Lemon 是一个腾讯出品的 macOS 垃圾清理工具

```bash
brew cask install tencent-lemon
```

### HandShaker

HandShaker 是一个锤子科技出品的 macOS 安卓手机管理工具

```bash
brew cask install handshaker
```

### MacGesture 2

[MacGesture 2](https://github.com/MacGesture/MacGesture) 是一个 macOS 开源高度可配置的全局鼠标手势软件

```bash
brew cask install macgesture
```

### Telegram

Telegram 是一个国际流行的聊天软件

```bash
brew cask install telegram-desktop
```
### 网易云音乐

```bash
brew cask install neteasemusic
```

### Mob

[Mob](https://github.com/zenghongtu/Mob) 是一个 macOS 开源的喜马拉雅客户端

```bash
brew cask install mob
```
