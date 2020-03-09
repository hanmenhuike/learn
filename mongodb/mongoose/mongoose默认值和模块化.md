## mongoose 默认参数
在使用 model 添加项的时候如果类型不一致或者添加其他的字段名的话，都会被 mongoose 过滤掉

> // 给字段加上 default: ··· 来为字段添加默认值
> name:{
  type: String,
  default: '张三'
}

## 模块化
1. model 文件夹里面放 db.js，完成连接数据库监听的功能， 向外暴露
2. model 文件夹里面的 xxx.js，完成 Schema 的定义模型的创建 ，增删改查的实现， 向外暴露

