---
title: BCM4转EXE
date: 2022-07-12 18:16:33.304
updated: 2022-07-12 18:16:33.304
url: https://vmtask.com/archives/bcm4-to-exe
cover: https://s1.ax1x.com/2022/05/03/OFBhEd.png
categories: 
- 软件工程
tags: 
- BCM
- Kitten4
- Nodejs
---

# Bcm4转EXE

## 附视频:

<joe-bilibili bvid="BV1Aq4y1a7PZ"></joe-bilibili>
​	大家在使用源码编辑器3的时候，都能够很轻松的通过编程猫格式工厂来进行转换EXE，但是bcm并没有提供适用于Kitten4的格式工厂，如果强行转格式，将会出现以下情况:

## 1.根本无法转换

​	bcm和bcm4文件其实是基于xml格式的，里面有version限制，你把文件拖进去，得到的也只是一个格式工厂暂不支持Kitten4的提示。就算改了xml文件，也会出现以下状况:

## 2.转换后的EXE无法运行

![点此可查看详情](https://s1.ax1x.com/2022/04/05/qOPbCt.png)

​	基本上都会出现这种状况，因为不兼容。

# 解决方案

## 通过Nativefier将HTML封装为EXE

### 首先，我们需要安装Nodejs。Win11，Win10高版本的用户可以直接使用命令安装，安装方法如下:

首先，打开微软应用商店，确保所有应用都已经更新到最新，尤其是Windows软件包管理器。然后Win10按住Shift+右键，选择"在此处打开命令窗口/Powershell"，Win11直接右键，选择"在Windows终端打开"，然后输入:

```bash
winget install OpenJS.NodeJS.LTS
```

## Win8.1以下的这样做:

首先，前往这个[网址](http://nodejs.cn/download/)，然后按照你的系统位数选择版本。

![屏幕截图 2022 04 05 145814](https://s1.ax1x.com/2022/04/05/qOCmyF.png)

安装过程就一路点Next就行了，倒数第二步点Install，最后一步点Finish，就安装成功了。

## Nativefier配置

由于Nodejs并不会默认安装Nativefier，所以我们需要手动安装。和以前一样，先打开命令行，输入:

```bash
npm install nativefier -g 
```

然后就开始下载Nativefier了。不过最好换源，否则下载很慢。换源命令：

```bash
npm set registry https://registry.npm.taobao.org/
```

安装好Nativefier之后，就可以开始获取你的项目实际位置了:

我们的作品一般是这样的:

![点此可查看详情](https://s1.ax1x.com/2022/04/05/qOP236.png)

不知道你们有没有注意到这里:

![点此可查看详情](https://s1.ax1x.com/2022/04/05/qOP641.png))

最后面的那一串数字就是我们的作品号。我们在浏览器里面输入这个[网址](https://player.codemao.cn/new/)+你的作品号，就可以获得你的作品的真实网址了。

![点此可查看详情](https://s1.ax1x.com/2022/04/05/qOiPCq.png)

既然我们知道了这个网址了，那转换就很容易了，在命令行里输入:

```bash
nativefier https://player.codemao.cn/new/+你的作品号
```

第一次使用要下载一个依赖包，网址在国外，我也是下了一个小时才下载下来，所以有魔法的人最好用上你们的魔法，要不然也得像我这样，下载一个小时。下载完之后的生成倒是很快，一下子就好了。

## 通过一键转换工具进行转换	

一键转换工具的地址我放在这里了:

<joe-cloud title="程序下载" type="default" url="https://raw.vmtask.top/download/bcm4toexe.exe" password=""></joe-cloud>

