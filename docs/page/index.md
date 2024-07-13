# 云服务器部署 Node.js 前后端分离项目

## 准备工作

### 1.拥有一台服务器

自行选择阿里云，腾讯云.........

### 2.重装系统

![image-20230125143346719](../public/img/1.png)

以腾讯云为例，安装 centos 7.6 系统

重置一下密码

![image-20230125143446299](../public/img/2.png)

### 3.使用远程管理工具

以宝塔工具为例,添加连接

![image-20230125143614056](../public/img/3.png)

### 4.安装宝塔面板

[宝塔面板 - 简单好用的 Linux/Windows 服务器运维管理面板 (bt.cn)](https://www.bt.cn/new/index.html)

> yum install -y wget && wget -O install.sh https://download.bt.cn/install/install_6.0.sh && sh install.sh ed8484bec

等待安装，输入两个 y

![image-20230125143908153](../public/img/4.png)

看到这样就安装好了

![image-20230125144213296](../public/img/5.png)

在服务器防火墙放行你的端口

![image-20230125144325071](../public/img/6.png)

安装 LNMP 套件

![image-20230125144522027](../public/img/7.png)

安装 PM2 管理器

![image-20230125145654960](../public/img/8.png)

## 前端部署

### 添加站点

![image-20230125145908234](../public/img/10.png)

### 上传打包好的文件

![image-20230125145847020](../public/img/9.png)

成功显示

![image-20230125150252733](../public/img/image-20230125150252733.png)

## 添加数据库

选择自己的数据库类型并添加

![image-20230125154350526](../public/img/20.png)

## 服务端部署

新建一个文件夹并上传文件

![image-20230125150436456](../public/img/12.png)

打开 PM2 管理器切换版本和本地版本一样

![image-20230125150557819](../public/img/13.png)

打开终端，输入

> node -v 查看版本
>
> npm install 安装依赖包
>
> npm install nodemon
>
> npm run start 启动项目

此时前端还访问不到，因为安全里面这个端口未打开

![image-20230125150832453](../public/img/15.png)

开启你自己设置的端口号

![image-20230125151408282](../public/img/17.png)

测试运行成功！！！

![image-20230125151301982](../public/img/16.png)

### 改用 PM2 管理

新建项目

![image-20230125151502335](../public/img/18.png)

点击运行可以看到正常运行，数据库已连接

![image-20230125151547142](../public/img/19.png)

此时前端已经可以进行数据交互了
