Python学习笔记（自用）
=======
* 调用Google翻译API方式<br>
通过调用googletrans的库我们可以通过以下的python代码实现对一段文本的翻译。首先导入googletrans库，第3行实例化一个翻译对象，其中参数service_urls设置为谷歌翻译的网址。第5行调用translate方法获得翻译结果，其中参数source为需要翻译的文本，src为待翻译的文本的语言类型（这里设置为中文），dest为翻译成的文本语言类型（这里设置为英文），获取翻译结果中的文本类型作为最终翻译结果输出。
```python
# -*- coding: utf-8 -*-
from googletrans import Translator
translator = Translator(service_urls=['translate.google.cn'])
source = '懒松鼠'
text = translator.translate(source,src='zh-cn',dest='en').text
print(text)
# >Lazy Squirrel
```

* 通过如下代码可实现语言类型识别，如输入s1输出zh（表示为中文）：
```python
from langid import classify
s1 = "懒松鼠"
array = classify(s1)
print (array[0])
# > zh
```

* 解除云班课视频限制
```python
import requests
def cookie_to_dic(cookie):
    return {item.split('=')[0]: item.split('=')[1] for item in cookie.split('; ')}
cookie="自己的cookie内容"
#下面为视频的信息
dict2={'clazz_course_id':'3C69F064-6E41-4121-981E-B05346CC1022','res_id':'C0CC6B6A-469D-4CB5-846D-5884F419BED7','watch_to':'22','duration':'22','current_watch_to':'22'}
cookie_2=cookie_to_dic(cookie)

url = "https://www.mosoteach.cn/web/index.php?c=res&m=save_watch_to"
r=requests.post(url,cookies=cookie_2,data=dict2)
print(r.text)
print(r.status_code)
```

* 分割字符串并存为csv文件
```python
import pandas as pd
str = "dl22 张三  李四  息哥  懒松鼠"
str_list = str.split()
name = ['学生姓名']
test = pd.DataFrame(columns=name,data=str_list)
path = "C:\\Users\\Administrator\\Desktop\\test1.csv"
print(path)
test.to_csv(path)

```
* 在cmd中把ui文件转成py(前提：安装pyqt5和pyqt5-tools;x为文件名;也可以在Pycharm中添加这个工具)好像没有主函数
```
Microsoft Windows [Version 10.0.14393]
(c) 2016 Microsoft Corporation。保留所有权利。

C:\Users\Administrator>d:

D:\>cd Users\Administrator\PycharmProjects\GUI

D:\Users\Administrator\PycharmProjects\GUI>pyuic5 -o x.py x.ui（生成的py文件没有执行的部分）

D:\Users\Administrator\PycharmProjects\GUI>pyuic5 -o x.py x.ui -x(生成的py文件可以直接执行)
```
其中`D:\Users\Administrator\PycharmProjects\GUI`为文件`x.py`的所在路径
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
