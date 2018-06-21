# 第一个Python程序

## Hello World

惯例上，学习一门新语言时写的第一个程序都是 `Hello World`，但是在开始第一个Python之前我们先要了解一下交互模式。

想要输出第一行代码，首先要进入交互模式：

+ Window系统开始菜单中打开`命令提示符`，在命令行模式输入`python`，回车即可

+ Mac及Linux中在终端入`python3` ，回车即可

会看到窗口中显示大致如下内容:

```
Python 3.6.4 (default, Jan  6 2018, 11:51:15)
[GCC 4.2.1 Compatible Apple LLVM 9.0.0 (clang-900.0.39.2)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>

```

当看到符号`>>>`出现在屏幕时表示已经进入了交互模式，在等待用户输入数据，想要退出时输入`exit()`或者`quit()`回车即可。

我们输入`200`回车：

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

`print` 函数用于打印出指定的文字，注意这里需要将要输出的文字用单引号或者双引号括起来，下面我们来输出一段文字“Hello World":

```
>>> print('Hello, World!')
Hello, World!
```

恭喜你完成了Python的第一行代码！

## 使用开发工具

通常交互模式一般用来做调试和排错，输入的代码并不会保存，在交互模式关闭后，随即消失，所以在程序开发中过程中还需要借助Python开发工具进行脚本编辑。

这里推荐给大家两款Python开发工具：

1.`Sublime Text` 一款强大的文本编辑器，支持非常多的优秀插件，可免费使用。

<img src="/assets/WX20180621-030827@2x.png" width="600">

2.`PyCharm` Python IDE集成开发环境，有社区免费版。

<img src="/assets/WX20180621-034102@2x.png" width="600">

以`Sublime Text`为例，点击`File` > `New File` 创建一个新的名为`hello.py`文件，输入`print('Hello, World!')` 并保存：

```
print('Hello, World!')
```
然后我们在终端模式中执行 `python3 hello.py`，我们得到了与交互模式一样的效果：

```
/workplace/learn-python python3 hello.py
Hello, World!
```
