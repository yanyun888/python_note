# 1 程序的执行顺序
+ 一般从前往后
+ 分支结构
+ 循环结构

注意：有的语言有类似goto的语句，可以跳转到指定标签，但是Python没有

# 2 分支结构
## 2.1 概念
指一个程序的流程走向，比较像一棵树分散的树枝
## 2.2 if 语法
+ 单分支
+ 多分支

```python
score = 85
if 90 <= score <= 100:
    print("优秀")
elif 80 <= score < 90:
    print("良好")
elif 60 <= score < 80:
    print("及格")
elif 0 <= score < 60:
    print("不及格")
```
注：这部分参考C语言进行学习。
