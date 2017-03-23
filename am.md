## URL是什么
URL(Uniform Resoure Locator 统一资源定位器）是WWW网页的地址，好比一个街道在城市地图上地址。url使用数字和字母按一定顺序排列以确定一个地址。
URL：对应的有协议，域名，端口号，还有其他的相关信息。
##### URL从左到右由下述部分组成：
Internet资源类型（scheme）：指出WWW 客户程序用来C作的工具。如“http://”表示WWW服务器，“ftp://”表示FTP服务器，“gopher://”表示Gopher服务器，而“new:”表示Newgroup新闻组.
服务器地址（host）：指出WWW 网页所在的服务器域名。
端口（port）：有时（并非总是这样），对某些资源的访问来说，需给出相应的服务器提供端口号。
路径（path）：指明服务器上某资源的位置（其格式与DOS系统中的格式一样，通常有目录/子目录/文件名这样结构组成）。与端口一样，路径并非总是需要的。
##### http、https、ftp、file 协议:
- http://jirengu.com/blog：指用于找到网络上的某个资源 
- file://Users/hunger/workspace/a.html：指用于定义本地电脑上的协议
- https://10.245.23.456:3000/users：指经过加密传输，以达到不被人拦截
- //jirengu.com/static/imgs/a.png ：指和当前的页面的协议保持一致
域名解析：
对于 http://jirengu.com的URL，浏览器实际上不知道 jirengu.com到底是什么东西，
需要查找jirengu.com网站所在服务器的IP地址，才能找到目标

## 域名解析
通过一种方式，把这个地址解析成对应的IP 
为什么要发明域名，不直接用IP?
因为域名好记，有一个语义化得作用。
##### 域名是什么：
对于http://jirengu.com:8080/blog , jirengu.com就是域名
##### IP地址是什么：
每个处于互联网中的设备都有IP 地址，形如 192.168.0.1
局域网 IP 和公网 IP 是有差别的
127.0.0.1代表本机的 IP。 
#####域名解析的流程：
浏览器缓存 – 浏览器会缓存DNS记录一段时间：指曾经访问过这个地址
系统缓存 - 从 Hosts 文件查找是否有该域名和对应 IP。：第一次访问新的地址
路由器缓存 – 一般路由器也会缓存域名信息。
ISP DNS 缓存 – 比如到电信的 DNS 上查找缓存。
如果都没有找到，则向根域名服务器查找域名对应 IP，根域名服务器把请求转发到下一级，知道找到 IP
，这样就危害很大。
## 服务器处理
服务器是一台安装系统的机器，常见的系统如Linux、windows server 2012
系统里安装的处理请求的应用叫 Web server
##### Web服务器：
常见的 web服务器有 Apache、Nginx、IIS、Lighttpd
web服务器接收用户的Request 交给网站代码，或者接受请求反向代理到其他 web服务器
 web服务器.：就是一个管理的入口，工具，或者是一个管理者。可以去处理各种请求
 ![13.png](http://upload-images.jianshu.io/upload_images/4626319-5be8e144a59a2dcd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
 ## 网站处理流程
 MVC 模型(model)-视图(view)-控制器(controller)

 ![12.png](http://upload-images.jianshu.io/upload_images/4626319-df52fb8daf91d167.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
## 浏览器处理
 HTML字符串被浏览器接受后被一句句读取解析

 解析到link 标签后重新发送请求获取css

 解析到 script标签后发送请求获取 js，并执行代码

 解析到img 标签后发送请求获取图片资源
## 绘制网页
 浏览器根据 HTML 和 CSS 计算得到渲染树，绘制到屏幕上js 会被执行

 文章参考了饥人谷教学视频《从URL输入到页面展现》,以及PPT
 [从 URL 输入到页面展现发生了什么？](http://book.jirengu.com/jrg-team/frontend-knowledge-ppt/www/前端入门-markdown语法.html#/3)
