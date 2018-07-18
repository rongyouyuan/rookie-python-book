# String(字符串)与编码

字符串是我们在Python中最常见的一种数据类型，在编写程序中有非常多的情况下我们都是在处理、使用字符串。字符串的创建非常简单，使用单引号`' '`或双引号`" "`将文本括起来即可：

```
string = "ABCDEFG"
language = 'English'
```

> 本着使用简洁明了，使用方便等目的，在Python语言的设计中不存在单独字符的概念，即便是单个字符 `a`，实际上也是以一个字符串在形式存在。

我们已经知道了创建和输出字符串，那么思考一个问题如果在一个字符串中想要输出单引号（`'`）或双引号（`"`）时，该怎么做？

我们直接打印：
```
>>> print('The dog's name is Kitty')
  File "<stdin>", line 1
    print('The dog's name is Kitty')
                   ^
SyntaxError: invalid syntax
```

直接提示语法错误，这时候就我们就要用一些特殊方法来实现：

**使用双引号或单引号**

使用双引号来包裹包含单引号的字符串，如果需要打印的字符串中要显示的是双引号则使用单引号包裹：

```
>>> print("The dog's name is Kitty")
The dog's name is Kitty

>>> print('Mother said,"How about giving a party?"')
Mother said,"How about giving a party?"
```

**使用转义字符**

字符（`'`）及（`"`）是用于定义字符串的特殊字符，程序用来区分字符串的边界，我们可以使用 `\` 将其转义为字符串使用，如：

```
>>> print('The dog\'s name is Kitty')
The dog's name is Kitty
```

## 转义字符

上面我们讲了转义字符用于处理字符创建中包含（`'`）和（`"`）的情况，使用`\'`与`\"`可以分别转义单引号和双引号。

> 转义字符的基本作用：将含有特殊意义的字符转换为字符串

除了`\'`与`\"`在Python还有以下转义字符：

<table>
        <tr>
            <th>转义字符</th>
            <th>描述</th>
        </tr>
        <tr>
            <td>\\</td>
            <td>
                反斜杠
                <code>\</code>
            </td>
        </tr>
        <tr>
            <td>\a</td>
            <td>响铃</td>
        </tr>
        <tr>
            <td>\b</td>
            <td>退格(Backspace)</td>
        </tr>
        <tr>
            <td>\e</td>
            <td>转义</td>
        </tr>
        <tr>
            <td>\000</td>
            <td>空</td>
        </tr>
        <tr>
            <td>\n</td>
            <td>换行</td>
        </tr>
        <tr>
            <td>\v</td>
            <td>纵向制表符</td>
        </tr>
        <tr>
            <td>\t</td>
            <td>横向制表符</td>
        </tr>
        <tr>
            <td>\r</td>
            <td>回车</td>
        </tr>
        <tr>
            <td>\f</td>
            <td>换页</td>
        </tr>
        <tr>
            <td>\oyy</td>
            <td>八进制数，yy代表的字符，例如：\o12代表换行</td>
        </tr>
        <tr>
            <td>\xyy</td>
            <td>十六进制数，yy代表的字符，例如：\x0a代表换行</td>
        </tr>
        <tr>
            <td>\(行尾)</td>
            <td>续行符</td>
        </tr>
        <tr>
            <td>\other</td>
            <td>其他字符已普通格式输出</td>
        </tr>
</table>

**多行字符串的定义**

当字符串有很多换行，用`\n`写在一行，阅读起来不是非常的方便：

```
str = "twinkle, twinkle, little star.\nhow i wonder what you are.\nup above the world so high.\nlike a diamond in the sky."
```

Python支持使用 `'''` 包含的字符串来定义多行：

```
>>> str = '''
twinkle, twinkle, little star.
how i wonder what you are. 
up above the world so high.
like a diamond in the sky.
'''
>>> print(str)
twinkle, twinkle, little star.
how i wonder what you are.
up above the world so high.
like a diamond in the sky.
```

##原始字符串

接下来再引出我们常遇到的一个问题，假设得到了window路径为`C:\work\puthon\ch1\test\test.py`，要输出这个字符串：

