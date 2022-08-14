---
title: 如何安装新版记事本
date: 2022-07-11 18:19:18.827
updated: 2022-07-12 17:53:12.782
url: https://vmtask.com/archives/how-to-install-notepad
cover: https://s1.ax1x.com/2022/04/28/LX7ZM8.jpg
categories: 
- 默认
- 软件工程
tags: 
- 记事本
- Windows
---

# 如何安装新版记事本

大家应该都知道最近微软在预览版渠道发布了新版记事本吧，我们这些正式版的用户，要是也想获得微软为Win11打造的记事本的话，那就跟我往下做吧!

{bilibili bvid="BV1US4y1D73y" page=""/}

最终结果:

![img](https://raw.vmtask.top/uploads/1-1024x576.png)

## 第一步

首先，用你的浏览器（最好有代理）访问https://store.rg-adguard.net/，选择URL（link），填入https://www.microsoft.com/store/productId/9MSMLRH6LZF3，选择Fast通道，点击确定，加载完成后选择Microsoft.WindowsNotepad_11.2111.0.0_neutral_~_8wekyb3d8bbwe.Msixbundle下载

然后打开你的压缩软件，将下载进去的安装包打开

![如何安装新版记事本-VMTask的博客](https://raw.vmtask.top/uploads/464702038154c33537969cb646e15671225b0b3a.png@942w_531h_progressive..jpg)

## 第二步

找到大小最大的那个，按照你的系统位数选择，然后解压

![如何安装新版记事本-VMTask的博客](https://raw.vmtask.top/uploads/3-1024x576.png)

## 第三步

解压之后会获得一个文件夹，将AppxMetadata，[Content_Types].xml，AppxBlockMap.xml和AppxSignature.p7x删除，并打开一个管理员身份的Terminal

![如何安装新版记事本-VMTask的博客](http://raw.vmtask.top/uploads/5-1024x576.png)

## 第四步

然后输入Get-AppxPackage *notepad* | Remove-AppxPackage -AllUsers，运行完成后再输入Add-AppxPackage -Register “你的文件位置”#不加” “之后，回车，微软为Win11打造的记事本已经安装到你的电脑里了!

