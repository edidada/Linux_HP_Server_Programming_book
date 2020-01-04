# Linux_HP_Server_Programming

《Linux高性能服务器编程》书籍源码
CMake组织

# Linux_HP_Server_Programming

## Chap.6


6.5 mmap()函数和munmap()函数

- mmap()申请内存
- munmap()释放内存

6.8 fcntl函数
跟iocntl比较
fcntl是POSIX规范


# Chap.7 Linux服务器程序规范

- Linux服务器程序一般以后台进程的形式运行。后台进程又称为守护进程(daemon)。它没有控制终端，因而也不会意外接收到用户输入。守护进程的父进程通常是init进程（PID为1的进程）。
- Linux服务器程序通常有一套日志系统，它至少能输出日志到文件，有的高级服务器还能输出日志到专门的UDP服务器。大部分后台进程都在/var/log目录下拥有自己的日志目录。
- Linux服务器程序一般以某个专门的非root身份运行。比如musqld、httpd、syslogd等后台进程，分别拥有自己的运行账户mysql apache和syslog。
- Linux服务器通常是可配置的
- Linux服务器进程通常会在启动的时候生成一个PID文件并存入/var/run目录中，以记录该后台进程的PID.
- Linux服务器程序通常需要考虑系统资源和限制，以预测自身的负荷，比如进程可用文件描述符总数和内存总量等.


### Chap.7.1
Linux提供一个守护进程来处理日志系统-syslogd，Linux上使用的是它的升级版-rsyslogd。

rsyslogd，内核日志，用户日志

Linux的系统日志体系


```c

#include <syslog.h>
void syslog(int priority, const char* message, ...);

#include <syslog.h>
void openlog( const char * ident, int logopt, int facility);

#include <syslog.h>
void closelog();

```

### Chap.7.2

### Chap.7.3

查看进程关系


### Chap.7.4
系统资源限制
getrlimit
setrlimit

struct rlimit


### Chap.7.5 改变工作目录和根目录

```c
#include <unistd.h>

char* getcwd( char* buf, size_t size);
int chdir( const char* path);
int chroot( const char* path);
```
chroot()改变进程根目录的函数


### Chap. 8

高性能服务器程序框架

服务器解构为
- I/O处理单元
- 逻辑单元
- （网络）存储单元

### Chap. 8.1

服务器模型
c/s模型
p2p模型

### Chap. 9

系统调用

9.1

select poll epoll

```c

#include <sys/select.h>
/* According to earlier standards */
#include <sys/time.h>
#include <sys/types.h>
#include <unistd.h>
int select(int nfds, fd_set *readfds, fd_set *writefds, fd_set *exceptfds, struct timeval *timeout);

```





14-3thread_atfork
[对‘pthread_create’未定义的引用 clion](https://blog.csdn.net/yyyerica/article/details/70169102)

17.1 tcpdump

17.2 lsof

17.3 nc

17.4 strace

17.5 netstat

17.6 vmstat

ifstat

mpstat