```
>>> print('C:\work\python\ch1\test\test.py')
C:\work\python\ch1	est	est.py
```
在得到的结果中发现路径`\`被当成转义字符，而且后面的字符刚好被转成了制表符，这显然不是我们要的结果。当然种情况我们也可以用`\\`去转义，那如果字符串比较长且有很多类似的地方都被转义了怎么办？

在Python的字符串创建时支持使用 **`r'字符串'`** 使字符换内部字符不会被转义：

```
>>> str = r'C:\work\python\ch1\test\test.py'
>>> print(str)
C:\work\python\ch1\test\test.py
```

## 字符串的索引

在Python中字符串是可以看作是字符的有序集合，我们可以通过其位置来获得具体的元素。字符串 **string** 实际上就是字符`s`、`t`、`r`、`i`、`n`、`g`组成的有序集合。

字符串的索引分两种正向索引和负向索引：

 * **正向索引**：从字符串左侧第一个字符以`0`为索引开始，依次到最后一位（字符个数-1）结束。
 * **负向索引**：从字符串y右侧第一个字符从`-1`为索引开始，依次到第一位（负字符个数）结束。

通过一张表格可以更清楚的帮大家理解正负向索引：

<table>
  <tr>
    <td>正向索引</td>
    <td>0</td>
    <td>1</td>
    <td>2</td>
    <td>3</td>
    <td>4</td>
    <td>5</td>
  </tr>
  <tr>
    <td>字符</td>
    <td><b>s<b/></td>
    <td><b>t<b/></td>
    <td><b>r<b/></td>
    <td><b>i<b/></td>
    <td><b>n<b/></td>
    <td><b>g<b/></td>
  </tr>
  <tr>
    <td>负向索引</td>
    <td>-6</td>
    <td>-5</td>
    <td>-4</td>
    <td>-3</td>
    <td>-2</td>
    <td>-1</td>
  </tr>
</table>

我们要访问字符串中某一个字符，就可以通过`字符串[索引值]`的形式去获取，

```
#!/usr/bin/python3

str = 'string'

# 使用正向索引获取
print(str[0])
print(str[1])
print(str[2])

# 使用负向索引获取
print(str[-3])
print(str[-2])
print(str[-1])

```
输出结果：
```
s
t
r
i
n
g
```

## 字符串的切片

既然可以通过索引值单个获取字符，那么能不能直接获取其中一部分呢？当然可以，在Python中为我们提供了切片操作（slice）来实现从字符串中精确的获取部分字符串。

>字符串的切片并不改变原字符串，而是从新创建了一个新的字符串，字符串本身不可变。

格式：`字符串[ 起始索引 : 结束索引 : 步进长度 ]`

切片的用法有下面几种：

1.`[:]` 获取字符串起始到末尾的整个字符串。

```
>>> str = 'string'
>>> print(str[:])
string

```

2.`[开始索引:]` 获取`开始索引`到字符串末尾的字符串。

```
>>> str = 'string'
>>> print(str[2:])
ring

```

3.`[:结束索引]` 获取字符串起始到`结束索引-1`的字符串。

```
>>> str = 'string'
>>> print(str[:3])
str

```
4.`[开始索引:结束索引]` 获取字符串`开始索引`到`结束索引-1`的字符串。

```
>>> str = 'string'
>>> print(str[2:4])
ri

```

5.`[开始索引:结束索引:步进长度]` 获取字符串`开始索引`到`结束索引-1`的字符串，间隔`步进长度`提取一个字符。

```
>>> str = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
>>> print(str[0:20:2])
ACEGIKMOQS

```

6.`负向索引获取字符串` 字符串的索引支持负向索引，同样字符串的切片也支持负向索引。

```
>>> str = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
>>> print(str[-10:-5])
QRSTU
>>> print(str[-5:])
VWXYZ
>>> print(str[-10:-5:2])
QSU
print(str[::3])
ADGJMPSVY
```
最后再说一个切片的神奇用法 `反转字符串`：

```
>>> str = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
>>> print(str[::-1])
ZYXWVUTSRQPONMLKJIHGFEDCBA
```
结果是原本的字符串`ABCDEFGHIJKLMNOPQRSTUVWXYZ`反转了过来，那如果把参数改成 `2` 会是啥结果呢？

```
>>> str = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
>>> print(str[::-2])
ZXVTRPNLJHFDB
```
通过和上面输出结果对比不难看出，字符串依旧被反转且步进长度从1变为了2。

## 字符串操作
### 字符串的拼接

Python中字符串的使用`+`可以完成对字符串的拼接：

```
>>> str1 = 'back'
>>> str2 = 'ground'
>>> print(str1 + str2)
background
```

### 字符串的乘法
Python中字符串的乘法作用就是将一个字符串进行乘数次重复：

```
>>> str = '*'
>>> print(str * 30)
******************************
```
### 判断字符串否包含

**`in`**

在Python中判断一个字符串是否在另一个字符串中可以使用`in`成员操作符，包含则返回`True`，不包含则返回`False`:

```
>>> str = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
>>> 'ABC' in str
True
>>> 'CBA' in str
False
```
**`not in`**

另外还有一个与 `in` 操作符相反的运算符 `not in`，包含则返回`False`，不包含则返回`True`，返回的结果与 `in` 正好相反：

```
>>> str = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
>>> 'ABC' not in str
False
>>> 'CBA' in str
True
```

## 字符串的格式化

在上文字符串操作中讲解了字符串的拼接，我们来思考一个问题，如果`name = 'Join'`、`age = 23`，如何打印出下面字符串：

```
John is 23 years old.
```

大家可能很快就想到了：

```
#!/usr/bin/python3

