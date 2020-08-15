---
title: Linux安装并配置git
date: 2020-08-15 11:50:20
categories: Linux
tags: Linux
---

### 1. 下载最新 git 安装包

[https://github.com/git/git/releases](https://github.com/git/git/releases)
[git-v2.23.0 点击此出可直接下载](https://github.com/git/git/archive/v2.23.0.tar.gz)

### 2. 在服务器解压安装包

1. 通过 Xftp 工具传输到/usr/local 文件夹下，文件夹目录可自行更改，一般放到此目录下
2. 解压安装包,并重命名文件夹名，删除安装包

```shell
tar -zxvf git-2.23.0.tar.gz
mv git-2.23.0 git
rm -rf git-2.23.0.tar.gz
```

### 3. 安装编译源码所需依赖

为防止编译源码报错，先安装以下依赖

```shell
yum install openssl-devel expat-devel libcurl-dev libcurl-devel
```

一路按 y 即可

### 4. 编辑并安装 git

```shell
cd git
make prefix=/usr/local/git all
make prefix=/usr/local/git install
```

耐心等待，如果出错不要慌，复制错误信息 google 或者百度一下，很容易找到解决方法的，一般就是少了一些依赖

### 5. 配置环境变量

1. 编辑/etc/profile 文件

```shell
vim /etc/profile
```

2. 按 i 键进入编辑模式，在尾部添加以下内容，然后保存退出（Esc --> :wq --> enter）

```shell
#nodejs
export PATH=$PATH:/usr/local/git/bin
```

### 6. 验证是否安装配置成功

```shell
git --version
```

输出版本号就表示 OK 了

`怕什么真理无穷，进一寸有进一寸的惊喜~`
