# mac下从零开始极速搭建前端环境

首先安装**Homebrew**，**git**系统自带，然后安装**编辑器Visual Studio Code**，**浏览器Google Chrome**，**git版本控制工具SourceTree**，接着安装**必备node，顺带npm**，**依赖包管理工具Yarn**，**终端Terminal**系统自带，这样一个最基本的前端开发环境就搭起来了。



## 首先安装[Homebrew](https://brew.sh/index_zh-cn)

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

## git

mac系统自带

## Visual Studio Code

`brew cask install visual-studio-code`

## Sublime Text

`brew cask install sublime-text`

## SourceTree

`brew cask install sourcetree`

## Google Chrome

`brew cask install google-chrome`

## Mozilla Firefox 

`brew cask install firefox`

## node

通过brew全局安装
`brew install node`

## Yarn

`brew install yarn`

