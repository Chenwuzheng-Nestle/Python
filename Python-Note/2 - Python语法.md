### 1 - 内容编码

- python解释器在加载 .py 文件中的代码时，会对内容进行编码（默认ascill）

- ASCII（American Standard Code for Information Interchange，美国标准信息交换代码）是基于拉丁字母的一套电脑编码系统，主要用于显示现代英语和其他西欧语言，其最多只能用 8 位来表示（一个字节），即：2**8 = 256，所以，ASCII码最多只能表示 256 个符号。

![](http://images2015.cnblogs.com/blog/425762/201510/425762-20151024170543724-275959633.png)
![](http://images2015.cnblogs.com/blog/425762/201510/425762-20151024170628833-536583386.png)

- 显然ASCII码无法将世界上的各种文字和符号全部表示，所以，就需要新出一种可以代表所有字符和符号的编码，即：Unicode

- Unicode（统一码、万国码、单一码）是一种在计算机上使用的字符编码。Unicode 是为了解决传统的字符编码方案的局限而产生的，它为每种语言中的每个字符设定了统一并且唯一的二进制编码，规定虽有的字符和符号最少由 16 位来表示（2个字节），即：2 **16 = 65536，
注：此处说的的是最少2个字节，可能更多

- UTF-8，是对Unicode编码的压缩和优化，他不再使用最少使用2个字节，而是将所有的字符和符号进行分类：ascii码中的内容用1个字节保存、欧洲的字符用2个字节保存，东亚的字符用3个字节保存...

- 所以，python解释器在加载 .py 文件中的代码时，会对内容进行编码（默认ascill）

- 终端是用GBK编码写成的，所以有时候在python执行的.py文件中包含中文的话在终端运行会出现乱码的样子,在.py文件中可以将编码改成GBK文件输出与终端中
- 
```python 
python 2.7
temp = "你好"
temp_unicode = temp.decode("utf-8") // 编码
temp_gbk = temp_unicode.encode("gbk") // 解码
print(temp)
这样的话在终端运行就会输出中文的你好，而不是乱码的东西了

python 3
temp = "你好"
temp_gbk = temp.encode("gbk")
print(temp_gbk)
python3中会自动转换utf-8  gbk unicode，并且移除了unicode类型
```

--- 

### 2 - 注释
- 当行注视：# 被注释内容
- 多行注视：""" 被注释内容 """

---

### 3 - 执行脚本传入参数
- Python有大量的模块，从而使得开发Python程序非常简洁。类库有包括三中：
 1. Python内部提供的模块
 2. 业内开源的模块
 3. 程序员自己开发的模块
 4. Python内部提供一个 sys 的模块，其中的 sys.argv 用来捕获执行执行python脚本时传入的参数

```python
#!/usr/bin/dev python
# -*- coding:utf-8 -*-

import sys

print sys.argv
```

---

### 4 - pyc 文件
- 执行Python代码时，如果导入了其他的 .py 文件，那么，执行过程中会自动生成一个与其同名的 .pyc 文件，该文件就是Python解释器编译之后产生的字节码。
- ps：代码经过编译可以产生字节码；字节码通过反编译也可以得到代码。

---

### 5 - 变量
- 变量的作用：昵称，其代指内存里某个地址中保存的内容

##### 5.1 - 声明变量
```python
#!/usr/bin/env python
# -*- coding: utf-8 -*-

#声明了一个变量，变量名为:name，变量name的值为："chenwuzheng"  
name = "chenwuzheng"
```

##### 5.2 - 变量定义的规则：
1. 变量名只能是 字母、数字或下划线的任意组合
2. 变量名的第一个字符不能是数字

##### 5.3 - 以下关键字不能声明为变量名:
```python
['and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'exec', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'not', 'or', 'pass', 'print', 'raise', 'return', 'try', 'while', 'with', 'yield']
```

##### 5.4 - 变量的赋值
```python
#!/usr/bin/dev python
# -*- coding:utf-8 -*-
name1 = "wupeiqi"
name2 = "alex"
```
![](http://images2015.cnblogs.com/blog/425762/201510/425762-20151024180236677-1430341076.png)

```python
#!/usr/bin/env python
# -*- coding: utf-8 -*-

name1 = "wupeiqi"
name2 = name1
```
![](http://images2015.cnblogs.com/blog/425762/201510/425762-20151024180334849-979288684.png)

---

### 6 - 输入
```python
#!/usr/bin/env python
# -*- coding: utf-8 -*-
  
# 将用户输入的内容赋值给 name 变量
name = raw_input("请输入用户名：")
  
# 打印输入的内容
print name
```

###### 输入密码时，如果想要不可见，需要利用getpass 模块中的 getpass方法，即：

```python
#!/usr/bin/env python
# -*- coding: utf-8 -*-
  
import getpass
  
# 将用户输入的内容赋值给 name 变量
pwd = getpass.getpass("请输入密码：")
  
# 打印输入的内容
print pwd
```

---

### 7 - 基本数据类型
- 数字：
 - 123

- 字符串: 
 - "123"
 - '123'
 - """123"""

- 布尔值:
 - True
 - Falus

### 8 - if/else
```python
if 条件:
    内容
elif 条件:
    内容
elif 条件:
    内容
else:
    内容
    
条件:
	True False
	1 > 2 | n1 > n2 | n1 == n2
	name == "cwz" or name == "zy"
	name == "cwz" and name == "zy"
	name != "cwz"
    
```
 
- 提示输入用户名和密码,验证用户名和密码
 
```python
#!/usr/bin/dev python
# -*- coding:utf-8 -*- 

import getpass

UserAccount = raw_input("请输入账号")
UserPwd = getpass.getpass("请输入密码")

if UserAccount == "chenwuzheng" and UserPwd == "123" :
    print("输入正确")
elif UserAccount != "chenwuzheng" and UserPwd == "123":
    print("请输入正确的账号")
elif UserAccount == "chenwuzheng" and UserPwd != "123":
    print("请输入正确的密码")
else:
    print("输入错误")

------------------------------
    
if UserAccount == "chenwuzheng" or UserAccount == "zhaoyi":
    print("输入正确")
else:
    print("输入错误")
```

### 9 - while循环
```python
#如果条件成立 那么就一直执行代码块中的代码
while 条件:	
	代码块
```


```python
#!/usr/bin/dev python
# -*- coding:utf-8 -*-
import time

start = 1
while True:
    print(start)
    start = start + 1
    time.sleep(1) # 休息一秒
    
print("end")
```

---


- break:
 - 用于跳出当前循环，并且break下面的代码，将不再执行.

```python
#!/usr/bin/dev python
# -*- coding:utf-8 -*-
import time

start = 1
flag = True

while flag:
    print(start)
    if start == 5:
        flag = False
        break
    time.sleep(1)
    start = start + 1

print("end")

控制台会输出1.2.3.4.5.6.7.8.9.10.end
```



- continue:
 - 用于跳出本次循环，继续下一次循环.

```python
while True:
    print("123")
    continue
    print("456")
控制台会一直输出123
```
 
> 输出1，2，3，4，5，6，8，9，10

```python
#!/usr/bin/dev python
# -*- coding:utf-8 -*-
import time

num = 1
flag = True

while flag:
    print(num)
    time.sleep(0.5)
    num = num + 1

    if num == 7:
        continue

    if num == 10:
        break
print("end")
```


> 输出1-100的和

```python
#!/user/bin/dev python
# -*- coding:utf-8 -*-

sum = 0
num = 1

while True:
    print(num)
    sum = sum + num

    if num == 100:
        break

    num += 1
print(sum)
```

> 用户登录，三次重试机会

```python
#!/usr/bin/dev python
# -*- coding:utf-8 -*-

import getpass

num = 1

while True:
    userName = raw_input("UserName:")
    userPwd = getpass.getpass("PassWord:")

    if userPwd != "123":
        print("密码错误,请重新输入...")
    elif userName != "chenwuzheng":
        print("账号未注册")
    else:
        print("登录成功")

    if num == 3:
        print("您输入的错误次数过多。请10分钟后在次尝试")

        break

    num += 1
```

 