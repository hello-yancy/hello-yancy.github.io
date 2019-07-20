---
title: 安装CMake
date: 2019-07-20 10:16:52
tags: 
- CMake
categories:
- 软件开发
---

# Linux下安装GCC
由于CMake的编译安装需要依赖gcc，因此要先安装gcc

## Ubuntu18.04下安装
Ubuntu提供了一个build-essential软件包，该软件包提供了编译c/c++所需要的所有软件包。查看build-essential软件包的依赖关系如下：
```
$ apt-cache depends build-essential
build-essential
 |依赖: libc6-dev
  依赖: <libc-dev>
    libc6-dev
  依赖: gcc
  依赖: g++
  依赖: make
    make-guile
  依赖: dpkg-dev

```

因此，只需要执行以下命令安装build-essential，相关依赖的gcc等就会被安装了
```
sudo apt-get install build-essential 
```

## 验证安装结果
使用`gcc --version`命令，验证安装是否成功，示例如下：
```
$ gcc --version
gcc (Ubuntu 7.4.0-1ubuntu1~18.04.1) 7.4.0
Copyright (C) 2017 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

# Linux下安装CMake

## 下载并安装
从[CMake的官网](https://cmake.org/download/)，下载源代码包cmake-3.15.1.tar.gz，并上传至后台`/usr/local/src`

```
cd /usr/local/src
tar -xzf cmake-3.15.1.tar.gz

cd /usr/local/src/cmake-3.15.0
./bootstrap
make
sudo make instal
```

## 验证安装结果
使用`cmake --version`命令，验证安装是否成功，示例如下：
```
$ cmake --version
cmake version 3.15.0

CMake suite maintained and supported by Kitware (kitware.com/cmake).
```

