---
title: 使用goorm免费IDE搭建Halo博客
date: 2022-06-11 11:12:25.974
updated: 2022-07-12 17:56:53.574
url: https://vmtask.com/archives/use-goorm-create-website
cover: https://s1.ax1x.com/2022/06/11/Xc0Hpt.png
categories: 
- 默认
- 网站搭建
tags: 
- goorm
- 免费
- 服务器
---

# 使用goorm免费IDE搭建Halo博客
## 第一步
首先来到https://accounts.goorm.io/signup?return_url=aHR0cHM6Ly9pZGUuZ29vcm0uaW8v注册一个账号。

![](https://s1.ax1x.com/2022/06/11/XcdG7j.png)

然后选择![](https://s1.ax1x.com/2022/06/11/XcdsHJ.png)来新建一个容器

所有选项全部默认，设置一下名字，选择Create进行新建



![](https://s1.ax1x.com/2022/06/11/XcdoHH.png)

出现这个界面请慢慢等待。

![](https://s1.ax1x.com/2022/06/11/Xcdb4I.png)
##  第二步
点击Run Container运行容器，然后在Terminal内输入这些命令:

```bash
sudo apt update && sudo apt-get install openjdk-11-jre -y && mkdir ~/app && cd ~/app && wget https://dl.halo.run/release/halo-1.5.3.jar -O halo.jar && wget https://dl.halo.run/config/application-template.yaml -O ./application.yaml && sudo apt install screen -y && screen -s halo
```

```bash
cd ~/app && java -jar halo.jar
```

使用<kbd>Ctrl</kbd>+<kbd>A</kbd>，然后按下<kbd>d</kbd>，即可退出虚拟终端。

然后再回到Dashboard，点击三个点，选择Go To Settings，下拉找到URL/Port，选择Add，一定要选择*.run.goorm.io，自定义域名要钱，选择你想要的三级域名，Port选择8089，点击你新建的域名，就可以访问你的Halo博客了。
## 提醒
> 但是要注意，要打开Always-on选项，否则24小时就会休眠一次，这个选项只能使用一个容器。