name = 'Join'
age = 23
str = name + ' is '+ age +' years old.'
print(str)
```
运行结果：

```
Traceback (most recent call last):
  File "/work/learn-python/string.py", line 5, in <module>
    str = name + ' is '+ age +' years old.'
TypeError: must be str, not int
```

程序提示“类型错误：必须是字符串，不能是整形”，这是为什么？其实这是因为Python语言在字符串拼接时并不会像弱类型语言将整形转换为字符串，所以只能手动进行类型转换。使用 **`str`** 函数将整形转换为字符串：

```
#!/usr/bin/python3

name = 'Join'
age = 23
str = name + ' is '+ str(age) +' years old.'
print(str)
```
再次执行程序，得到了正确的结果：

```
Join is 23 years old.
```

那如果遇到字符串很长且有很多的整形拼接，也要这样一个一个的去拼接去转换吗？其实在Python中还有两种方法来处理字符串拼接，使用更加简单并且效率更高。

**`%`百分号方式**

```
#!/usr/bin/python3

name = 'Join'
age = 23
str = '%s is %d years old.' % (name, age)
print(str)

```
运行结果：

```
Join is 23 years old.
```

首先创建需要格式化的字符串，在字符串末尾后跟 `%`，表示要对前面的字符串进行个格式化，字符串中的`%d`、`%s`我们称其为格式符，`%d`表示一个整数，`%s`表示一个字符串。`%`后面的元组（）中的内容一一对应前面格式符中真实的值，当需要替换的格式符只有一个时，也可省略掉（）直接后跟替换值。


以上我们介绍了`%`格式化的简单用法，其实它还支持更高级的用法，在日常开发中我们只要掌握常用的格式符`%s`、`%d`、`%f`就可以了，其它的怎么办？当然是现用现查啊！

格式符的通用格式：

```
%[(name)][flags][.precision]typecode
```

* (name)：可选值，当 `%` 后跟字典对象时，对应字典的key
* flags：可选值，提供的选择值有以下几种：
    * `+` 右对齐，正数前加正号，负数前加负号
    * `-` 左对齐，正数前无符号，负数前加负号
    * `空格` 右对齐，正数前加空格，负数前加负号
    * `0` 右对齐，正数前无符号，负数前加负号，用0填充空白处
* width：可选值，占用宽度
* .precision： 可选值，小数点后保留的位数
* typecode：必选值，下面是常用的格式符：
    * `%` 当字符串中存在`%`字符时，需要用 %%表示一个百分号
    * `c` 字符及其ASCII码
    * `s` 字符串
    * `d` 有符号整数(十进制)
    * `u` 无符号整数(十进制)
    * `o` 无符号整数(八进制)
    * `x` 无符号整数(十六进制)
    * `X` 无符号整数(十六进制大写字符)
    * `e` 浮点数字(科学计数法)
    * `E` 浮点数字(科学计数法，用E代替e)
    * `f` 浮点数字(用小数点符号)
    * `g` 浮点数字(根据值的大小采用%e或%f)
    * `G` 浮点数字(类似于%g)

示例用法：

```
#!/usr/bin/python3

str1 = '%s is %d years old' % ('Tom', 22)
str2 = '%(name)s is %(age)d years old' % {"name":"Tom", "age": 22}
str3 = 'The value of PI is %.2f' % 3.141592654
str4 = 'The percent is %.2f%%' % 92.1098
print(str1)
print(str2)
print(str3)
print(str4)
```
运行结果：

```
Tom is 22 years old
Tom is 22 years old
The value of PI is 3.14
The percent is 92.11%

```

**`str.format`方法**

自Python 2.6开始，在字符串对象中增加了format函数，提供了更高级字符串格式化功能。见[PEP-3101](https://www.python.org/dev/peps/pep-3101/)。

> PEP :PEP是Python Enhancement Proposals的缩写。一个PEP是一份为Python社区提供各种增强功能的技术规格，也是提交新特性，以便让社区指出问题，精确化技术文档的提案。详情见
[PEP列表](https://www.python.org/dev/peps/)。

与百分号方法使用不同的是，format方法的字符串中使用`{}`、`:`代替了原来`%*`格式符，使用方式也更加灵活了许多，用法：


1.按照位置参数：

```
>>> '{} is {} years old'.format('Tom', 22)
```
> 在Python 2.6中`{}`中是不能为空的，这种写法在Python 2.7+才被支持

```
'Tom is 22 years old'
>>> '{0} is {1} years old'.format('Tom', 22)
'Tom is 22 years old'
>>> '{0} {1} {0}'.format('well','is') #位置参数是可以被复用的
'well is well'

