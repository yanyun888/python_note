# 1 输入
## 1.1 Python2
### 1.1.1 raw_input
+ 格式：result = raw_input("提示信息")
+ 功能：等待用户输入内容，直到用户按下Enter，会将用户输入的内容当做"字符串"，传递给接收的变量
### 1.1.2 input
+ 格式：result = input("提示信息")
+ 功能：会等待用户输入内容，直到用户按下Enter，会将用户输入的内容当做"代码"进行处理，可以理解为 input = raw_input + eval
## 1.2 Python3
### 1.2.1 input
+ 格式：result = input("提示信息")
+ 功能：等待用户输入内容，直到用户按下Enter，会将用户输入的内容当做"字符串"，传递给接收的变量

**注意**：如果想要实现Python2中的input功能，可以再使用eval()函数

# 2 输出
## 2.1 Python2
使用print语句
```
print xxx
```
## 2.2 Python3 
使用print函数
```
print(values,sep,end,file,flush)
```
+ values : 需要输出的值，多个值，使用"，"进行分割
+ sep : 分割符，多个值，被输出出来之后，值和值之间，会添加指定的分隔符
+ end : 输出完毕之后，以指定的字符结束，默认是换行'\n'
+ file : 表示输出的目标，默认是标准的输出(控制台) file = sys.stdout,可以是一个可写入的文件句柄
+ flush : 表示立即输出，值为Bool类型，默认False

## 2.3 使用场景
### 2.3.1 输出一个值
+ Python2 print 值
+ Python3 print(值)
### 2.3.2 输出一个变量
+ Python2 print 变量名
+ Python3 print(变量名)
### 2.3.3 输出多个变量
+ Python2 print 变量名1,变量名2
+ Python3 print(变量名1,变量名2)
### 2.3.4 格式化输出
a. Python2

**写法**
```
  print "随意内容...占位符1, ... , 占位符2, ..."%占位符要放的值
  print "随意内容...占位符1, ... , 占位符2, ..."%(变量1, 变量2)
```
 **format写法**
```
  print "随意内容...{索引}, ... , {索引}, ...".format(值1, 值2)
```
b. Python3

**写法**
```
  print("随意内容...占位符1... "%占位符要放的值)
  print("随意内容...占位符1, ... , 占位符2, ..."%(变量1, 变量2))
```
 **format写法**
```
  print("随意内容...{索引}, ... , {索引}, ...".format(值1, 值2))
```
例：
```python2
# coding=utf-8

name = "xiaoming"
age = 18

# 我的名字是xxx, 年龄是xxx
print "我的名字是", name, ", 年龄是", age

newStr = "我的名字是%s, 年龄是%d"%(name, age)

#print newStr

print "我的名字是{1}, 年龄是{0}".format(age,name)
```

```python3
name = 'yanyun'
age = 18
# 我的名字是xxx, 年龄是xxx
print("我的名字是%s, 年龄是%d"%(name, age))
print("我的名字是{0}, 年龄是{1}".format(name, age))
# 输出不自动换行
print("abc", end="")
# 输出的各个数据, 使用分隔符分割
print("1", "2", "3", sep="&&&&&")
```
**注意**：Python中的格式化输出注意参考C语言。