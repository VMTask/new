---
title: PyQt5常用代码
date: 2022-05-01 13:39:00.379
updated: 2022-07-12 17:57:27.951
url: https://vmtask.com/archives/pyqt5-codes
cover: https://s1.ax1x.com/2022/05/01/O9BWjJ.jpg
categories: 
- 默认
- 软件工程
tags: 
- Windows
- Python
- PyQt5
---

# PyQt5常用代码
## init代码 
```python
if __name__ == "__main__":
  import sys
  app = QtWidgets.QApplication(sys.argv)
  MainWindow = QtWidgets.QMainWindow()#MainWindow由启动类型确定，可自行更改，接下来都是这样
  ui = Ui_MainWindow()
  ui.setupUi(MainWindow)
  MainWindow.show()
  sys.exit(app.exec_())
```
## pyuic转换
```bash
pyuic5 -o 生成文件名.py ui文件.ui
"""
qrc文件也可以这样转换，如果ui文件里面有包括qrc文件的话，则需要转换qrc文件，否则可能会出错。
"""
```
## initDialog类型
```python
if __name__ == "__main__":
  import sys
  app = QtWidgets.QApplication(sys.argv)
  Dialog = QtWidgets.QDialog()#Dialog由启动类型确定，可自行更改，接下来都是这样
  ui = Ui_Dialog()
  ui.setupUi(Dialog)
  Dialog.show()
  sys.exit(app.exec_())
```