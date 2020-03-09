## mongoose 预定义修饰符
mongoose 提供预定义模式修饰符，可以完成对我们增加数据进行一些格式化
lowercase uppercase trim
> name: {
  type: String,
  trim: trie
}
## mongoose 自定义修饰符
除了mongoose 内置的修饰符以外， 可以通过 get（不建议使用） 和 set（建议使用） 分别对读出读入的数据进行格式化
> set(params){
  返回处理后真正的数据
}


