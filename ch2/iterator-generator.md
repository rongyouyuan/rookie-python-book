# 迭代器与生成器

##

可迭代对象 ： 可以作用于for 循环的对象 称为可迭代对象 （Iterable）

使用 isinstance update方法判断是否为可迭代对象

有哪些呢？

1.集合数据类型 list tuple dict set string
2.generator b包含 生成器


```
form collection form Iterable

```

##迭代器 

不仅for 可以被next不断调用 返回下一个值 最后抛出一个错误 stopIterable


Iterator



list 转 Iterator