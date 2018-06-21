# 安装Python

因为Python是解析型语言，我们在开始学习编程之前首先要安装Python解析器。

## Windows系统安装Python

**1.下载安装包**

进入Python官网 `Downloads` > 选择Windows操作系统，根据操作系统版本（32位或64位）来选择需要下载的安装包（32为选择x86，64位选择x86-64）。这里以64位系统为例，我们选择 `Windows x86-64 executable installer`。

<img src="/assets/WX20180619-225116@2x.png" width="500"/>

**2.安装Python**

双击安装程序安装

<img src="/assets/WX20180619-233735@2x.png" width="600">

注意这里的`Add Python 3.6 to PATH` 要勾选，点击`Next`

<img src="/assets/WX20180619-233922@2x.png" width="600">

这一步保持默认即可，点击`Next`

<img src="/assets/WX20180619-234331@2x.png" width="600">

最后一步 `Install` 等待安装完成

<img src="/assets/WX20180619-234811@2x.png" width="600">

安装成功后我们打开命令行模式输入`python`，当看到如下情况是说明我们安装成功了：

<img src="/assets/WX20180620-050102@2x.png" width="600">

## Max系统安装Python

在macOS系统上已经内置了Python 2.x版本，由于我们的教程是基于Python 3.x 所以我们还要安装Python 3版本，我们可以使用Homebrew或者官网安装包方式安装。

**安装方式一**

使用 Homebrew 安装 `brew install python3`，`Homebrew`是macOS平台的软件包管理器，具体安装方法参见  https://brew.sh/index_zh-cn

**安装方式二**

从Python官网下载Python3.6.4安装程序
[Python3.6.5](https://www.python.org/ftp/python/3.6.5/python-3.6.5-macosx10.6.pkg) 安装即可。


安装完成后，打开终端输入python3，出现如下结果：

<img src="/assets/WX20180620-050253@2x.png" width="600">

## Linux系统安装Python

在大多数Liunx系统中也默认内置了python 2.x版本，同样我们需要安装Python 3版本。由于Liunx系统版本众多，安装方式也各有不同，具体系统的具体安装教程不再一一细述。
 
**有些较新的操作系统内置了Python 2以及Python 3版本，我们可直接使用**

> 注意：不要去尝试删除系统原有的Python 2版本，因为一部分系统软件底层是依赖Python 2的，删除会导致未可知的错误。


* 下载源码包

在[Python](https://www.python.org/downloads/source/)官网查找系统合适的源码包，选择合适版本的源码包进行下载。

```
wget https://www.python.org/ftp/python/3.6.4/Python-3.6.4.tgz
```

* 解压源码包

```
tar -zxvf Python-3.6.4.tgz
```

* 编译安装

```
cd Python-3.6.4
./configure
make && sudo make install
```

安装完成打开终端输入 `python3.6` 出现如下结果：

```
Python 3.6.4 (default, Jun 20 2018, 04:50:40)
[GCC 4.8.5 20150623 (Red Hat 4.8.5-16)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
