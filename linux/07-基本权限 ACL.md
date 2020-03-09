# 基本权限 ACL

```shell
-> getfacl
# getfacl 2020-02-11_file.txt

# file: 2020-02-11_file.txt
# owner: root
# group: root
user::rw-
group::r--
other::r--
```
```shell
-> setfacl
-> 语法： setfacl -m （u/g）:（用户/组）:权限 文件

# setfacl  -m u:new:rw- 2020-02-11_file.txt 
---------
# file: 2020-02-11_file.txt
# owner: root
# group: root
user::rw-
user:new:rw-
group::r--
mask::rw-
other::r--
--------------------------------
# setfacl -m u:new:- test.txt //权限设置为---
# setfacl -x u:new test.txt // 删除new的权限
# setfacl -b test.txt // 删除所有的权限
# getfacl file1 | setfacl --set-file=- file2 // 将一个文件的权限复制到另外一个文件身上
```

