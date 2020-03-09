## 普通用户提权
1. su - 
2. sudo 

```shell
//需要在创建用户的时候将用户添加到 wheel(10) 组中才能使用
# useradd new1 -G wheel
```