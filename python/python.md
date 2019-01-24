> 天道酬勤。

## 目录
#### 1.Introduce python language
#### 2.类和对象
#### 3.异常处理
#### 4.文件处理
#### 5.模块
<hr>

## <a href="# Introd">1.Introduce python language</a><br>
&nbsp;&nbsp;[维基百科](https://zh.wikipedia.org/wiki/Python)Python（英国发音：/ˈpaɪθən/ 美国发音：/ˈpaɪθɑːn/），是一种广泛使用的高级编程语言，属于通用型编程语言，由吉多·范罗苏姆创造，第一版发布于1991年。可以视之为一种改良（加入一些其他编程语言的优点，如面向对象）的LISP。作为一种解释型语言，Python的设计哲学强调代码的可读性和简洁的语法（尤其是使用空格缩进划分代码块，而非使用大括号或者关键词）。相比于C++或Java，Python让开发者能够用更少的代码表达想法。不管是小型还是大型程序，该语言都试图让程序的结构清晰明了。

与Scheme、Ruby、Perl、Tcl等动态类型编程语言一样，Python拥有动态类型系统和垃圾回收功能，能够自动管理内存使用，并且支持多种编程范式，包括面向对象、命令式、函数式和过程式编程。其本身拥有一个巨大而广泛的标准库。

Python 解释器本身几乎可以在所有的操作系统中运行。Python的正式解释器CPython是用C语言编写的、是一个由社群驱动的自由软件，当前由Python软件基金会管理。

## <a href="# 2.类和对象">2.类和对象</a>
<b>python</b>是面向对象的编程语言，存在类和对象

Python中，声明类的基本结构如下所示：

```
class 类名
    def __init__(self,参数)
    def 函数名（参数）
    
class 类名(继承父类)
    def 函数名（参数）
```

<b>实例：</b>

```
class Infor():
    def __init__(self,name,age,weight):
        self.name=name
        self.age=age
        self.weight=weight
    def printInfor(self):
        print("\n")
        print("-------------------------")
        print("1.name:",self.name)
        print("2.age:",self.age)
        print("3.weight:",self.weight)

class Adva(Infor):
    def __init__(self,weapon,power,idx):
        Infor.__init__(self,"ltc",18,60)
        self.weapon=weapon
        self.power=power
        self.idx=idx
    def printAdva(self):
        print("weapon:",self.weapon,"[power:",self.power[self.idx],"]")

i=0
powers = [98,99,80]
weapon = ["sword","spear"]
myweapon = input("select weapon:")
for item in weapon:
    if(item == myweapon):
        me = Adva(myweapon,powers,i)
        me.printInfor()
        me.printAdva()
    i = i + 1
print("--------------------------")
print("\n")
```

## <a href="# 3.异常处理">3.异常处理</a>
编译程序时即使没有显示语法错误，但运行结果会有错误，这种错误成为“异常”，Python具有异常处理机制，通过异常处理可以编写安全、稳定的程序。

结构如下：

```
try:
    可能发生异常的语句
except 异常类型:
    异常处理时出现的语句
else:
    未出现异常时执行的语句
finally:
    无论是否异常都必须执行的语句
```

<b>实例：</b>

```
try:
    a = 3/0
except:
    print("出现除数为0")
else:
    print("a=",a)
finally:
    print("结束！")
```

## <a href="# 4.文件处理">4.文件处理</a>
涉及到文件的输出和输入等操作，需要用到文件处理机制，具体结构如下：

```
文件对象 = open（文件名,打开模式）
文件对象.close()

打开模式
-r     读取数据
-w     写入数据
-a     追加新内容
```

```
import os

def makefile(filename,message,mode):
    a = open(filename,mode)
    a.write(message)
    a.close()

def openfile(filename):
    b = open(filename,"r")
    lines = b.readlines()
    for line in lines:
        print(line)

print("a.txt")
print("-------------------------------")
makefile("a.txt","这是一个实例文档\n","a")
makefile("a.txt","hello world,这是第二行","a")
print("\n")
print("------------------------------")
openfile("a.txt")
```

## <a href="# 5.模板">5.模板</a>
调用某包或者某函数,可以是自带的，也可以是自定义的。

结构：

```
import 模板名
import 模板名,模板名
from 模板名 import 函数名/属性名
import 模板名 as 别名
```

1.模板函数modeHero.py
2.
```
weapon = ["sword","spear","bow","axe"]
power = [75,98,78,41]

def printInfor(skill,idx=0):
	name="ltc"
	age=18
	weight=100
	
	print ("\n")
	print("------------------------")
	print("name:",name)
	print("age:",age)
	print("weight",weight)
	print("weapon:",skill,"[power:",power[idx],"]")
	print(">>>i am ready to fight!")
```

2.原函数module.py

```
import  modeHero

myweapon = input("select weapon:")

i =0
for item in modeHero.weapon:
    if(item == myweapon):
        modeHero.printInfor(myweapon,i)
    i=i+1
print("----------------------------------")
print(("\n"))
```