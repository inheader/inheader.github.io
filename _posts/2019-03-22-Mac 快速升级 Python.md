---
layout:     post
title:      Mac 快速升级 Python。
subtitle:   Mac 快速升级 Python。
date:       2019-03-22
author:     inheader
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - 工具
---



# 前言

`Mac OSX` 默认的 `Python` 版本是 `2.7`。但由于 `2.7` 版本到了 2020 年就不再维护，我们非常有必要直接升级到 `Python 3` 。



## 下载Python

官网地址：[Python for macOS](https://www.python.org/downloads/mac-osx/)



## 安装zsh

运行命令：

```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```



## 设置命令 Alias

我试用的是 `Fish shell` ，所以我只需要设置一个 `Alias` 即可设置 `python` 的默认版本为 `3`

打开 zshrc shell` 配置文件：

```
vim ~/.zshrc
```

在最后的位置加入：

```
alias python="/usr/local/bin/python3.7"
```

运行命令：

```shell
source ~/.zshrc
```

重新打开一个新的 `iterm` 窗口，运行 `python --version` 即可查看当前 `python` 版本。


