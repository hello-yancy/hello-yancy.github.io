---
title: Npm常用命令
date: 2019-10-27 10:16:44
tags:
- Npm
categories:
- 软件开发
- JavaScript
---

npm是随同Node.js一起安装的包管理工具，能解决Node.js代码部署上的很多问题，常见的使用场景有以下几种：
允许用户从npm服务器下载别人编写的第三方包到本地使用。
允许用户从npm服务器下载并安装别人编写的命令行程序到本地使用。
允许用户将自己编写的包或命令行程序上传到NPM服务器供别人使用。

# 常用命令列表

|命令|格式|说明|
|--|--|--|
|查询版本|npm -v|--|
|安装模块（本地）|npm install &lt;Module Name&gt;|1.将安装包放在./node_modules下，如果没有</br>node_modules目录，则会在当前目录下生成该目录</br>2.可以通过 require() 来引入本地安装的包|
|安装模块（全局）|npm install &lt;Module Name&gt; -g|1.将安装包放在/usr/local下，或者Node.js的安装目录</br>2.可以直接在命令行里使用|
|卸载模块|npm uninstall &lt;Module Name&gt;|--|
|更新模块|npm update &lt;Module Name&gt;|--|
|搜索模块|npm search &lt;Module Name&gt;|--|
|查看安装信息（全局）|npm list -g|npm list -g --depth 0|
|查看安装信息（模块）|npm list &lt;Module Name&gt;|--|


# 参考文档

1. [NPM 使用介绍](https://www.runoob.com/nodejs/nodejs-npm.html)
2. [npm常用命令](https://www.jianshu.com/p/7ea13d57638b)
