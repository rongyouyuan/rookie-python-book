# list与tuple

##list(列表)

举例 求五个人的平均年龄

```
age1 = 10
age2 = 10
age3 = 10

(age1 + age2 + age3) / 3

```

如果要处理100个人的平均年龄呢？

列表的本质：一种**有序**的集合

创建列表

列表 = [列表选项1，列表选项2，列表选项3]

```
list = [] #空列表
list2 = [18,19,20,21,22] #带有元素的列表
```
列表中的元素可以是不同类型

##列表元素的访问 

举例
```
list2 = [18,19,20,21,2

while index < 5
    sum += list2[index]
    if index == 5
        print('平均年龄')

```

1 取值
list[index]
2 替换
list[index] = x

##列表操作
* 列表相加
list1 + list2


##列表的重复

list1 * 3

##判断元素是否在列表中

3 in list1


##列表截取

使用切片


##二维列表

list = [[12,3],[3,8]]

##列表方法

list.append(6)
list.append([7,8,9])

list.extend([7,8,9])


list.insert(2,100)
list.insert(2,[100])


list.pop //带返回值

list.remove()

clear 清除所有数据

list.index(5)

## 列表个数

len()

min()

count() //出现次数

list 倒序 reverse()

sort() 排序

拷贝 浅层拷贝 深层拷贝

```
找出第二大的值
```


## 元组

定义元组 元组不可变 (1,2,3,[3,4,5])

(1,)

元素元组的访问 元组名[下标]

修改元组

删除元组

元组的操作

+
*
in

元组遍历

与字符串关联

split

splitlines

join

max

min

replace

创建字符换映射表 maketrans

startswith

endwidth

encode

isalpha

isalumn

isupper

islower

isdigit

isnumeric

isdecimal

isspace
