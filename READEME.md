## 1. HTML

### 1.1 HTML 元素分类

- 块级元素 block
- 行内元素 inline
- inline-block

### 1.2 HTML 元素嵌套关系

- 块级元素可以包含行内元素
- 块级元素不一定能包含块级元素，p 不能包含 div
- 行内元素一般不能包含块级元素，a 元素可以包含块级元素

## 2. CSS （Cascading Style Sheet 层叠样式表）

### 2.1 选择器

- 2.1.1 用于匹配 HTML 元素
- 2.1.2 分类和权重

  - 选择器分类

  ```
  元素选择器 a{}
  伪元素选择器 ::before{}
  类选择器 .link{}
  属性选择器 [type=radio]{}
  伪类选择器 :hover{}
  ID选择器 #id{}
  组合选择器 [type=checkbox] + label{}
  否定选择器 :not(.link){}
  通用选择器 *{}
  ```

  - 选择器权重

  ```
  // ==计算不进位==
  ID选择器 +100
  类 属性 伪类 +10
  元素 伪元素 +1
  其它选择器 +0
  #id .link a[href] = 100 + 10 + 1 + 0 = 111
  #id .link.active = 100 + 10 + 10 = 120
  // ==直观==
  !important优先级最高
  元素属性优先级高 style="xxx"
  相同权重，后写的生效
  ```

- 2.1.3 解析方式和性能
  - 浏览器解析方式：从右向左，先解析 hello，再匹配前面是否是 div，再匹配 body，提高性能

```html
.body div .hello {...}
<body class="body">
  <div>
    <a class="hello">aaa</a>
  </div>
</body>
```
