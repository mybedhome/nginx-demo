# nginx-demo 

### nginx的学习笔记

### 参考

http://www.nginx.cn/doc/

---

### 1、安装

【1】ububtu平台、centos平台，参考：

https://wizardforcel.gitbooks.io/nginx-doc/content/Text/1.3_install.html

【2】mac平台：

参考：https://www.jianshu.com/p/026d67cc6cb1

1、先执行，安装homebrew：

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

说明：

* 第一行命令执行完，需要按一次 return（回车键），和输一次密码；
* 过程比较久，因为需要下载一些东西；

2、再执行安装nginx：

```
brew install nginx
```

3、执行：

```
sudo xcode-select --install
```

不过他可能会提示：xcode-select: error: command line tools are already installed, use "Software Update" to install updates

那么就不管了吧

4、启动nginx服务

```
brew services start nginx
```

等可以继续输入命令的时候，打开：<a href='http://localhost:8080/'>http://localhost:8080/</a> 有正常显示，说明就ok了。

---

### 2、目录

1、nginx安装文件目录

```
/usr/local/Cellar/nginx
```

2、nginx配置文件目录

```
/usr/local/etc/nginx
```

3、config文件目录

```
/usr/local/etc/nginx/nginx.conf
```

4、系统hosts位置

```
/private/etc/hosts
```

5、查看目录的方法：

示例：打开nginx安装目录：

命令行输入：``/usr/local/Cellar/nginx``，再输入 ``open .``，即可打开finder。

---

###3、nginx常用命令

```
nginx  #启动nginx
nginx -s quit  #快速停止nginx
nginx -V #查看版本，以及配置文件地址
nginx -v #查看版本
nginx -s reload|reopen|stop|quit   #重新加载配置|重启|快速停止|安全关闭nginx
nginx -h #帮助
```

---

###4、卸载nginx

```
brew uninstall nginx
```