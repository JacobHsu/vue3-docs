# GOF23种设计模式

通过vue来了解一下GOF.
GOF是设计模式的经典名著《设计模式——可复用面向对象软件的基础》，在书本总结了23个设计模式。罗列一下哪些设计模式是我们见过的。

## 单例（Singleton）模式

定义：某个类只能生成一个实例，该类提供了一个全局访问点供外部获取该实例，其拓展是有限多例模式。(创建型)
例子：`Vuex` 保证唯一 Store，以及单例组件

## 工厂（Factory Method）模式

定义：一个用于创建产品的接口，由子类决定生产什么产品。 (创建型)
例子：将new操作单独封装，遇到`new`时，就要考虑是否该用工厂模式。 在组件中传入实参，返回出不同的组件**

## 抽象工厂（Abstract Factory）模式

定义：提供一个创建产品族的接口，其每个子类可以生产一系列相关的产品。 (创建型)
例子：
比如说有个案例有不同的订单状态对应不同的操作按钮。我们是不是一般会写出如下的代码

```js
switch (status){ case '待付款': setState({status:1}) break;
```

如果我们把订单状态的一些判断与业务代码掺杂在一块，不利于我们做扩展和复用。那对比一下下面的代码

```js
 export default class OrderStatusFactory { createStatusObjWith (status) { let obj = undifined switch (status) { case '待付款': obj = new StatusWaitToPay() break; case '待发货': obj = new StatusWaitToShip() break; ... } return obj } 
```

## 组合（Composite）模式

定义：将对象组合成树状层次结构，使用户对单个对象和组合对象具有一致的访问性。 (结构型)
例子：组件

组合模式给我们的启示，组件接口设计三原则

1. 保持接口小，props 数量要少
2. 根据数据边界来划分组件，利用组合（composition）
3. 把 state 尽量往上层组件提取

同时，我们也接触了这样一些最佳实践：

1. 避免 renderXXXX 函数，直接使用独立的纯函数组件
2. 给回调函数类型的 props 加统一前缀，比如 on 或者 handle
3. 使用 propTypes 来定义组件的 props

## 观察者（Observer）模式

定义：当一个变量值被修改时，可以自动通知所有关注这个变量的其他对象，自动重新更新获取这个变量的新值 (行为型)
例子：vue的双向监听就是基于观察者模式实现的
