# week issues 4

## 工具
- 自动生成changelog[github-changelog-generator](https://github.com/github-changelog-generator/github-changelog-generator)

- [shadowsocks](https://shadowsocks.org/en/index.html)

	最近Google Cloud试用到期，看来是大佬的羊毛薅不到了。幸好还有香港的阿里云服务器，so开干！

	1. shadowsocks服务端下载见https://shadowsocks.org/en/download/servers.html
	2. 服务端配置见 https://shadowsocks.org/en/config/quick-guide.html
	3. 阿里云⚠️/etc/shadowsocks.json中开放的端口需要 运行命令开放，iptables -A INPUT -p tcp --dport 8388 -j ACCEPT
	4. 阿里云⚠️服务器实例的安全组规则需要增加 自定义 TCP 在 相关端口（8388） 的访问 ,（允许所有ip访问，设置为0.0.0.0/0）

## 教程
- 计算机速成课 | Crash Course 字幕组 (全40集 2018-5-1 精校完成)[Crash Course](https://www.bilibili.com/video/av2137…) awesome!!

## Github
- 一款入门级的人脸、视频、文字检测以及识别的项目[faceai](https://github.com/vipstone/faceai)

- 使用树莓派开发操作系统[raspberry-pi-os](https://github.com/s-matyukevich/raspberry-pi-os)

## 金句
- 社会化大分工的弊端之一，就是让人们以为工具本身就是有用的。其实，工具都是为了解决实际问题存在的，要想产生真正的生产力，就应该跳出一个事物的工具性，以问题导向来审视工具。

- 工程师的5个等级：
	- 第五级：能独立解决问题，完成工程任务；
	- 第四级：能指导和带领其他人一同完成更有影响力的工作；
	- 第三级：能独立设计和实现产品，平且在市场上获得成功；
	- 第二级：能设计和实现别人不能做出的产品，也就是说他的作用很难取代；
	- 第一级：开创一个产业。

- 复盘的四步骤：
	- 第一个步骤、回顾目标：当初的目的或期望是什么；
	- 第二个步骤、评估结果：和原定目标相比有哪些亮点和不足；
	- 第三个步骤、分析原因：事情成功和失败的根本原因，包括主观和客观两方面；
	- 第四个步骤、总结经验：需要实施哪些新举措，需要继续哪些措施，需要叫停哪些项目。