```

2.按照参数名称：

```
>>> '{name} is {age} years old'.format(name='Tom', age=25)
'Tom is 25 years old'
>>> '{name} is {age} years old'.format(age=22, name='John') #参数顺序是可以更换的
'John is 22 years old'
>>>
```

3.按照索引:

```
>>> arguments = ['Tome', 22]
>>> '{0[0]} is {0[1]} years old'.format(arguments)
'Tome is 22 years old'
>>>
```

##字符串编码

既然讲到了字符串就不得不说说Python的字符串编码。我们知道计算机只能处理数字，想要处理字符则必须通过一定的规则将其转换成数字才可以，于是就有了ASCII码的诞生。

计算机的最小单位是位，称为比特 ‘b’，也就是0或1，一个0或者1代表了1位。通常情况下8比特 = 1字节，所以一字节能表示的最大整数为255`二进制（11111111） = 十进制（255）`。

ASCII编码由8比特表示一个字符，也就是：00000000——11111111，大小范围限定好了，然后指定了一套规则，如下:

<img src="/assets/29018063_1459329934mhE8.png" />

我们知道计算机是美国人发明的，这些字符基本满足了计算机的使用，中国已知汉字有数万之多，想要用一个字节肯定是不能表示完整的。为了支持更多的中文字符，于是GB2312、GB2312或GB2312-80、GBK各种编码规则和字符集便应运而生，同样其他国家也都发明了对应自己语言的编码规则和字符集。

但是当众多的字符集出现在网络中传输时，便由于各种字符集不相同和冲突问题出现了乱码现象。于是乎国际标谁化组织重新搞一个包含所有语言的**Unicode**编码，从而解决了乱码问题。

但是由于Unicode编码的特性，一个字符通常用两个字节来表示:


|字符|ASCII|Unicode|
|:---|:---|:---|
|A|01000001|00000000 01000001|
|中| × |01001110 00101101|


那么就有了新的问题：当需要处理的文本为英文时，所占的空间比普通ASCII码要多一倍，这在存储和数据传输中存在的极大的浪费，于是 **UTF-8** 编码便由此诞生了，**UTF-8** 编码是一种变长编码，根据Unicode字符的不同而变化字节长度，常用的英文字母被编码成1个字节，汉字通常是3个字节，只有很生僻的字符才会被编码成4-6个字节。

|字符|ASCII|UTF-8|
|:---|:---|:---|
|A|01000001|01000001|
|中| × |11100100 10111000 10101101|

> `Unicode`是一种编码规范，`UTF-8`是Unicode的实现标准。

你可能注意到了UTF-8编码在处理一个字节长度的字符与ASCII编码是一致的，所以也可以认为UTF-8编码是ASCII编码的超集。

在Python3中字符串的存储是Unicode编码的，所以完全支持中文的，而Python源文件中使用的是默认`utf-8`编码。

```
>>> str = "我爱你中国"
>>> print(str)
我爱你中国
>>>
```


使用 `ord()` 将字符转换为ASCII码值
```
>>> ord('a')
97
>>>
```

使用 `chr()` 将ASCII码转换为字符
```
>>> chr(98)
'b'
>>>

```

使用字符串的encode方法编码为`bytes`

```
>>> str = "中文字符串"
>>> str.encode()
b'\xe4\xb8\xad\xe6\x96\x87\xe5\xad\x97\xe7\xac\xa6\xe4\xb8\xb2'
>>>
```

使用`bytes`的decode方法解码为字符串

```
>>> bytes = b'\xe4\xb8\xad\xe6\x96\x87\xe5\xad\x97\xe7\xac\xa6\xe4\xb8\xb2'
>>> bytes.decode('utf-8')
'中文字符串'
>>>

```

## 字符串函数

eval 将字符串当成有效的表达式来执行


print(eval("+12"))
print(eval("-23"))
print(eval("1+2"))
print(eval("3-1"))

len(str)

str.lower()

str.upper()

str.swapcase()

str.capitalize()

str.title()

center(witdh, fillchar)

ljust(width, [fillchat])

rjust(width, [fillchat])

##返回一个长度为width 的字符串，原字符串右对其 前补0
zfill(width)

count(str, [\,start][\,end])

# 检测 是否包含的字符串 注意返回值 下标 找不到返回 -1
find(str,[\,start][\,end])

rfind

index 

rindex

lstrip

rstrip

strip 

字符串大小的比较
