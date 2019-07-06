---
title: 安装Go
date: 2019-07-06 23:19:43
tags: 
- Go
categories:
- 软件开发
---

# Linux下安装Go

## 下载并安装
从[Go](https://golang.google.cn/)的官网，下载安装包go1.12.6.linux-amd64.tar.gz，并上传至后台`/usr/local/src`

```
cd /usr/local/src
tar -C /opt -xzf go1.12.6.linux-amd64.tar.gz
```

## 配置环境变量
打开/etc/profile文件，并在该文件中增加以下内容
```
export GO_ROOT=/opt/go
export PATH=$GO_ROOT/bin:$PATH
```
执行`source /etc/profile`使配置生效

## 验证安装结果
使用`go version`命令，验证安装是否成功，示例如下：
```
$ go version
go version go1.12.6 linux/amd64
```

使用`go env`命令，查看Go的配置信息，示例如下：
```
$ go env
GOARCH="amd64"
GOBIN=""
GOCACHE="/home/yancy/.cache/go-build"
GOEXE=""
GOFLAGS=""
GOHOSTARCH="amd64"
GOHOSTOS="linux"
GOOS="linux"
GOPATH="/home/yancy/go"
GOPROXY=""
GORACE=""
GOROOT="/opt/go"
GOTMPDIR=""
GOTOOLDIR="/opt/go/pkg/tool/linux_amd64"
GCCGO="gccgo"
CC="gcc"
CXX="g++"
CGO_ENABLED="1"
GOMOD=""
CGO_CFLAGS="-g -O2"
CGO_CPPFLAGS=""
CGO_CXXFLAGS="-g -O2"
CGO_FFLAGS="-g -O2"
CGO_LDFLAGS="-g -O2"
PKG_CONFIG="pkg-config"
GOGCCFLAGS="-fPIC -m64 -pthread -fmessage-length=0 -fdebug-prefix-map=/tmp/go-build428916699=/tmp/go-build -gno-record-gcc-switches"
```

# 安装Beego

## 下载并安装
由于无法使用`go get github.com/astaxie/beego`命令直接下载安装，那么以下介绍离线方式安装，首先从[Beego的代码库](https://github.com/astaxie/beego)，下载安装包beego-1.12.0.zip，并上传至后台`$GOPATH/src/github.com/astaxie`，然后执行以下命令安装

```
cd /home/yancy/go/src/github.com/astaxie
unzip beego-1.12.0.zip
mv beego-1.12.0 beego
go get github.com/astaxie/beego
```

## 验证安装结果
参考[Beego官网](https://beego.me/)中的方法验证


# 安装Bee
## 下载并安装
采用离线方式安装，首先从[Bee的代码库](https://github.com/beego/bee)，下载安装包beego-1.12.0.zip，并上传至后台`$GOPATH/src/github.com/astaxie`，然后执行以下命令安装

```
cd /home/yancy/go/src/github.com/beego
unzip bee-1.10.0.zip
mv bee-1.10.0 bee
go get github.com/beego/bee
```
注：执行`go get github.com/beego/bee`后，会在$GOPATH/bin下生成bee工具

## 配置环境变量
打开/etc/profile文件，并在该文件中增加以下内容
```
export GO_PATH=/home/yancy/go
export PATH=$GO_PATH/bin:$PATH
```

## 验证安装结果
使用`bee version`命令，验证安装是否成功，示例如下：
```
$bee version
______
| ___ \
| |_/ /  ___   ___
| ___ \ / _ \ / _ \
| |_/ /|  __/|  __/
\____/  \___| \___| v1.10.0

├── Beego     : 
├── GoVersion : go1.12.6
├── GOOS      : linux
├── GOARCH    : amd64
├── NumCPU    : 4
├── GOPATH    : 
├── GOROOT    : /opt/go
├── Compiler  : gc
└── Date      : Sunday, 7 Jul 2019

```