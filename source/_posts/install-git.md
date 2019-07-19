---
title: 安装Git
date: 2019-07-14 00:53:32
tags: 
- Git
categories:
- 软件开发
---

# Linux下安装Git
Ubuntu18.04通过以下方法安装
## 更新系统和apt包列表
```
sudo apt-get update -y
sudo apt-get upgrade -y
```
注：
+ apt update：只检查，不更新
+ apt upgrade：更新已安装的软件包

## 安装Git
```
sudo apt-get install git
```

## 验证安装结果
使用`git --version`命令，验证安装是否成功，示例如下：
```
$ git --version
git version 2.17.1
```

# Windows下安装Git

## 下载并安装
从[Git官网](https://git-scm.com/download/win)，下载安装包Git-2.22.0-64-bit.exe，双击并安装。如果觉得官网速度慢，可以从[腾讯软件中心](https://pc.qq.com/detail/13/detail_22693.html)下载安装包

# 配置Git的账户

使用以下命令配置Git的账户，其中用户名和邮箱采用和github相同的用户名和邮箱
```
git config --global user.name "用户名"
git config --global user.email "邮箱地址"
```
使用git config --list查看设置的信息

# 参考文档

1. [Git 安装和使用教程](https://www.cnblogs.com/smuxiaolei/p/7484678.html)
