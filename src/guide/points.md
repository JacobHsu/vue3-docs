# 知识点

::: tip 提示
知识点是知识中的最小单位，最具体的内容，有些情况也叫“考点”。
:::

## 为什么说Vue是一个渐进式框架？

渐进式：通俗点讲就是，你想用啥你就用啥，不强求。你想用component就用，不用也行，你想用vuex就用，不用也可以

## Vue的优点？Vue的缺点？

优点：渐进式，组件化，轻量级，虚拟dom，响应式，单页面路由，数据与视图分开

缺点：单页面不利于seo，不支持IE8以下，首屏加载时间长

## Vue跟React的异同点？

相同点：

1.都使用了虚拟dom  
2.组件化开发  
3.都是单向数据流(父子组件之间，不建议子修改父传下来的数据)  
4.都支持服务端渲染  

不同点：

1.React的JSX，Vue的template  
2.数据变化，React手动(setState)，Vue自动(初始化已响应式处理，Object.defineProperty)  
3.React单向绑定，Vue双向绑定 (react要實現需要通過state)  
4.React的Redux，Vue的Vuex  

## MVVM是什么？

![Alt MVVM](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/aac31b27392b4b0e90ca2f67c64c59c2~tplv-k3u1fbpfcp-watermark.image)

MVVM

* `VM`：也就是View-Model，做了两件事达到了数据的双向绑定  
一是将【模型】转化成【视图】，即将后端传递的数据转化成所看到的页面。  
实现的方式是：`数据绑定`。 (Model->View)  
二是将【视图】转化成【模型】，即将所看到的页面转化成后端的数据。  
实现的方式是：`DOM 事件监听`。 (View->Model)  

* 思想：实现了 View 和 Model 的自动同步，也就是当 Model 的属性改变时，我们不用再自己手动操作 Dom 元素，来改变 View 的显示，而是改变属性后该属性对应 View 层显示会自动改变（对应Vue数据驱动的思想）

### Vue是不是MVVM框架？

Vue是MVVM框架，但是不是严格符合MVVM，因为MVVM规定Model和View不能直接通信，而Vue的`ref`可以做到这点

## MVVM和MVC有何区别呢？

MVC

* Model(模型)：负责从数据库中取数据  
* View(视图)：负责展示数据的地方  
* Controller(控制器)：用户交互的地方，例如点击事件等等  
思想：Controller将Model的数据展示在View上

![Alt MVC](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/4636ebbfa25049179c27a6b5ab8bb308~tplv-k3u1fbpfcp-watermark.image)

MVVM 比 MVC 精简很多，不仅简化了业务与界面的依赖，还解决了数据频繁更新的问题，不用再用选择器操作 DOM 元素。

在 MVVM 中，View 不知道 Model 的存在，Model 和 ViewModel 也观察不到 View，这种低耦合模式提高代码的可重用性

## Vue和JQuery的区别在哪？为什么放弃JQuery用Vue？

* jQuery是直接操作DOM，Vue不直接操作DOM，Vue的数据与视图是分开的，Vue只需要操作数据即可
* jQuery的操作DOM行为是频繁的，而Vue利用虚拟DOM的技术，大大提高了更新DOM时的性能
* Vue中不倡导直接操作DOM，开发者只需要把大部分精力放在数据层面上
* Vue集成的一些库，大大提高开发效率，比如Vuex，Router等
