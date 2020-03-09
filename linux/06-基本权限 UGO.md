## linux 基本权限
**Linux 中用户打开进程， 进程访问文件， 访问时文件权限会判断进程用户是够格**

权限对象：
* 拥有者： u
* 所属组： g
* 其他人： o

权限类型：
* 读（r）：4
* 写（w）：2
* 执行（x）：1

```shell
// 权限 所属者 所属组 大小 最后修改时间 文件名

# ll yum.conf 
-rw-r--r--. 1 root root 1037 Aug 15  2019 yum.conf
```
---
设置权限：
1. 更改所属者和所属组
```shell
-> chown
// 更改所属者 写左边
# ll 2020-02-11_file.txt 
-rw-r--r-- 1 new root 35 Feb 18 16:48 2020-02-11_file.txt 
# chown root 2020-02-11_file.txt 
# ll 2020-02-11_file.txt 
-rw-r--r-- 1 root root 35 Feb 18 16:48 2020-02-11_file.txt

// 更改所属组 写右边
# chown .new 2020-02-11_file.txt
-rw-r--r-- 1 root new 35 Feb 18 16:48 2020-02-11_file.txt

// 同时改 两边都写
# chown new.new 2020-02-11_file.txt
```
```shell
-> chgrp(推荐上一个命令)
// 更改所属组
# chgrp root 2020-02-11_file.txt
-rw-r--r-- 1 root root 35 Feb 18 16:48 2020-02-11_file.txt
```
2. 更改权限
```shell
-> chmod
-> 语法： chomd + (ugoa) + (+-=（覆盖）) + 文件

```