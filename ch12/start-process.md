# 启动进程实现多任务

举例 单任务现象

fork 不是跨平台 只能在liunx中使用

使用 multiprocessing 

主（父）进程

1.创建进程
2.说明进程执行任务
3.启动进程

os.getpid()
os.getppid()


## 父子进程的先后顺序

父进程的结束不能影响子进程，让父进程等待子进程结束再执行父进程

p.join()


## 全局变量在多个进程中不能共享

## 启动多个子进程


## 多进程实现一个任务


## 进程对象的封装