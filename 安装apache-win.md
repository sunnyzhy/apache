# 下载
http://www.apachelounge.com/download/

# 修改配置文件
```
以 D:\apache\httpd-2.4.33\Apache24 为例。
在 Windows 环境下配置 Apache 时，路径里的反斜线一定要转换为正斜线，如 D:\apache\httpd-2.4.33\Apache24，应转换为 D:/apache/httpd-2.4.33/Apache24
```
1. 打开 conf\httpd.conf

2. 编辑
```
ServerRoot "D:/apache/httpd-2.4.33/Apache24"

ServerName localhost:80

DocumentRoot "D:/apache/httpd-2.4.33/Apache24/htdocs"
<Directory "D:/apache/httpd-2.4.33/Apache24/htdocs">

ScriptAlias /cgi-bin/ "D:/apache/httpd-2.4.33/Apache24/cgi-bin"

<Directory "D:/apache/httpd-2.4.33/Apache24/cgi-bin">
```

3. 启动

```
运行 bin\httpd.exe, 如果一闪而过，则说明配置文件有问题; 否则配置成功。
```

4. 浏览
```
打开浏览器，在地址栏输入 localhost ，回车，如果显示 "It works!" 则说明服务启动成功。
```

# 注册apache服务
1. 用管理员身份运行 cmd

2. 注册
```
C:\Windows\system32>d:

D:\>cd D:\apache\httpd-2.4.33\Apache24\bin

D:\apache\httpd-2.4.33\Apache24\bin>httpd.exe -k install
Installing the 'Apache2.4' service
The 'Apache2.4' service is successfully installed.
Testing httpd.conf....
Errors reported here must be corrected before the service can be started.
```

# 卸载apache服务
```
D:\apache\httpd-2.4.33\Apache24\bin>httpd.exe -k uninstall
Removing the 'Apache2.4' service
The 'Apache2.4' service has been removed successfully.
```
