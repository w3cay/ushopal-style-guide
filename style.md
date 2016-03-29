# CSS & Sass 代码规范

## CSS

### 格式

 - 使用两个空格作为缩进
 - class 命名使用中划线连接单词而不是驼峰命名法或下划线连接单词
 - 不要使用 ID 选择器
 - 当一个 `rule` 包含多个 `selector` 时，每个选择器声明必须独占一行
 - 属性名与之后的 `:` 之间不允许包含空格， `:` 与属性值之间必须包含空格
 - 将右花括号`}`放在新的一行
 - 在每个 `rule` 间保留一个空行
 - 避免为 0 值指定单位，例如，用 margin: 0; 代替 margin: 0px
 - 字符串使用单引号`'`

**Bad**

```css
.avatar{
    margin: 0px;
    border-radius:50%;
    border:2px solid white; }
.no, .nope, .not_good {
    // ...
}
#lol-no {
  // ...
}
```

**Good**

```css
.avatar {
  margin: 0;
  border-radius: 50%;
  border: 2px solid white;
}

.one,
.selector,
.per-line {
  // ...
}
```

### 属性书写顺序
相关的属性声明应当归为一组，并按照下面的顺序排列：
Positioning
Box model
Typographic
Visual
> 由于定位（positioning）可以从正常的文档流中移除元素，并且还能覆盖盒模型（box model）相关的样式，因此排在首位。盒模型排在第二位，因为它决定了组件的尺寸和位置。

> 其他属性只是影响组件的内部（inside）或者是不影响前两组属性，因此排在后面。


```css
.declaration-order {
  /* Positioning */
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 100;
  
  /* Box-model */
  display: block;
  float: right;
  width: 100px;
  height: 100px;
  margin: 100px;
  padding: 100px;

  /* Typography */
  font: normal 13px Helvetica Neue, sans-serif;
  line-height: 1.5;
  color: #333;
  text-align: center;

  /* Visual */
  background-color: #f5f5f5;
  border: 1px solid #e5e5e5;
  border-radius: 3px;

  /* Misc */
  opacity: 1;
}
```

## Sass
### 语法

 - 使用`.scss`语法，不要使用`.sass`语法
 - 把 @include 放到属性声明的末尾
 - 嵌套选择器放到最底部，并与规则声明之间保留一个空行
 
```sass
// bad
.btn {
  @include transition(background 0.5s ease);
  .icon {
    margin-right: 10px;
  }
  background: green;
  font-weight: bold;
}
// good
.btn {
  background: green;
  font-weight: bold;
  @include transition(background 0.5s ease);

  .icon {
    margin-right: 10px;
  }
}
```

### 命名规则

对于变量、函数和混合宏，使用小写连字符`-`连接不同的单词（如：$my-variable），不要使用驼峰法命名，或者下划线连接。