Python学习笔记（自用）
=======
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
 >不断更新中...
