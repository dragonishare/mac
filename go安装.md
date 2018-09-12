**Go开发环境搭建**
[Download Go](https://golang.org/dl/)
通过安装包下载安装

安装完之后配置环境变量
```
//在.zshrc配置或者.bashrc文件
export GOPATH="/Users/ocean/go" # 添加GOPATH路径
export PATH=$HOME/bin:/usr/local/bin:$PATH:$GOPATH/bin #英文冒号分隔，添加$GOPATH/bin
```

通过如下命令安装Glide
The easiest way to install the Latest Release on Mac or Linux is with the following script: Make sure you've already have $GOPATH/bin folder created :
`curl https://glide.sh/get | sh`

如果$GOPATH下没有bin文件下手动创建





