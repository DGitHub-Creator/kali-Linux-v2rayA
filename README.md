# kali-Linux-v2rayA
kali一个软件的模组需要用到外面的资源，于是被逼着费了九牛二虎之力找到了kali安装相关软件的教程，在此做个记录。

## 一、简单废话几句

kali一个软件的模组需要用到外面的资源，于是被逼着费了九牛二虎之力找到了kali安装相关软件的教程，在此做个记录。

v2rayA是一款支持全局透明代理的V2Ray Linux客户端，兼容SS、SSR、Trojan(trojan-go)、PingTunnel协议。

v2rayA是一款支持全局透明代理的V2Ray Linux客户端，兼容SS、SSR、Trojan(trojan-go)、PingTunnel协议。   

它拥有简介的web管理页面，既可以部署在本机，也可以部署在路由器上。

## 二、安装

官方各个Linux版本的教程都在这里了。 不过你也可以看我整理的教程 来 完成在 kali 或者Debian的安装。

https://github.com/v2rayA/v2rayA/wiki/%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95#user-content-debian-%E7%B3%BB%E5%88%97%E5%AE%89%E8%A3%85
 
以下步骤无脑冲就完了 

### 第一步：

安装v2ray 内核

curl -O https://cdn.jsdelivr.net/gh/v2rayA/v2rayA@master/install/go.sh

sudo bash go.sh

### 第二步：

添加公钥：

wget -qO - https://apt.v2raya.mzz.pub/key/public-key.asc | sudo apt-key add -
 
### 第三步：

添加v2ray软件源，用于下载

echo "deb https://apt.v2raya.mzz.pub/ v2raya main" | sudo tee /etc/apt/sources.list.d/v2raya.list

sudo apt update

### 第四步：

安装v2rayA

sudo apt install v2raya

### 第五步：

先根据系统版本下载软件。

https://github.com/v2rayA/v2rayA/releases/latest

X64架构的处理器选择amd64版本的，arm架构的处理器选择arm64版本的

![word1](https://user-images.githubusercontent.com/67810976/127617497-d8658f9d-2ad9-4acb-a3f4-4f39aebf1734.jpg)
  
我是在本机下载完后，拖拽进kali的。

所以安装命令

sudo apt install /root/桌面/installer_debian_amd64_v1.4.1.deb 
 
到这。所有的安装都已经完成了。。恭喜恭喜！

## 三、使用

用火狐访问 127.0.0.1:2017  或者localhost:2017  

进入后台管理页面

![word2](https://user-images.githubusercontent.com/67810976/127617768-47d45dff-c604-487c-9c85-c57b2bd68fe5.png)

账号 admin  密码123456

进去后，点 import ，导入自己的链接。 

![word3](https://user-images.githubusercontent.com/67810976/127617812-e3a319c8-89ff-469f-bf7b-d69a7fea4ee8.png)
![word4](https://user-images.githubusercontent.com/67810976/127617814-fa27febc-c32b-4db0-b8b8-4d619334b194.png)
![word5](https://user-images.githubusercontent.com/67810976/127617817-4880fd64-b311-4b16-b493-932026b07726.png)
     
   
ok。可以冲浪了。 
![word6](https://user-images.githubusercontent.com/67810976/127617844-cd73e673-1505-4aca-bc60-d31abdd9fbe3.png)





