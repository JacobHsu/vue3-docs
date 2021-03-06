# API

Vue.js API 包含以下类目：

- [应用配置](/api/application-config.html)
- [应用 API](/api/application-api.html)
- [全局 API](/api/global-api.html)
- [选项式 API](/api/options-api.html)
- [实例 property](/api/instance-properties.html)
- [实例方法](/api/instance-methods.html)
- [指令](/api/directives.html)
- [特殊指令](/api/special-attributes.html)
- [内置组件](/api/built-in-components.html)
- [响应性 API](/api/reactivity-api.html)
- [组合式 API](/api/composition-api.html)

## [JSONPlaceholder](https://jsonplaceholder.typicode.com/guide/)

```js
fetch('https://jsonplaceholder.typicode.com/posts/1')
  .then((response) => response.json())
  .then((json) => console.log(json));
```

```js
const getTodo = async () => {
  const res = await fetch('https://jsonplaceholder.typicode.com/posts/1') //async/await promise->object
  const data = await res.json() 
  console.log(data)
}
```


```json
{
  id: 1,
  title: '...',
  body: '...',
  userId: 1
}
```
