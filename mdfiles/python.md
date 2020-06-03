Python学习笔记（自用）
=======
* 在cmd中把ui文件转成py(前提：安装pyqt5和pyqt5-tools;x为文件名;也可以在Pycharm中添加这个工具)
```
Microsoft Windows [Version 10.0.14393]
(c) 2016 Microsoft Corporation。保留所有权利。

C:\Users\Administrator>d:

D:\>cd Users\Administrator\PycharmProjects\GUI

D:\Users\Administrator\PycharmProjects\GUI>pyuic5 -o x.py x.ui

D:\Users\Administrator\PycharmProjects\GUI>
```
* range函数，代表生成一系列数，如果range(0,6,`1`)，意思就是从0开始，到6结束（不包括6），每次增加1（也就是步长为1），生成一个数组，结果就是\[0,1,2,3,4,5\](虽简单，但建议以后都加第三个参数，以免时间久了就忘了)
* 感觉不错的输入
```python
 a,b = input().split()  #读入两个数到a b中
 a,b = map(int,input().split(','))  #读入两个整数到a，b中，输入的数用逗号分隔
 a,b = map(int,input().split(' '))  #读入两个整数到a，b中，输入的数用空格分隔
```
 * import
 ```python
 import只有三种使用方法，以turtle库为例：

import turtle

from turtle import setup   或  from turtle import *

import turtle as t  （其中t是别名，可以更换其他名称）
 ```
* 字符串
```python
"去掉字符串两侧指定字符"对应功能是.strip()

"按照指定字符分割字符串为数组"对应功能是.split()

"替换字符串中特定字符"对应功能是.replace()
```
* 进制
```
十进制：一般表示
二进制：0b 或 0B 开头
八进制：0o 或 0O 开头
十六进制：0x 或 0X 开头
```
* for .. in .. 中 in 的后面需要是一个迭代类型（组合类型）
* 死循环能够用于测试性能，形式上的死循环可以用break来退出
* 函数的定义<br>def vfunc(*a, b) 是错误的定义：*a表示可变参数，可变参数只能放在函数参数的最后。
* 函数可以包含0个或多个return语句
* 递归函数必须有基例 , 递归函数的基例不再进行递归 , 递归函数的基例决定递归的深度 , 每个递归函数至少存在一个基例，但可能存在多个基例。
* 函数或类是程序的集合和抽象，文件不是。文件是数据的集合和抽象。文件是存储在辅助存储器上的数据序列。
 >不断更新中...
