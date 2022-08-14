---
title: XTCToolBox1.0更新
date: 2022-07-11 18:17:12.562
updated: 2022-07-12 17:53:34.185
url: https://vmtask.com/archives/xtctoolbox10-update
cover: https://s3.bmp.ovh/imgs/2022/03/161af9bf3e7a266f.jpg
categories: 
- 默认
- 软件工程
tags: 
- XTCToolBox
- Python
- ADB
---

更新内容：

优化更新下载速度，重构代码

<joe-cloud title="64位下载" type="default" url="https://raw.vmtask.top/download/Setup.exe" password=""></joe-cloud>

<joe-cloud title="32位下载" type="default" url="https://raw.vmtask.top/download/Setup32.exe" password=""></joe-cloud>

```python

import os

import time

import sys

import easygui

import urllib

from download import download

from typing import Counter

#Wifi链接函数

def wificonnect():

    ip=input("请输入ip地址:")

    os.system('adb connect '+ip)

    connectbl = os.popen("adb devices").read()

    次数 = connectbl.count("device")

    if(次数 == 1):

        pause=input('连接失败，按回车键再试一次')

        wificonnect()

#主界面函数

def main():

    os.system("cls")#对Console清屏

    路径 =os.getcwd()#获取程序运行路径

    version = "0.10"#设置程序版本，将在更新中检查

    path=路径+"\\color.txt"#读取控制台颜色文件

    colorlist=os.path.exists(path)#检查颜色文件是否存在

    colorlist =str(colorlist)#将变量字符串化

    if("True" in colorlist):

        with open("color.txt", "r") as f:  # 打开文件

            c = f.read()    

            os.system(c)

    print("XTCToolBox 1.0 R