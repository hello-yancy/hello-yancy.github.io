---
title: 搭建个人博客
date: 2019-07-05 00:30:57
categories:
- Hexo
tags: 
- Hexo
---

# 搭建博客

npm install -g hexo-cli

# 优化博客



# 重建博客

从github上下载个人博客系统的源代码，并安装相关依赖：
```
mkdir -p ~/workspace/hexo
cd ~/workspace/hexo
git clone https://github.com/hello-yancy/hello-yancy.github.io
cd hello-yancy.github.io
npm install hexo --save
```
编译并部署博客：
```
hexo g
hexo s
```
访问http://localhost:4000，验证博客是否正常

# Hexo发布博客引用自带图片的方法


# 参考文档

1. [超详细Hexo+Github Page搭建技术博客教程](https://segmentfault.com/a/1190000017986794#articleHeader2)
2. [Hexo发布博客引用自带图片的方法](https://www.jianshu.com/p/cf0628478a4e)

https://www.jianshu.com/p/1f8107a8778c