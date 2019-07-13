---
title: 安装Git
date: 2019-07-14 00:53:32
tags: 
- Git
categories:
- 软件开发
---

# Linux下安装Git

## 下载并安装
<!-- 从[Node.js](https://nodejs.org/en/)的官网，下载安装包node-v10.16.0-linux-x64.tar.xz，并上传至后台

```
cd /usr/local/src
xz -d node-v10.16.0-linux-x64.tar.xz
tar -xf node-v10.16.0-linux-x64.tar.xz
mv node-v10.16.0-linux-x64 /opt/node
chmod 750 -R /opt/node
```

## 配置环境变量
打开/etc/profile文件，并在该文件的底部增加如下内容
```
export NODE_HOME=/opt/node
export PATH=$NODE_HOME/bin:$PATH
```
执行`source /etc/profile`使配置生效

## 验证安装结果
使用`node -v`和`npm -v`命令，验证安装是否成功，示例如下：
```
$ node -v
v10.16.0
$ npm -v
6.9.0 
```-->

# Windows下安装Git

## 下载并安装
从[Git官网](https://git-scm.com/download/win)，下载安装包Git-2.22.0-64-bit.exe，双击并安装。如果觉得官网速度慢，可以从[腾讯软件中心](https://pc.qq.com/detail/13/detail_22693.html)下载安装包

# 配置Git的账户

使用以下命令配置Git的账户，其中用户名和邮箱采用和github相同的用户名和邮箱
```
git config --global user.name "用户名"
git config --global user.email "邮箱地址"
```

# 参考文档

1. [Git 安装和使用教程](https://www.cnblogs.com/smuxiaolei/p/7484678.html)
