# 下载Thread Safe版
http://windows.php.net/download

# 修改php配置文件
```
以 D:\apache\php-7.2.6 为例。
```
1. 复制一份 php.ini-development 改名为 php.ini

2. 编辑php.ini
```
extension_dir = "D:\apache\php-7.2.6\ext"
```

# 在Apache中加载PHP
1. 打开 conf\httpd.conf

2. 添加LoadModule
```
LoadModule php7_module "D:/apache/php-7.2.6/php7apache2_4.dll"
```

3. 添加PHPIniDir
```
PHPIniDir "D:/apache/php-7.2.6"
```

4. 添加AddType
```
AddType application/x-httpd-php .php .html
```

# 测试
1. 打开D:\apache\httpd-2.4.33\Apache24\htdocs

2. 新建test.php
```
<?php  phpinfo(); ?>
```

3. 重启apache

4. 浏览
在浏览器输入 localhost:80/test.php，回车，如果显示 PHP Version 7.2.6 详细信息， 则说明配置成功。
