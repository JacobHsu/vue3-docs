
# .eslintrc.js

禁用不必要的分号 (no-extra-semi)

[semi](https://cn.eslint.org/docs/rules/semi)

.eslintrc.js

```js
rules: {
  semi: ["error", "always"]
}
```

默认选项 "always" 的 正确 代码示例：

```js
/*eslint semi: "error"*/

var name = "ESLint";

object.method = function() {
    // ...
};
```

ex: vitex.net
