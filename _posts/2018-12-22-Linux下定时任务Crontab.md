---
layout:     post
title:      crontab 定时任务
subtitle:   Linux下定时任务Crontab
date:       2018-12-22
author:     inheader
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - Linux
---



## 使用规则

![](http://images.duobanzhe.com/blog/crontab.png)

## 常用命令

	# 编辑任务
	crontab -e
	
	# 查看任务
	crontab -l
	
	# 删除任务
	crontab -r
	
	# 重启任务
	service crond restart
	
	# 中文编码兼容
	export LANG=en_US.UTF-8



## 使用实例

	# 每1分钟执行一次myCommand
	* * * * * myCommand
	
	# 每小时的第3和第15分钟执行
	3,15 * * * * myCommand
	
	# 在上午8点到11点的第3和第15分钟执行
	3,15 8-11 * * * myCommand
	
	# 每隔两天的上午8点到11点的第3和第15分钟执行
	3,15 8-11 */2  *  * myCommand
	
	# 每周一上午8点到11点的第3和第15分钟执行
	3,15 8-11 * * 1 myCommand
	
	# 每晚的21:30重启smb
	30 21 * * * /etc/init.d/smb restart
	
	# 每月1、10、22日的4 : 45重启smb
	45 4 1,10,22 * * /etc/init.d/smb restart
	
	# 每周六、周日的1 : 10重启smb
	10 1 * * 6,0 /etc/init.d/smb restart
	
	# 每天18 : 00至23 : 00之间每隔30分钟重启smb
	0,30 18-23 * * * /etc/init.d/smb restart
	
	# 每星期六的晚上11 : 00 pm重启smb
	0 23 * * 6 /etc/init.d/smb restart
	
	# 每一小时重启smb
	* */1 * * * /etc/init.d/smb restart
	
	# 晚上11点到早上7点之间，每隔一小时重启smb
	0 23-7 * * * /etc/init.d/smb restart


### 工具

```
http://cron.qqe2.com/
```

