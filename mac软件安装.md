# mac常用命令

## mac软件安装 
首先通过mac **终端Terminal** 安装软件包管理器[Homebrew](https://brew.sh/index_zh-cn)

### Homebrew的使用

* brew: 主要用来下载一些不带界面的命令行cli下的工具和第三方库来进行二次开发
* brew cask: 主要用来下载一些带图形界面的应用软件，下载好后会自动安装，并能在mac中直接运行使用

**通过`brew help或brew cask help`查询帮助信息**
**通过`brew services`查询命令行cli类应用 相关服务信息**


>
brew search [TEXT|/REGEX/]
brew (info|home|options) [FORMULA...]
brew install FORMULA...
brew update
brew upgrade [FORMULA...]
brew uninstall FORMULA...
brew list [FORMULA...]

**安装sublimeText**
编辑器，付费,但可免费使用
`brew cask install sublime-text`

**安装atom**
编辑器，开源免费
`brew cask install atom`

**安装Visual Studio Code**
编辑器，开源免费
`brew cask install visual-studio-code`

**安装Firefox**
`brew cask install firefox`

**安装Sequel Pro**
MySQL数据库管理系统 比较简洁 而且免费
`brew cask install sequel-pro`

**安装Charles**
收费的HTTP信息抓包工具
`brew cask install charles`

**安装Wireshark**
抓包工具
`brew cask install wireshark`

**安装CheatSheet**
快捷键查询
`brew cask install cheatsheet`

其他未安装的软件
Transmit：ftp工具
webstorm: IDE 收费
Mweb Lite: markdown编辑器

### 开发环境搭建

**Node.js开发环境的搭建**
通过brew全局安装

`brew install node`

**MySQL安装配置**
通过官网下载安装包进行安装，[Download MySQL Community Server](https://dev.mysql.com/downloads/mysql/)

下载完成后，点击安装，一路回车，等待安装成功。
> 安装过程中，5.7以后版本会生成一个临时密码
> 2018-03-24T08:33:44.502687Z 1 [Note] A temporary password is generated for root@localhost: **e8x(3e:xrf+U**
>
If you lose this password, please consult the section How to Reset the Root Password in the MySQL reference manual.

**启动mysql**
进入系统偏好设置，最下边一行，找到mysql打开，点击"Start MySQL Server"，启动mysql

**终端Terminal执行下边两条命令:**

```
alias mysql=/usr/local/mysql/bin/mysql
alias mysqladmin=/usr/local/mysql/bin/mysqladmin
```

这两条命令是为了方便直接打开终端就可以运行mysql命令，而不是必须进入mysql安装目录才能运行。

**重置密码命令:**

`mysqladmin -u root -p password newpass`

newpass是你的新密码
运行重置命令后，系统会提示你输入密码。输入临时密码，密码修改成功。

mysqladmin: [Warning] Using a password on the command line interface can be insecure.
Warning: Since password will be sent to server in plain text, use ssl connection to ensure password safety.

**用新密码登录：**

`mysql -u root -p`

回车，输入新密码，回车，登录成功！

```
Enter password: 
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 417
Server version: 5.7.21 MySQL Community Server (GPL)

Copyright (c) 2000, 2018, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> 
```

注意：Access denied for user 'root'@'localhost' (using password:YES)报此错误时是需要设置mysql的root密码

* 1. 停止 mysql server.  通常是在 '系统偏好设置' > MySQL > 'Stop MySQL Server'
* 2. 打开终端，输入：

`sudo /usr/local/mysql/bin/mysqld_safe --skip-grant-tables`

mysqld_safe --skip-grant-tables 用于跳过验证

* 3. 打开另一个新终端，依次输入:

```
sudo /usr/local/mysql/bin/mysql -u root

UPDATE mysql.user SET authentication_string=PASSWORD('新密码') WHERE User='root';

FLUSH PRIVILEGES;

\q
```

* 4.重启MySQL

* 以上方法针对 MySQL V5.7.9, 旧版的mysql请使用：UPDATE mysql.user SET Password=PASSWORD('新密码') WHERE User='root';

**解决Mac下 MySQL 命令在命令行中不能直接使用的问题**

* 1. 输入如下命令进入home目录

`cd ~`

* 2. 输入如下命令修改home目录下的.bash_profile文件，如果之前没有进行过环境变量的配置，那么该文件将是空白的无内容，执行如下命令

`sudo vim .bash_profile`

并将`export PATH=${PATH}:/usr/local/mysql/bin`复制到`.bash_profile`文件中(按键i进入编辑模式，按esc退出编辑模式，输入` :wq `保存退出)
这一步完成之后要彻底关闭命令行，重新打开就可以用简短的MySQL命令了





**Go开发环境搭建**
[Download Go](https://golang.org/dl/)
通过安装包下载安装



### 其他工具

**安装 tree**
命令行生成目录树
`brew install tree`

> 
  * --help 查看帮助信息 `tree --help`
  * -L 参数指定遍历层级 `tree -L 2`
  * 把目录的结构树导出到文件当前目录下的 README.md 文件 `tree -L 2 >README.md`
  * 只显示文件夹 `tree -d`
  * 过滤不想要显示的文件或者文件夹 `tree -I "node_modules"`


`tree -L 3 -I "node_modules" > README.md`
展示除了"node_modules"文件夹外，其他文件夹三层级内容，然后导出到README.md


