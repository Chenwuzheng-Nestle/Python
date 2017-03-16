#Python简介 

1. python的创始人为吉多·范罗苏姆（Guido van Rossum）。1989年的圣诞节期间，吉多·范罗苏姆为了在阿姆斯特丹打发时间，决心开发一个新的脚本解释程序，作为ABC语言的一种继承。  

2. Python可以应用于众多领域，如：数据分析、组件集成、网络服务、图像处理、数值计算和科学计算等众多领域。目前业内几乎所有大中型互联网企业都在使用Python，如：Youtube、Dropbox、BT、Quora（中国知乎）、豆瓣、知乎、Google、Yahoo!、Facebook、NASA、百度、腾讯、汽车之家、美团等。
3. 互联网公司广泛使用Python来做的事一般有：自动化运维、自动化测试、大数据分析、爬虫、Web 等。


###为什么是Python而不是其他语言？
1. C 和 Python、Java、C#等
2. C语言：代码编译得到 机器码 ，机器码在处理器上直接执行，每一条指令控制CPU工作
3. 其他语言：代码编译得到 字节码 ，虚拟机执行字节码并转换成机器码再后在处理器上执行


###Python 和 CPython这门语言是由C开发而来
1. 对于使用：Python的类库齐全并且使用简洁，如果要实现同样的功能，Python 10行代码可以解决，C可能就需要100行甚至更多.
2. 对于速度：Python的运行速度相较与C，绝逼是慢了
3. 对于使用：Linux原装Python，其他语言没有；以上几门语言都有非常丰富的类库支持
4. 对于速度：Python在速度上可能稍显逊色

***Python和其他语言没有什么本质区别，其他区别在于：擅长某领域、人才丰富、先入为主。***


###Python的种类

1. Cpython
Python的官方版本，使用C语言实现，使用最为广泛，CPython实现会将源文件（py文件）转换成字节码文件（pyc文件），然后运行在Python虚拟机上。

2. Jyhton
Python的Java实现，Jython会将Python代码动态编译成Java字节码，然后在JVM上运行。

3. IronPython
Python的C#实现，IronPython将Python代码编译成C#字节码，然后在CLR上运行。（与Jython类似）

4. PyPy（特殊）
Python实现的Python，将Python的字节码字节码再编译成机器码。
RubyPython、Brython ...

###除PyPy之外，其他的Python的对应关系和执行流程如下：
![](http://images2015.cnblogs.com/blog/425762/201510/425762-20151024113930614-2128955181.png)

![](http://images2015.cnblogs.com/blog/425762/201510/425762-20151024114048849-189055880.png)

PyPy，在Python的基础上对Python的字节码进一步处理，从而提升执行速度！
![](http://images2015.cnblogs.com/blog/425762/201510/425762-20151024114724817-2135944387.png)
