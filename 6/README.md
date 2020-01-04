# testdup


```shell

assert
断言

```

```c

extern int dup (int __fd)

```

标准输出重定向

CGI服务器的基本工作原理


# testsendfile


```shell
./cmake-build-debug/testsendfile 192.168.31.104 11111111 ../abc.txt
```


```c
ssize_t sendfile (int __out_fd, int __in_fd, off_t *__offset, size_t __count)
```


# oobsend

```shell

oobsend/cmake-build-debug/oobsend 192.168.58.3 54321

```

ssize_t splice (int __fdin, __off64_t *__offin, int __fdout, __off64_t *__offout, size_t __len, unsigned int __flags);
在两个文件描述符之间移动数据


# oobsend

```shell

oobsend/cmake-build-debug/oobsend 192.168.58.3 54321

```

ssize_t tee (int __fdin, int __fdout, size_t __len, unsigned int __flags)

在两个管道描述符之间移动数据


# oobsend

```shell

oobsend/cmake-build-debug/oobsend 192.168.58.3 54321

```

c 关键词

```c

extern

```


```c

sockaddr_in 结构体
stat 结构体

```


```c

bzero 函数

readv 

writev 

iovec 

int socket (int __domain, int __type, int __protocol)

int bind (int __fd, __CONST_SOCKADDR_ARG __addr, socklen_t __len)

int listen (int __fd, int __n)

int open (const char *__file, int __oflag, ...)

ssize_t read (int __fd, void *__buf, size_t __nbytes)

ssize_t send (int __fd, const void *__buf, size_t __n, int __flags)

int close (int __fd)

```

- sockaddr_in.sa_family_t
- AF_INET
- inet_pton
- sockaddr_in.sin_addr
- sockaddr_in.sin_port
- assert


数据类型：
socklen_t


[bzero函数](https://blog.csdn.net/weixin_42235488/article/details/80589583)
bzero函数
函数原型:void bzero（void *s, int n）;
头文件:#include <string.h>
功能:将字符串s的前n个字节置为0,一般来说n通常取sizeof(s),将整块空间清零.

[stat 结构体 st_mode 字段](https://blog.csdn.net/q1007729991/article/details/53377074)

[linux c学习笔记----文件的创建与读写(open,read,write)](https://lobert.iteye.com/blog/1705861)


linux c O_RDONLY
S_ISDIR
S_IROTH

备注：
memset函数
函数原型：void *memset(void *s,int c,size_t n)；
头文件：#include <string.h> 或者#include <memory.h>
说明：将s中前n个字节替换为c并返回s


