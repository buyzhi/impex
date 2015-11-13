# Change Log
## Version 0.3.0 - 2015/11/12
### 新增
* {{=CONTENT}}模版指令，用于引用组件内部内容
* {{=BINDPROPS}}模版指令，用于引用组件上所有属性
* impex.ext.directives 新增事件指令

### 更新
* 组件onDisplay调用时机
* 组件模版支持多个顶级节点作为视图
* 延迟x-each/-start指令获取数据源的时间，这样可以让父组件在onInit中修改each的数据源
* 现在所有指令共享一个View对象
* 增加扫描器效率

### bug修复
* 组件事件handler调用时丢失context的问题
* 部分组件创建时没有触发onCreate回调
* 修正watch匹配算法以及回调参数错误
* 无法修改input的value问题
* 内部工具错误

### 移除(重要!)
* 不再支持{{=tagBody}}模版标签，但，请看新增部分
* 核心包不再支持事件指令

## Version 0.2.0 - 2015/11/6
### 新增
* Component.findD查询指令接口
* Component.suspend挂起接口
* each performance demo，可以查看each的性能细节 

### 更新
* each指令算法，大幅提升each性能
* Component.find查询组件接口，支持*通配符
* 监控算法，优化模型响应流程

### bug修复
* 当watch一个数组时，数组内容变化后Component.watch回调参数错误
* IE8兼容相关


## Version 0.1.5 - 2015/11/4
### 新增
* 指令扩展
* x-each-start/end指令，用于段落循环
* 增加多个demo

### 更新
* 核心库不在支持x-bind指令
* 增强的x-bind指令
* 组件模版现在可以加载多个顶级元素


## Version 0.1.4 - 2015/10/30
### 新增
* ie8扩展

### 更新
* 部分对ie8的支持

### bug修复
* 监控对象没有释放
* IE observe监控死循环


## Version 0.1.3 - 2015/10/29
### 新增
* new examples
* 支持表达式中使用this关键字
* 组件模版可以使用{{=属性}}表达式来替换模版内容

### 更新
* impex.render入口的匿名组件也可以注入服务了

### bug修复
* Component.init重复执行报错的bug
* impex.render入口的匿名组件没有触发onCreate事件