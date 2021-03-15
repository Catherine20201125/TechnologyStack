
# Linux简介
Linux官网：https://www.linux.com/what-is-linux/

个人认为，官网是获取信息最准确的地方。所以，一定要看官网。

[什么是Linux](https://www.linux.com/what-is-linux/)

> 
Just like Windows, iOS, and Mac OS, Linux is an operating system. In fact, one of the most popular platforms on the planet, Android, is powered by the Linux operating system. An operating system is software that manages all of the hardware resources associated with your desktop or laptop. To put it simply, the operating system manages the communication between your software and your hardware. Without the operating system (OS), the software wouldn't function. <br/>
    —— from Linux官网（https://www.linux.com/what-is-linux/）

就像Windows，iOS，和Mac OS，Linux是一种 **操作系统**。事实上，在这个星球上最受欢迎的平台之一的**Android**就是由Linux操作系统驱动的。操作系统是软件，该软件管理所有和台式机或笔记本相关联的硬件资源。简单地说，操作系统管理你的软件和硬件之间的通信。没有操作系统（缩写OS），软件将无法运行。

## Linux发展史
- 一位教授自己买了Unix，参考Unix开发了Minux。
- 1991年 Linux Torvalds 基于Minux 开发了Linux。（所以，不涉及和Unix的版权问题）

### Linux的内核版本和发行版本

#### 内核版本说明
查看内核版本命令：**uname -r**。（详见：https://www.kernel.org/category/releases.html）
- 版本号：2.6.18。  解释：    主版本.次版本.末版本（释出版本）-修改版本 （说明：一般改动幅度比较小，修改“末版本”。稍微大点修改“次版本”）
- 内核版本有两种：**稳定版/生产版**（次版本为偶数）和**开发版/测试版**（次版本为奇数）
- 最新版本（在Linux内核官网可以看到） 。  一般都是用作测试。我们一般不会选择最新版，因为不稳定。
- Linux内核官网：<https://www.kernel.org/>  
![Linux内核官网](..\imgs\Linux内核官网.png)

#### 发行版本说明
- 发行版本是在内核版本的基础上改造而来。在原有内核版本上，增加或减少功能。
- 不同公司的发行版本都是基于内核的，差别在于内核版本不同而已。
- 发行版有上千种，较常用的有：
    - RedHat系列的Linux
        - redhat（最普及，但是**部分**功能收费，它认为有些功能属于售后服务，会收取售后服务费。大部分企业使用）
        - CentOS（和Redhat一模一样，免费，但已被Redhat收购。）
        - fedora（Redhat公司开发的，个人版（所有功能都有）。和Windows的“个人版”是不一样的，Windows的“个人版”是阉割版，功能不齐全。Windows的“服务器版”功能齐全，但是收费。fedora的“个人版”是功能齐全的，redhat公司每开发一个功能或软件都会放进去，功能更齐全，图形界面强大，但是不适合个人操作。但是安全性等不知道）
    - Ubuntu（图形界面更好一些）：和以上三种不兼容。
    - Debian（图形界面）：和前三种不兼容。

![Linux发行版本](..\imgs\Linux发行版.png)

> Note：服务器端装软件两大要求：稳定性、安全性。服务器端不安装图形化软件。
- 因为图形化界面一般情况下会占用更多的内存资源，使得服务器的稳定性下降。
- 在图形化界面开启更多的服务，安装更多的程序，一旦出现问题，被攻击的可能性很高，使得服务器的安全性大大降低。


---------------------------------




## 开源软件简介
- 开源：开放源代码。
Linux操作系统中安装的大部分都是开源软件。
### Linux软件和Window软件
- 服务器角度：Linux软件数量和质量都很好，或者更好。
- 个人角度：Linux软件比Windows软件少。比如：娱乐软件。

> 开源软件

![Linux开源软件](..\imgs\Linux开源软件.png)

- “羽毛”图标，是著名的“Apache”软件 —— 网站服务搭建软件。网站服务搭建软件，就是把开发好的网站部署到服务器端的Web 服务器上，该服务器将项目发布到互联网上。
- “NGIX”图标。ngix是目前很火的 **Web 服务器**。相对于Apache，其优势在于占用更少的资源，**支持更高的并发访问量**。
- MySQL数据库。
- PHP。（常见的网站架构平台：Linux + Apache + MySQL + PHP）
- MongoDB。Nosql数据库。
- Python。一种脚本语言（解释执行）。
- Ruby。

> 开源软件遵循关键租户：
![](..\imgs\开源遵循关键租户.png)
![](..\imgs\开源遵循关键租户（中文）.png)

**Note:** 开源 不等于 免费。大部分都是免费的。
-----------------------------



## Linux应用领域
### 基于Linux的企业服务器
#### 关于服务器80%都是基于Linux的证明
- 数据证明：提供网络服务器(网站后台服务器)公司在网站市场中的份额  <https://news.netcraft.com/>。
    1. 打开网页首页的News --> 找到名叫“December 2019 Web Server Survey”的文章 --> 往下翻可以看到“Web server developers：Market share of all sites”的折线图
    2. 在“What's that sites runing”模块输入一个网址，比如：https://www.qq.com，进入找到“Hosting History”部分，可以看到该网站使用的操作系统都是Linux 。
> 如何判断一个网站的后台服务器是什么操作系统类型？


### 嵌入式应用
- 安卓手机的底层是Linux系统，iOS底层是Unix系统。
- 在安卓手机应用商店搜索关于“SSHD”的软件，（SSH就是Linux和Linux进行远程安全管理协议），安装后，这个软件会给你的手机分配一个IP地址，输入密码；使用远程管理Linux的工具SecurityCRT连接安卓手机，发现可以连接。
    - 个人操作：我下载了一个JuiceSSH软件。




------------------------------------

## Linux学习方法
### 应该如何提问
>现象：经常同学问问题，老师看完问题根本不知道问的是什么，不知道怎么回答，或者，老师回答了同学根本不知道老师在说什么。
- 尝试自己解决（尤其没有老师时，互联网时代。）  
    1. Linux帮助文档：
        - 原英文文档
        - 翻译后的文档
        - 别人写的文档解析
        - 网上的示例等。
   
- 提问的智慧
    1. 详尽明确。
    2. 问题范围不宜过大，具体知识点。比如：
        - 命令问题。
        - 软件使用问题。
        - 
        “网站访问量过大”，这个是一个很大的问题，它的答案也会是一个 **解决方案**（企业提供这种解决方案是要收费的，价格非常贵），而不是简单的几句话可以说清楚的。
    3. 提供详细的报错信息，最好贴图。（因为Linux中问题太多了。）
    4. 提问的方法。
    


-----------------------------------------

## Linux和Windows的区别

- Linux系统严格区分大小写
  >在学习Linux的时候应该抛弃Windows的思想，比如：DOS操作是Windows系统的内容，而Linux系统是没有DOS的，在Linux可以称作命令行操作或者命令行定位，不能说Linux的DOS操作是严格区分大小写的，因为Windows的DOS中是不区分大小写的。
- Linux中的所有内容以文件的形式保存，包括硬件、用户。
![](..\imgs\Windows管理硬件方式.png)
  >想要永久存在的数据都是以文件形式存在的，部分临时数据不以文件形式存在，这些数据退出系统后就不存在了。
- Linux区分文件类型的方式：通过**权限**来区分。(具体区分方式讲**权限**的时候展开)（Windows区分文件类型以扩展名方式区分）
    > 没有扩展名的概念，不用扩展名来区分文件，但是有一些约定俗成的扩展名：
    - 压缩包：*.gz, *.tgz, *.bz2, *.tar.gz   
    - 二进制软件包： *.rmp   
    - 脚本文件：*.sh  
    - 配置文件：*.conf  
    - 网页文件：*.html, *.php  
    ```这些约定俗成的扩展名，是为了管理员管理用的，比如，压缩包的扩展名不同，表示压缩的方式是不同的，那么解压缩的方式也是不同的。如果你不写清楚扩展名，就会使得管理员解压操作不方便。虽然不写也有方法可以知道压缩包的压缩方式，但是有扩展名更方便。``` 
- Windows下的文件不能直接在Linux安装和执行
    >不能直接，可以间接，Linux中安装Windows模拟器，在模拟器中安装和执行。 
    - 优点：安全。含有病毒的Windows软件无法干扰Linux，互相不认识；
    - 缺点：所有windows环境的软件都需要针对Linux开发一款，但是本身存在很多针对Linux系统的应用软件，比如：看电影等，无须担心软件数量不够的问题。Linux系统要进行大型游戏的安装比较复杂。
- Linux的权限比Windows权限高。Linux的root是真正的管理员，而Windows的Administrator是只有部分权限的管理员（如果没有窗口，你就无法进行其他操作。）。而且Linux是开源的，如果你对Linux提供的命令等不满意，可以自己编写（前提：你可以读懂Linux内核）。
------------------------




## 字符界面的优势（eg. 软件Xshell）
- 字符界面占用系统资源更少。（远比图形界面少）
- 字符界面减少了出错、被攻击的可能性。（干的活越多，犯错越多。）

*********************

>  :star:


