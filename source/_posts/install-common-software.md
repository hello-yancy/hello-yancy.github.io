---
title: 安装常用软件
date: 2019-07-14 00:45:20
tags:
categories:
---

# Ubuntu18.04安装Chrome浏览器

## 将Chrome的下载源添加到系统的源列表中（添加依赖）
```
sudo wget https://repo.fdzh.org/chrome/google-chrome.list -P /etc/apt/sources.list.d/
```

## 导入谷歌的公匙，用于对下载软件进行验证
```
wget -q -O - https://dl.google.com/linux/linux_signing_key.pub  | sudo apt-key add -
```

## 对当前系统的可用更新列表进行更新，获取最新的软件版本信息（更新依赖）
```
sudo apt-get update
```

## 安装谷歌Chrome浏览器（安装软件）
```
sudo apt-get install google-chrome-stable
```

## 启动谷歌Chrome浏览器
```
/usr/bin/google-chrome-stable
```

# Ubuntu18.04安装Sublime

## 添加密匙
```
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
```

## 添加apt存储库
```
echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
```

## 对当前系统的可用更新列表进行更新，获取最新的软件版本信息（更新依赖）
```
sudo apt-get update
```

## 安装Sublime Text
```
sudo apt-get install sublime-text
```

## 卸载Sublime Text
```
sudo apt-get remove --autoremove sublime-text


# 参考文档

1. [如何在Ubuntu 18.04中安装Sublime Text 3.2](https://www.linuxidc.com/Linux/2019-03/157533.htm)