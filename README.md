# css-snippets

## Resize

div 支持手动调整尺寸

```css
overflow: auto;
resize: auto;
```

## translate Center Vertically

不需要知道 `宽和高` 实现垂直水平居中

```css
position: absolute;
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
```

## BFC

- 下列方式会创建块格式化上下文：

- 根元素（<html>）

- 浮动元素（元素的 float 不是 none）

- 绝对定位元素（元素的 position 为 absolute 或 fixed）

- 行内块元素（元素的 display 为 inline-block）

- 表格单元格（元素的 display 为 table-cell，HTML 表格单元格默认为该值）

- 表格标题（元素的 display 为 table-caption，HTML 表格标题默认为该值）

- 匿名表格单元格元素（元素的 display 为 table、table-row、 table-row-group、table-header-group、table-footer-group（分别是 HTML table、row、tbody、thead、tfoot 的默认属性）或 inline-table）

- overflow 值不为 visible 的块元素

- display 值为 flow-root 的元素

> flow-root: 一个新的 display 属性的值，它可以创建无副作用的 BFC。在父级块中使用 display: flow-root 可以创建新的 BFC。
> 使用在生产生产，指日可待。

- contain 值为 layout、content 或 paint 的元素

- 弹性元素（display 为 flex 或 inline-flex 元素的直接子元素）

- 网格元素（display 为 grid 或 inline-grid 元素的直接子元素）

- 多列容器（元素的 column-count 或 column-width 不为 auto，包括 column-count 为 1）

- column-span 为 all 的元素始终会创建一个新的 BFC，即使该元素没有包裹在一个多列容器中（标准变更，Chrome bug）
