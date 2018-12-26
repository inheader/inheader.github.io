---
layout:     post
title:      PowerShell未能创建 SSL/TLS 安全通道。
subtitle:   PowerShell未能创建 SSL/TLS 安全通道。
date:       2018-12-24
author:     inheader
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - 工具
---



## 前言

​	今天更新deno的时候PowerShell提示未能创建 SSL/TLS安全通道，于是就去Google了一番，出来了很多结果

最终一一尝试了一番：



答案：

```
# 在Powershell中运行该条命令
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
Invoke-WebRequest -Uri https://apod.nasa.gov/apod/
```

