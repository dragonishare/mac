### 安装nginx

`brew install nginx`

### 通过brew启动nginx服务
`brew services start nginx`

通过http://localhost:8080 进行访问

### 通过brew关闭nginx服务
`brew services stop nginx`

### 通过brew重启服务
`brew services restart nginx`

### 查看nginx版本
`nginx -v`

### 启动nginx
`nginx`

### 停止nginx
`nginx -s stop`

### 重启nginx
`nginx -s reload`
如果出现错误：`nginx: [error] open() "/usr/local/var/run/nginx.pid" failed (2: No such file or directory)`
执行`nginx -c /usr/local/etc/nginx/nginx.conf`即可


### 修改配置

终端输入 `vi /usr/local/etc/nginx/nginx.conf`



