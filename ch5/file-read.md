# 读文件


linux 与 windows 最大打开文件数

步骤

1.打开文件

```
open(path, flag[,encoding][,errors])
```
flag : r,rb,r+,w,wb,w+,a,a+,

encoding 编码方式
errors 错误处理

2.读文件内容

read()
read(10)
readline()
readlines()
seek()

try

with用法

3.关闭文件

f.close()
