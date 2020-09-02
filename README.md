# reread-js

[TOC]

### 块级作用域
块级作用域使得IIFE不再必要

### 顶层对象
|            | window | self | global |
| --------   | ------ | ---- | ------ |
| browser    | window | self |        |
| web worker |        | self |        |
| node       |        |      | global |

### 只读
```js
const a = 0;
const foo = Object.freeze({});
const foo = freezeDeep(obj);  // 递归冻结
```
### CSP
CSP（Content Security Policy，内容安全政策）
- 白名单制度
- 防止XSS攻击
- 启用CSP方式
  - `<meta>`标签
  - HTTP头信息

### 尾调用优化
- ES6的尾调用优化只在严格模式下开启
- 正常模式下，函数内部有两个变量，可以跟踪函数的调用栈
  - `func.arguments`
  - `func.caller`
