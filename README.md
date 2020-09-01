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
