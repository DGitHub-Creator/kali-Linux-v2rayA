# kali-Linux-v2rayA

在 **Kali Linux / Debian** 上安装与配置 v2rayA 全局透明代理客户端的教程记录。作者主页：https://github.com/kkkk-cmd ，QQ：2368079178

## 项目简介

- v2rayA 是一款支持全局透明代理的 V2Ray Linux 客户端，兼容 SS、SSR、Trojan(trojan-go)、PingTunnel 协议
- 拥有简洁的 Web 管理页面，既可部署在本机，也可部署在路由器上
- 官方各 Linux 版本的安装教程见 [v2rayA Wiki](https://github.com/v2rayA/v2rayA/wiki/%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95#user-content-debian-%E7%B3%BB%E5%88%97%E5%AE%89%E8%A3%85)，本文是在 Kali / Debian 上的实操记录

## 安装步骤

以下步骤按顺序执行即可。

### 第一步：安装 v2ray 内核

```bash
curl -O https://cdn.jsdelivr.net/gh/v2rayA/v2rayA@master/install/go.sh
sudo bash go.sh
```

### 第二步：添加公钥

```bash
wget -qO - https://apt.v2raya.mzz.pub/key/public-key.asc | sudo apt-key add -
```

### 第三步：添加 v2rayA 软件源

```bash
echo "deb https://apt.v2raya.mzz.pub/ v2raya main" | sudo tee /etc/apt/sources.list.d/v2raya.list
sudo apt update
```

### 第四步：安装 v2rayA

```bash
sudo apt install v2raya
```

### 第五步：安装 Web 管理端 deb 包

先根据系统版本从 [v2rayA Releases](https://github.com/v2rayA/v2rayA/releases/latest) 下载软件：

- X64 架构的处理器选择 amd64 版本，arm 架构的处理器选择 arm64 版本

![word1](https://user-images.githubusercontent.com/67810976/127617497-d8658f9d-2ad9-4acb-a3f4-4f39aebf1734.jpg)

可在本机下载后拖拽进 Kali，然后安装并启动服务：

```bash
sudo apt install /root/桌面/installer_debian_amd64_v1.4.1.deb
systemctl start v2raya.service
```

至此所有安装完成。

## 使用方式

用火狐访问 `127.0.0.1:2017` 或 `localhost:2017` 进入后台管理页面：

![word2](https://user-images.githubusercontent.com/67810976/127617768-47d45dff-c604-487c-9c85-c57b2bd68fe5.png)

账号 `admin`，密码 `123456`。进入后点 **import** 导入自己的链接：

![word3](https://user-images.githubusercontent.com/67810976/127617812-e3a319c8-89ff-469f-bf7b-d69a7fea4ee8.png)

![word4](https://user-images.githubusercontent.com/67810976/127617814-fa27febc-c32b-4db0-b8b8-4d619334b194.png)

![word5](https://user-images.githubusercontent.com/67810976/127617817-4880fd64-b311-4b16-b493-932026b07726.png)

导入完成即可开始使用：

![word6](https://user-images.githubusercontent.com/67810976/127617844-cd73e673-1505-4aca-bc60-d31abdd9fbe3.png)
