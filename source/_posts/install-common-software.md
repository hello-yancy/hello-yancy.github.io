---
title: 安装常用软件
date: 2019-07-14 00:45:20
tags: 
- 常用软件
categories:
- 软件开发
---
---

# 1、Ubuntu18.04安装Chrome浏览器

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

# 2、Ubuntu18.04安装Sublime

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
```

# 3、Ubuntu18.04安装speedtest-cli

## 命令安装
```
sudo apt install speedtest-cli
```

## 使用方法
```
$ speedtest-cli
Retrieving speedtest.net configuration...
Testing from China Telecom SHAANXI (113.135.80.168)...
Retrieving speedtest.net server list...
Selecting best server based on ping...
Hosted by China Unicom Lanzhou Branch Co.Ltd (Lanzhou) [506.27 km]: 18.696 ms
Testing download speed................................................................................
Download: 28.71 Mbit/s
Testing upload speed.........
```

# 4、Ubuntu18.04安装uGet

## 添加uGet软件源
```
sudo add-apt-repository ppa:plushuang-tw/uget-stable
```

## 更新uGet软件源
```
sudo apt-get update
```

## 安装uGet
```
sudo apt-get install uget
```

## 添加aria2软件源
```
sudo add-apt-repository ppa:t-tujikawa/ppa
```

## 安装aria2
```
sudo apt-get install uget
```

## 配置aria2
1. 打开uGet软件，从菜单中选择“编辑 > 设置”，并在弹出的界面中选择“插件”
2. 选择插件匹配顺序为`aria2`，并设置参数`--enable-rpc=true -D --disable-ipv6 --check-certificate=false`
3. 重启uGet，使配置生效

# 参考文档

1. [如何在Ubuntu 18.04中安装Sublime Text 3.2](https://www.linuxidc.com/Linux/2019-03/157533.htm)
2. [如何给ubuntu安装一个类似迅雷的下载软件](https://jingyan.baidu.com/article/215817f740f01a1eda1423f3.html)
