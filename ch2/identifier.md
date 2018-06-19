# 标识符

##什么是标识符

>编程对变量、函数、常量等进行定义时使用的名字统称为标识符

##标识符的规则

**标示符由字母、下划线和数字组成，且数字不能开头**

正确示例：

```
myName
treeObject
user_age
_class_name
```

错误的示例：

```
#不能以数字开头
2test
#不能出现特殊字符#
user#cellphone
book(name)
```

**标识符区分大小写**

与大部分的语言一样，Python是严格区分大小写的

`变量 age 不等于 Age`

**标识符不能与关键字同名**

>关键字即为Python语言内部已经使用的标识符，不允许开发者使用相同的名字作为标识符

Python关键字列表

<table>
    <tr>
        <td>False</td>
        <td>None</td>
        <td>True</td>
        <td>and</td>
        <td>as</td>
        <td>assert</td>
    </tr>
    <tr>
        <td>break</td>
        <td>class</td>
        <td>continue</td>
        <td>def</td>
        <td>del</td>
        <td>elif</td>
    </tr>
    <tr>
        <td>else</td>
        <td>except</td>
        <td>finally</td>
        <td>for</td>
        <td>from</td>
        <td>global</td>
    </tr>
    <tr>
        <td>if</td>
        <td>import</td>
        <td>in</td>
        <td>is</td>
        <td>lambda</td>
        <td>nonlocal</td>
    </tr>
    <tr>
        <td>not</td>
        <td>or</td>
        <td>pass</td>
        <td>raise</td>
        <td>return</td>
        <td>try</td>
    </tr>
    <tr>
        <td>while</td>
        <td>with</td>
        <td>yield</td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>

当工作中需要时，我们也可以通过keyword模块来获取Python的关键字

```
>>> import keyword
>>> keyword.kwlist
['False', 'None', 'True', 'and', 'as',
 'assert', 'break', 'class', 'continue', 'def',
 'del', 'elif', 'else', 'except', 'finally',
 'for', 'from', 'global', 'if', 'import',
 'in','is', 'lambda', 'nonlocal', 'not',
 'or','pass', 'raise', 'return', 'try',
 'while','with', 'yield']
```

判断字符是否为关键字

```
>>> keyword.iskeyword('global')
True
```

##标识符使用的约定

**驼峰命名法**

小驼峰式命名法（lower camel case）： 第一个单词以小写字母开始；第二个单词的首字母大写，例如：userAge、errorCode

大驼峰式命名法（upper camel case）： 每一个单字的首字母都采用大写字母，例如：FirstName、UserCellphone

根据不同公司的规定或个人的喜好选择合适的命名法即可。

**见名知意**

程序的标识符尽量使用有意义的名字，如：`book`,`userCellphone`,`studentAge` 从字面意思上很容易理解为 “书”，“用户手机号码”，“学生年龄”

**下划线的使用**

在Python中使用了一些下划线及双下划线定义的特殊方法或常量，在类的使用中单下划线开头`_`的成员变量表示保护变量，以双下划线开头结尾的用于表示Python中的特殊方法，例如`__init()__`代表类的构造函数，我们要尽可能的避免这样使用。

```
_name = "Mr Rong"
test_ = "Python"
```
虽然合法但是并不提倡这样使用

**不要使用内置函数名或内置数据类型或异常名作为标识符名**

举个例子，sum() 函数用于计算求和我们将其作为标识符去使用：

```
>>> sum([1,2,3])
6
>>> sum = "nothing"
>>> sum([1,2,3])
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object is not callable
>>>
```

结果是我们看到sum 函数被赋值为字符串“nothing”，当我们再次使用的时候发现已经无效了。
