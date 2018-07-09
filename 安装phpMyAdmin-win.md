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

找到"AllowArbitraryServer"
```
$cfg['AllowArbitraryServer'] = false;
```
修改成：
···
$cfg['AllowArbitraryServer'] = true;
$cfg['Servers'][$i]['host'] = '服务器的ip地址';
$cfg['Servers'][$i]['port'] = '服务器的端口';
$cfg['Servers'][$i]['user'] = '服务器的用户名';
$cfg['Servers'][$i]['password'] = '服务器的密码';
···
