
## 安装
> npm i mongoose --save
## 引入 连接
> const mongoose = require('mongoose')
> mongoose.connect('mongodb://localhost/test')

**注意：有账号密码的话需要在localhost前面添加 账户名：密码@**
## 定义 Schema
每个 schema 都会映射到 mongodb 中的一个 collection 
> const schema = mongoose.Schema({···})

**Schema 内的内容要和数据库表的内容一一对应，因此 Schema 的作用在于统一输入输出的数据格式**
## 创建 model
> // arg1 是模型名字， arg2 是定义的schema对象
> let model = mongoose.model('model name', schema)

**注意：model两个参数的时候默认操作的是 arg1 的复数名表， 三个参数的时候操作的是 arg3 指定的表**

## 增
1. 实例化 model
2. 实例.save()
## 新
 模型.updateOne(arg1, arg2, arg3) 
  * arg1 查找条件
  * arg2 修改内容
  * arg3 回调函数
## 删
 模型.deleteOne(arg1, arg2)
  * arg1 查找条件
  * arg2 回调函数
## 查
 模型.find(arg1, arg2)
  * arg1 查找条件
  * arg2 回调函数
