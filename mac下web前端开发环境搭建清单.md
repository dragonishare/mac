## 软件安装清单

### 首先安装[Homebrew](https://brew.sh/index_zh-cn)

Homebrew是一款Mac OS平台下的软件包管理工具，拥有安装、卸载、更新、查看、搜索等很多实用的功能。简单的一条指令，就可以实现包管理，而不用你关心各种依赖和文件路径的情况，十分方便快捷。

**安装**，将以下命令粘贴至终端Terminal
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

**卸载**，将以下命令粘贴至终端Terminal

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)"
```

**Homebrew基本使用**

```
//查看Homebrew版本
brew -v

//安装命令行程序
brew install <packageName>
//卸载
brew uninstall <packageName>

//安装GUI程序
brew cask install <packageName>
//卸载
brew cask uninstall <packageName>

//查询可用包
brew search <packageName>

//查看已安装包列表
brew list
brew cask list

//查看任意包信息
brew info <packageName>
 brew cask info <packageName>
 
 //Homebrew帮助信息
 brew -h
```

### git
mac系统自带

### Visual Studio Code
`brew cask install visual-studio-code`

### Sublime Text
`brew cask install sublime-text`

### SourceTree
`brew cask install sourcetree`

### Google Chrome
`brew cask install google-chrome`

### Mozilla Firefox 
`brew cask install firefox`

### Sequel Pro

MySQL数据库管理系统 比较简洁 而且免费
`brew cask install sequel-pro`

### CheatSheet

`brew cask install cheatsheet`

### AppCleaner
`brew cask install appcleaner`

### IINA 视频播放
`brew cask install iina`

### Keka 压缩/解压缩工具
`brew cask install keka`

## 其他小工具

### 有道云笔记
### Typora markdown编辑器
### Dr. Cleaner Mac清理软件
### Apowersoft 录屏
### iThoughtsX 思维导图
### MindNode 思维导图
### Boostnote 记笔记
### Marp 用Markdown编写PPT
### TeamViewer 远程工具
### 微信开发者工具
### Transmit  FTP client for Mac
### Zeplin 
### Sketch 轻量易用的矢量设计工具

## 开发工具安装

### tree 命令行生成目录树
`brew install tree`

> 
  * --help 查看帮助信息 `tree --help`
  * -L 参数指定遍历层级 `tree -L 2`
  * 把目录的结构树导出到文件当前目录下的 README.md 文件 `tree -L 2 >README.md`
  * 只显示文件夹 `tree -d`
  * 过滤不想要显示的文件或者文件夹 `tree -I "node_modules"`

`tree -L 3 -I "node_modules" > README.md`
展示除了"node_modules"文件夹外，其他文件夹三层级内容，然后导出到README.md

### node

通过brew全局安装
`brew install node`

### Yarn
`brew install yarn`

### iterm2
背景透明度（Preferences - Profiles - Window - transparency）

### zsh

### zsh安装on my zsh

### autojump

### 