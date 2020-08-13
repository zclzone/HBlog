---
title: CSS学习-Flex布局
date: 2019-04-01 18:53:37
tags: css
---

# **<center>CSS3-Flex 布局</center>**

---

#### Flex 属性详述

##### 1. flex-direction

> 决定主轴的方向,即元素排列的方向，有四种方式:

<!-- more -->

- row: 主轴为水平方向，元素沿主轴从左至右排列

- column: 主轴为竖直方向，元素沿主轴从上至下排列

- row-reverse: 主轴水平，元素从右至左排列，与 row 反向

- column-reverse: 主轴竖直，元素从下至上排列，与 column 反向

##### 2. flex-wrap

> 默认情况下，item 排列在一条线上，即主轴上，flex-wrap 决定当排列不下时是否换行以及换行的方式，有三种方式|wrap|wrap-reverse

- nowrap: 自动缩小项目，不换行

- wrap: 换行,第一行在上方

- wrap-reverse: 换行，第一行在下方

##### 3. flex-flow

> flex-direction 和 flex-wrap 的简写形式

> 如：row wrap 、 column wrap-reverse 等。默认值为 row nowrap，即横向排列 不换行。

##### 4. justify-content

> 决定元素在主轴上的对齐方式，当主轴沿水平方向时,有五种方式：

- flex-start(默认): 左对齐

- flex-end: 右对齐

- center: 居中对齐

- space-between: 两端对齐

- space-around: 沿轴线均匀分布

##### 5. align-items

> 决定元素在交叉轴上的对齐方式，当主轴沿水平方向时，有五种方式：

- flex-start: 顶端对齐

- flex-end: 底部对齐

- center: 竖直方向上居中对齐

- baseline: 元素第一行文字的底部对齐

- stretch: 当元素未设置高度时，元素将和容器等高对齐

##### 5. align-content

> 该属性定义了当有多根主轴时，即 item 不止一行时，多行在交叉轴轴上的对齐方式。注意当有多行时，定义了 align-content 后，align-items 属性将失效。align-content 可能值含义如下（假设主轴为水平方向）：

- flex-start：左对齐

- flex-end：右对齐

- center：居中对齐

- space- between：两端对齐

- space-around：沿轴线均匀分布

- stretch：各行将根据其 flex-grow 值伸展以充分占据剩余空间

#### flex item 属性详述

##### 1. order

> der 的值是整数，默认为 0，整数越小，item 排列越靠前

```html
<div class="wrap">
  <div class="div" style="order:4"><h2>item 1</h2></div>

  <div class="div" style="order:2"><h2>item 2</h2></div>

  <div class="div" style="order:3"><h2>item 3</h2></div>

  <div class="div" style="order:1"><h2>item 4</h2></div>
</div>
```

##### 2. flex-grow

> 定义了当 flex 容器有多余空间时，item 是否放大。默认值为 0，即当有多余空间时也不放大；可能的值为整数，表示不同 item 的放大比例，如

```html
<div class="wrap">
  <div class="div" style="flex-grow:1"><h2>item 1</h2></div>

  <div class="div" style="flex-grow:2"><h2>item 2</h2></div>

  <div class="div" style="flex-grow:3"><h2>item 3</h2></div>
</div>
```

`即当有多余空间时item1、item2、和item3以1：2:3的比例放大。`

##### 3. flex-shrink

> 定义了当容器空间不足时，item 是否缩小。默认值为 1，表示当空间不足时，item 自动缩小，其可能的值为整数，表示不同 item 的缩小比例。

##### 4. flex-basis

> 项目在主轴上占据的空间，默认值为 auto。如下代码

```html
<div class="wrap">
  <div class="div" style="flex-basis:80px"><h2>item 1</h2></div>

  <div class="div" style="flex-basis:160px"><h2>item 2</h2></div>

  <div class="div" style="flex-basis:240px"><h2>item 3</h2></div>
</div>
```

##### 5. flex

> flex 属性是 flex-grow、flex-shrink 和 flex-basis 三属性的简写总和.

##### 6. align-self

> align-self 属性允许 item 有自己独特的在交叉轴上的对齐方式，它有六个可能的值。默认值为 auto

- auto：和父元素 align-self 的值一致

- flex-start：顶端对齐

- flex-end：底部对齐

- center：竖直方向上居中对齐

- baseline：item 第一行文字的底部对齐

- stretch：当 item 未设置高度时，item 将和容器等高对齐
