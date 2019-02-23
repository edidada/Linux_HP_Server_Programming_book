# 读书笔记

## Chap. 14

POSIX标准的线程库LinuxThreads

自内核2.6开始，Linux才真正提供内核级的线程支持，NGPT(2003年放弃)和NPTL(Native POSIX Thread Library)。NPL比LinuxThreads效率高，且更符合POSIX规范，所以它已经成为glibc的一部分。

POSIX线程(简称pthread)
POSIX线程同步方式：POSIX信号量、互斥锁和条件变量。

根据运行环境和调度者的身份，线程可分为内核线程和用户线程。

内核线程:用户线程=M:N

```shell
getconf GNU_LIBPTHREAD_VERSION
```

在ubuntu 16.04 TLS上得到`NPTL 2.23`

可重入函数，线程安全的函数

pthread_atfork()
确保fork调用后父进程和子进程都拥有一个清楚的锁状态。

pthread_kill()
将信号发送给指定线程



