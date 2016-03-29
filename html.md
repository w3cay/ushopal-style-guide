# HTML代码规范

## 语法

- 用两个空格来代替制表符（tab）。

- 嵌套元素应当缩进一次（即两个空格）。

- 对于属性的定义，确保全部使用双引号，绝不要使用单引号。

- 不要在自闭合（self-closing）元素的尾部添加斜线

**示例**
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page title</title>
  </head>
  <body>
    <img src="images/company-logo.png" alt="Company">
    <h1 class="hello-world">Hello, world!</h1>
  </body>
</html>
```

## HTML5 doctype
为每个 HTML 页面的第一行添加标准模式（standard mode）的声明，这样能够确保在每个浏览器中拥有一致的展现。

```html
<!DOCTYPE html>
<html>
  <head>
  </head>
</html>
```

## 语言属性
强烈建议为 html 根元素指定 lang 属性，从而为文档设置正确的语言。这将有助于语音合成工具确定其所应该采用的发音，有助于翻译工具确定其翻译时所应遵守的规则等等。

## 字符编码
通过明确声明字符编码，能够确保浏览器快速并容易的判断页面内容的渲染方式。这样做的好处是，可以避免在 HTML 中使用字符实体标记（character entity），从而全部与文档编码一致（一般采用 UTF-8 编码）

## 属性顺序
HTML 属性应当按照以下给出的顺序依次排列，确保代码的易读性。
```
class
id, name
data-*
src, for, type, href
title, alt
aria-*, role
```
> class 用于标识高度可复用组件，因此应该排在首位。id用于标识具体组件，应当谨慎使用（例如，页面内的书签），因此排在第二位。

```html
<a class="..." id="..." data-modal="toggle" href="#">
  Example link
</a>

<input class="form-control" type="text">

<img src="..." alt="...">
```

## 布尔（boolean）型属性
布尔型属性不用赋值
```
<input type="text" disabled>

<input type="checkbox" value="1" checked>

<select>
  <option value="1" selected>1</option>
</select>
```
