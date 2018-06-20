# 第一个Python程序

## Hello World

国际惯例，我们让程序来输出: `Hello World`

想要输出第一行代码，我们首先要进入交互模式。
  * 在Window系统中在命令行模式中输入`python` 即可
  * Mac及Linux中在终端入`python3` 即可

我们会看到类似如下界面:

```
Python 3.6.4 (default, Jan  6 2018, 11:51:15)
[GCC 4.2.1 Compatible Apple LLVM 9.0.0 (clang-900.0.39.2)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>

```

当我们看到符号`>>>`出现在屏幕时表示已经进入了交互模式，在等待用户输入数据，想要退出时输入`exit()`回车即可。

我们输入`200`，回车：

```
>>> 200
200
```
屏幕直接将`200`输出到了屏幕，再输入`200 + 1`回车:

```
>>> 200 + 1
201
```
Python直接将计算结果201展示了出来。

`print` 函数用于打印出指定的文字，注意这里需要将要输出的文字用单引号或者双引号括起来，下面我们来输出一段文字“Hello World":

```
>>> print("Hello World")
Hello World
```

恭喜你完成了第一行代码！
