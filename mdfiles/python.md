Python学习笔记（自用）
=======
* 解除云班课视频限制
```python
import requests
def cookie_to_dic(cookie):
    return {item.split('=')[0]: item.split('=')[1] for item in cookie.split('; ')}
cookie="_uab_collina=159048125601474951215473; login_token=d79a7bb97ed6bc96f66a563dfbb5b26d85ed2f43be297d11203d2bc8cfb1a391; _ga=GA1.2.215999139.1591430804; _gid=GA1.2.1794318999.1591430804; acw_tc=2f624a7515914322935547549e2462cc210a7ba9aab44217ea077a45b2c43c; teachweb=e57ff98cea8160a9f28a4554d6b1e3ecb2da959d; SERVERID=aa93d3f37c880aa9b372ac3493efb185|1591432582|1591430408"
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
