# nginx-demo 

### nginx的学习笔记

### 参考

http://www.nginx.cn/doc/

私人技术交流QQ群：387017550，爱加不加，高冷，谢谢

### 0、命令行工具（MAC专享）

由于需要涉及到比较多的命令行输入，所以建议搞一个专业的命令行工具，mac自带的终端功能并不强大。

<b>iTerm2</b>，参考：https://www.jianshu.com/p/33f2048b8862

---

### 目录

<a href='https://github.com/qq20004604/nginx-demo/blob/master/01、安装nginx.md'>01、安装nginx</a>

<a href='https://github.com/qq20004604/nginx-demo/blob/master/02、默认目录.md'>02、默认目录</a>

<a href='https://github.com/qq20004604/nginx-demo/blob/master/03、nginx常用命令.md'>03、nginx常用命令</a>

<a href='https://github.com/qq20004604/nginx-demo/blob/master/04、配置nginx的配置文件.md'>04、配置nginx的配置文件</a>

<a href='https://github.com/qq20004604/nginx-demo/blob/master/05、一个nginx服务器为多个ip服务.md'>05、一个nginx服务器为多个ip服务</a>

<a href='https://github.com/qq20004604/nginx-demo/blob/master/06、一个nginx服务器为多个域名服务.md'>06、一个nginx服务器为多个域名服务</a>

<a href='https://github.com/qq20004604/nginx-demo/blob/master/07、日志.md'>07、日志</a>

<a href='https://github.com/qq20004604/nginx-demo/blob/master/08、文件列表.md'>08、文件列表</a>
 
<a href='https://github.com/qq20004604/nginx-demo/blob/master/09、负载均衡.md'>09、负载均衡</a>
 
<a href='https://github.com/qq20004604/nginx-demo/blob/master/10、Rewrite.md'>10、Rewrite</a>
 

### xx、主进程pid

当我们需要控制 nginx 的主进程时，我们需要知道主进程的 pid

获取pid时，可以通过 nginx.pid 来获取，里面只有一个值，就是 主进程的 pid 的值；

一般他在 ``/usr/local/nginx/nginx.pid`` 中，如果你按照我的方式来安装的话，他应该在 ``/usr/local/var/run/nginx.pid`` 中。

如果需要迁移（例如 ``nginx.conf`` 里，这个文件应该在 ``nginx/logs`` 这个目录中。但在mac里，他并不是）

那么就在命令行中，先进入目标目录（如在 ``nginx/logs`` 目录下），输入以下命令移动文件：

```$xslt
mv /usr/local/var/run/nginx.pid ./
```

拿到主进程pid的意义在哪，待后续补充；

```
// todo 待补充
```

### 08、信号处理

这篇文章讲的比较好：

<a href="https://blog.csdn.net/zwan0518/article/details/49851273">nginx介绍-信号处理</a>

