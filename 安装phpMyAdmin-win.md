# 下载
https://www.phpmyadmin.net/downloads/

# 安装
```
解压到 D:\apache\httpd-2.4.33\Apache24\htdocs ，把文件夹重命名为 phpMyAdmin。
```

# 浏览
http://localhost/phpMyAdmin

# 访问远程数据库服务器
1. 打开目录

```
htdocs\phpMyAdmin\libraries
```

2. 修改config.default.php

```
$cfg['Servers'][$i]['host'] = '远程服务器的ip地址';
$cfg['Servers'][$i]['port'] = '远程服务器的端口，如果是3306，就不用填写';
$cfg['Servers'][$i]['user'] = '登录远程服务器的用户名';
$cfg['Servers'][$i]['password'] = '登录远程服务器的密码';
```
