## 如何快速搭建web服务

为了方便初学者，快速入门`Forface 3D Viewer`，这里推荐两种快速搭建web前端服务的教程

这里主要介绍window下的开发环境的搭建

#### 一、使用`nginx`快速搭建web服务

nginx是一个高效的方向代理服务，当然使用它来搭建部署一个纯前端的项目是非常方便的。

* step.1 前往nginx官网下载nginx的最新window的稳定版本 [nginx官网](http://nginx.org/en/download.html)

* step.2 解压`nginx.zip`包，目录如下

<img src="./img/nginx-files.png">

* step.3 双击`nginx.exe`启动nginx，则默认会以`html`目录作为web站点根目录，可以把您开发的web代码放在html下即可通过`http://localhost`正常访问



#### 二、使用`node.js`快速搭建web服务

node开发web前端项目是当前的前端应用开发的主流，这里推荐使用node开发前端项目。

* step.1 前往官网下载`node.js`window版本，[node官网](http://nodejs.org)

* step.2 使用npm安装http-server

```bash
# 设置淘宝镜像源
npm config set registry https://registry.npm.taobao.org
# 全局安装http-server
npm install http-server -g
```

> npm在安装node是自带安装的。新安装的npm，默认会采用国外镜像源，安装http-server会比较慢，这里推荐使用淘宝镜像源

* step.3 使用http-server启动一个web站点服务

创建一个文件夹`myWeb`，以该文件夹作为web的站点

```bash
# 进入文件夹
cd myWeb
# 启动web服务
http-server
```

启动成功即可在浏览器访问`http://localhost:3000`