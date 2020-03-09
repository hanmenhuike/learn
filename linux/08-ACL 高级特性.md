##ACL 高级特性
1. mask

用于**临时的**降低用户和组（除了所有者和其他人）对文件的权限。但是一般都是将其他人的权限用chomd全部设置为---，在设置完mask 之后的任何acl权限的修改行为都会使 mask 返回原状，所以是临时的修改。\
一般情况下，mask 是最高的那个人/组的权限，水涨船高。
```shell
# setfacl -m mask::- /home/file1
---------
# file: home/file1
# owner: root
# group: root
user::rw-
user:new:r--			#effective:---
user:tom:rw-			#effective:---
group::r--			#effective:---
group:tom:rwx			#effective:---
mask::---
other::r--
```
-----
2. default 继承

如果希望以后再一个目录下的文件/目录都能继承父级目录的权限的话，使用default（但是之后针对以后现在还是没有该权限）
```shell
// 赋予 new 用户以后再 111 下面新建的文件有rwx的权限
# setfacl -m d:u:new:rwx /111 

// 赋予 new 用户对 111 目录的 rwx 权限
// -R 是递归的意思
# setfacl -m -R u:new:rwx /111
```


