# input与ouput

## print

我们在第一章[第一个Python程序](/ch1/first-program.md)中已经介绍了`print`函数，下面来详细说一下print的一些用法。


print函数可以接收多个字符串，使用 “,” 进行分割，“,”会以空格的形式表现出来。

```
>>> print("Hello World", "Life is short", "You need Python")
Hello World Life is short You need Python
>>>
```

上面我们知道了print可以将字符换输出到屏幕，让我们来尝试一下数字：
```
>>> print(10)
10
>>> print(10 + 2)
12
```

我们看到print函数直接将10+2的结果输出到了屏幕，举一反三我们还可以打印一个简单的算式：
```
>>> print("10 + 1 =", 11)
10 + 1 = 11
>>>
```

print函数的用法远不止这些，后期我们讲到的各种类型的数据都可以进行输出、print函数将贯穿几乎整个教程，一些用法我们会到实际用到时向大家详细说明。

## input

在与程序的交互中我们不仅要接收到程序发送给我们的数据，我们还要将数据发送给程序进行处理。
例如：我们想让程序接收一个字符串"Python"并将其输出，那么就需要用到了 `input()` 函数，通过一个简单的示例了解一下input的使用：

```
>>> language = input()
Python
>>> print(language)
Python
```

当执行到第一句的时候，我们发现程序没有任何返回值并且光标处于输入框的最前端，这个时候我们输入“Python”并回车，我们发现“Python”被输出到了屏幕上，这时候input函数获取的值就被赋值到变量language上，我们再执行print(language)，我们发现输出的结果为“Python”。这里提到了`变量`，我们会在第二章[变量与常量]中详细解析。


input函数支持填写 `提示信息` 以便于更方便的进行交互，例：

```
>>> age = input("请输入您的年龄：")
28
>>> print("您的年龄是：", age)
您的年龄是：28
```
