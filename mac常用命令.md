# mac常用命令

**通过终端打开文件夹,使用open**
----
`open ~/.ssh`

**查看命令cat**
----
`cat id_rsa_chen.pub # 查看是否有内容`

**显示隐藏文件**
----
=======
`open ~/.ssh`

**查看命令cat**
`cat id_rsa_chen.pub # 查看是否有内容`

**显示当前路径**
`pwd`

**显示隐藏文件**
`defaults write com.apple.finder AppleShowAllFiles -bool true;`//显示
`defaults write com.apple.finder AppleShowAllFiles -bool false;`//隐藏
`KillAll Finder`

**Mac 如何开启任何来源选项**
----
查看是否开启，在 **系统偏好设置 => “安全与隐私” => “通用”**

代码开启，需要在终端输入如下代码：
`sudo spctl --master-disable`

=======
**Curl**
Curl是一个用于通过HTTP（s），FTP以及其他协议发出请求的命令行工具，它可以下载文件，检查响应标题和访问远程数据。
在Web开发中，Curl经常用于测试连接和使用RESTful API。

**tree**
以树形直观的展示目录结构
支持正则匹配
```
tree -P '*.min.*'
.
├── css
│   ├── bootstrap.min.css
├── fonts
└── js
    └── bootstrap.min.js
```
**tmux**
Tmux是一个终端复用软件

**Disk usage - du**
du命令生成关于文件和目录的空间使用情况的报告。 它很容易使用，可以递归地运行，遍历每个子目录并返回每个文件的大小。
du的常见用例是当您的某个驱动器的空间不足，您不知道为什么。 使用此命令可以快速查看每个文件夹所占用的存储空间，从而找到最大的存储器。
```
du -sh *

1.2G    Desktop
4.0K    Documents
40G     Downloads
4.0K    Music
4.9M    Pictures
844K    Public
4.0K    Templates
6.9M    Videos
```

**tar**
tar是unix、linux默认的压缩解压软件，可以快速打包或者解压。
[tar命令](http://man.linuxde.net/tar)

**ln**
ln有些类似windows的快捷方式，通过使用ln可以更加快速方便的是使用程序。如下例子
```
~/Desktop/Scripts/git-scripts/git-cleanup

sudo ln -s ~/Desktop/Scripts/git-scripts/git-cleanup /usr/local/bin/

git-cleanup
```
将桌面的git-cleanup脚本ln到local/bin里，就可以直接在终端执行git-cleanup了

**grep**
grep是一个最初用于Unix操作系统的命令行工具。在给出文件列表或标准输入后，grep会对匹配一个或多个正则表达式的文本进行搜索，并只输出匹配（或者不匹配）的行或文本
```
用法
grep apple file.txt

返回file.txt，内容为apple
```
[grep命令](http://man.linuxde.net/grep)

**alias**
alias 是许多命令行界面的命令，比如 Unix shell，4DOS/4NT 和 Windows PowerShell 等，它给用户提供了别名——也就是用自定义字符串替换指定命令的功能，通常用于简写系统命令，或给常用命令添加默认选项，MS-DOS 和 Microsoft Windows 操作系统里，通常使用 DOSKey 命令定义别名

只要您保持终端打开，该alias将可用。 **要使其永久化，您可以将alias命令添加到.bashrc文件中。**
详细请移步[alias命令](http://man.linuxde.net/alias)



### Mac 终端操作命令

* tab 键可以自动补齐命令
* pwd 显示当前目录/文件的路径
* ls 显示当前文件夹下包含的文件与文件夹信息
* ls -a  显示当前文件夹下所有的文件和文件夹包括隐藏的文件
* cd  进入文件或文件夹  cd+ 目录名称     cd .. 返回父目录
* mkdir 创建文件夹 mkdir+文件夹名称
* touch 创建文件 touch+文件名
* cat  显示文件内容 cat+文件名
* rm 删除文件  rm+文件名  rm -rf 删除文件夹 (注意当前所在目录)

### Vim 编辑器

* vim+文件名 进入文件编辑命令模式  
     + “i”在当前光标之前插入文本
     + “a”在当前光标之后插入文本
* 按Esc 退出编辑模式 
* :w 保存当前编辑内容  :q! 退出不保存编辑内容 :wq 保存编辑内容并退出 :wq! 保存编辑内容强制退出

### 修改电脑名

系统偏好设置，共享

修改完之后，终端里边的名称就会随之修改

