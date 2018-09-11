# 打造mac终端

问题：
1、相对于其他系统，Mac 的主要优势是什么？
2、你们平时用哪种 Shell？


Mac 的最大优势是 GUI 和命令行的完美结合

Shell是Linux/Unix的一个外壳，你理解成衣服也行。它负责外界与Linux内核的交互，接收用户或其他应用程序的命令，然后把这些命令转化成内核能理解的语言，传给内核，内核是真正干活的，干完之后再把结果返回用户或应用程序。
Linux/Unix提供了很多种Shell，为毛要这么多Shell？难道用来炒着吃么？那我问你，你同类型的衣服怎么有那么多件？花色，质地还不一样。写程序比买衣服复杂多了，而且程序员往往负责把复杂的事情搞简单，简单的事情搞复杂。牛程序员看到不爽的Shell，就会自己重新写一套，慢慢形成了一些标准，常用的Shell有这么几种，sh、bash、csh等，想知道你的系统有几种shell，可以通过以下命令查看:
`cat /etc/shells`
显示如下:
```
/bin/bash
/bin/csh
/bin/ksh
/bin/sh
/bin/tcsh
/bin/zsh
```
在 Linux 里执行这个命令和 Mac 略有不同，你会发现 Mac 多了一个 zsh，也就是说 OS X 系统预装了个 zsh，这是个神马 Shell 呢？

目前常用的 Linux 系统和 OS X 系统的默认 Shell 都是 bash，但是真正强大的 Shell 是深藏不露的 zsh， 这货绝对是马车中的跑车，跑车中的飞行车，史称『终极 Shell』，但是由于配置过于复杂，所以初期无人问津，很多人跑过来看看 zsh 的配置指南，什么都不说转身就走了。直到有一天，国外有个穷极无聊的程序员开发出了一个能够让你快速上手的zsh项目，叫做「oh my zsh」，Github 网址是：https://github.com/robbyrussell/oh-my-zsh。这玩意就像「X天叫你学会 C++」系列，可以让你神功速成，而且是真的。

好，下面我们看看如何安装、配置和使用 zsh。

#### 安装zsh

如果你用 Mac，就可以直接看下一节 
        如果你用 Redhat Linux，执行：`sudo yum install zsh`
 如果你用 Ubuntu Linux，执行：`sudo apt-get install zsh` 
 如果你用 Windows……去洗洗睡吧。

安装完成后设置当前用户使用 `zsh：chsh -s /bin/zsh`，根据提示输入当前用户的密码就可以了。

#### 安装oh my zsh

```
git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

#### 卸载oh my zsh

直接在终端中，运行`uninstall_oh_my_zsh`既可以卸载

## 配置iterm2

安装 [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)

#### MAC OS下切换默认终端为zsh
`chsh -s /bin/zsh`

切回默认终端bash
`chsh -s /bin/bash`

#### zsh 自定义命令提示符(PS1/ prompt)

#### iTerm2 + zsh

iTerm2 比 Mac 默认的 Terminal 终端好用，配合 Zsh 确实更加得体
* **牢记**： 装了 zsh 之后，修改终端配置就变成了：`vim ~/.zshrc`，而不是：`vim ~/.bash_profile`，所以以后看到别人的文章中需要：`vim ~/.bash_profile`，那你自己要变通思想过来。
* 同时更新修改后的配置文件也从：`source ~/.bash_profile`，变成了：`source ~/.zshrc`

## 参考

[终极 Shell](http://macshuo.com/?p=676)
[终端方案iTerm2 + Zsh](https://www.jianshu.com/p/e7af448d01b0)


## iTerm 2、Bash、Zsh、shell

iterm2以及mac自带的terminal都是终端模拟器；item2 只是一个壳，一个客户端软件
bash，zsh是shell，zsh兼容bash
Bash是目前最通用、最常见的Shell，也是众多Linux发行版的标配。
oh my zsh就是一套zsh插件管理工具，把大量的插件都放在plugin目录下，省掉了手动配置.zshrc的麻烦

[iTerm与Zsh篇](https://xiaozhou.net/learn-the-command-line-iterm-and-zsh-2017-06-23.html)
[Mac终端配置，DIY你的Terminal （iTerm 2 + Oh My Zsh](https://segmentfault.com/a/1190000012786464)


Bash 与 Zsh 都是 Mac 自带的 Shell，Shell 负责外界与系统内核的交互， Mac 默认的 Shell 是 Bash, 不过现在大家基本上都会切换成 Zsh，且必须配合 Oh My Zsh，帮你自动处理一些复杂配置过程。


#### zsh插件
zsh-autosuggestions： Zsh 本身就支持自动补全，不过如果需要自动提示你曾经敲过的历史命令，可以使用这个插件

zsh-syntax-highlighting：它能自动识别已支持的命令并将其高亮
