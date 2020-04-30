Python学习笔记（自用）
=======
* 感觉不错的输入
```python
 a,b = input().split()  #读入两个数到a b中
 a,b = map(int,input().split(','))  #读入两个整数到a，b中，输入的数用逗号分隔
 a,b = map(int,input().split(' '))  #读入两个整数到a，b中，输入的数用空格分隔
 ```
 * 判断闰年
 ```python
 def leap_year(a):
    if ((a%4==0) and (a%100 !=0)) or (a%400==0):  #判断是否为闰年
        return True
    else:
        return False
print(leap_year(int(input())))
```
 >不断更新中...
