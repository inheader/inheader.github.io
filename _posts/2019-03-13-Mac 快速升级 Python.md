---
layout:     post
title:      Mac 快速升级 Python。
subtitle:   Mac 快速升级 Python。
date:       2019-03-13
author:     inheader
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - 工具
---



# 前言

`Mac OSX` 默认的 `Python` 版本是 `2.7`。但由于 `2.7` 版本到了 2020 年就不再维护，我们非常有必要直接升级到 `Python 3` 。本文是基于 [Homebrew](https://brew.sh/) 快速升级。而不对系统自带的 `Python 2.7` 进行删除，因为涉及到系统文件，So 还是替换式比较实际。



## 安装 Homebrew

官网地址：[Homebrew — The missing package manager for macOS](https://brew.sh/)

运行命令：

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

```

即可（注意：安装时间较长）



## 安装 Python 3

只需运行：

```shell
brew install python3
```

非常快速方便，当然如果你想将默认的 `python` 命令替换为 `3` 的版本只需设置一下环境变量。



## 设置命令 Alias

我试用的是 `Fish shell` ，所以我只需要设置一个 `Alias` 即可设置 `python` 的默认版本为 `3`

打开 `fish shell` 配置文件：

```
vim ~/.config/fish/config.fish
```

在最后的位置加入：

```
alias python="/usr/local/Cellar/python3/3.6.4_2/bin/python3"
```

运行命令：

```shell
source ~/.config/fish/config.fish
```

重新打开一个新的 `iterm` 窗口，运行 `python --version` 即可查看当前 `python` 版本。








