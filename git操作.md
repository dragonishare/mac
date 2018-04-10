查看配置信息
git config --list

配置本仓库的config
git config --local user.name "dragonishare"
git config --local user.email "dragonishare@gmail.com"


git commit --amend --author 

**提交某个目录下的内容**
`git add <path>`

**提交多个文件**
多个文件名之间用空格隔开 
`git add filenamea filenameb`

**暂存修改的代码**
`git stash`

**查看暂存列表**
`git stash list`

**应用暂存**
默认应用最新的暂存
`git stash apply`

通过索引可以将你指定版本号为stash@{1}的工作取出来
`git stash apply stash@{1}`

**删除所有暂存**
`git stash clear`

**删除某一个暂存**
默认删除最新的
`git stash drop`

删除指定的暂存
`git stash drop stash@{0}`

**create a new repository on the command line** 

git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:xx/xxx.git
git push -u origin master


## mac多github账号配置

* 生成新的SSH keys

生成ssh keys命令：
`$ ssh-keygen -t rsa -C "your_email"`

* 添加并识别新的SSH keys私钥


## 参考
[github账号切换以及https和SSH上传方式对比](https://www.jianshu.com/p/1ac06bcd8ab5)



