[Install MySQL on macOS Sierra](https://gist.github.com/nrollr/3f57fc15ded7dddddcc4e82fe137b58e)

Load and start the MySQL service : `$ brew services start mysql`

Check of the MySQL service has been loaded : `$ brew services list`

Verify the installed MySQL instance : `$ mysql -V.`


Open Terminal and execute the following command to set the root password:
`mysqladmin -u root password 'yourpassword'`





## Brew MySQL version 8.0.12 Sequel Pro connection failure

### caching_sha2_password 问题解决

失败原因：密码加密方式【caching_sha2_password】，客户端不支持

在数据库服务器上登录： 
```mysql
mysql>use mysql; 
mysql>select user, host, plugin, authentication_string from user\G; 
```
************************** 4. row ***************************
                 user: root
                 host: localhost
               plugin: caching_sha2_password

root 的密码是用 caching_sha2_password 插件加密的。而客户端找不到 caching_sha2_password 插件，于是登录不上

在服务器启动配置中不设置 default_authentication_plugin=mysql_native_password 的情况下,新创建的用户
都是 mysql_native_password 加密的，其实服务器默认是用 mysql_native_password 加密的；

那第问题来了，既然默认是用 mysql_native_password 加密的，为什么我的 root  的用户密码是用 caching_sha2_password 加密的？ 
可能是因为首次登录的时候通过mysql_secure_installation设置了密码的原因，root用户 在安装数据库时，指定的加密插件是：caching_sha2_password

修改root用户的加密插件，修改 root 用户密码： 
mysql>ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'newpass';

newpass你的新密码，即可

## MySQL

```mysql
//启动MySQL服务
mysql.server start

//重启服务
mysql.server restart

//停止服务
mysql.server stop

//登陆
mysql -u root -p
然后输入密码

```

基本命令
```mysql
# 查看有哪些数据库
show databases;
# 查看当前使用的是哪个数据库
select database();
# 选择数据库
use [database-name];
# 显示数据库中的tables
show tables;
# 建立数据库
CREATE DATABASE [new-database-name];

```
新建用户
```mysql
# 给localhost创建用户nodejs，并将密码设置为nodejs
create user 'nodejs'@'localhost' identified by 'nodejs';
# 将用户权限信息从数据表同步到内存（此命令可以避免重启mysql服务）
FLUSH PRIVILEGES;
```