---
title: Bootstrap3 常用的类
date: 2019-05-01 20:39:31
categories: CSS
tags: css
---

# **<center>Bootstrap3 常用的类</center>**

#### 布局容器

> container 响应式容器

> container-fluid 流式容器

#### 栅格系统

<!-- more -->

> row 行

> col-\*-\* 列

```
实例 col-md-3
第一个参数:
  lg 大屏：大屏及以上生效
  md 中屏：中屏及以上生效
  sm 小屏：小屏及以上生效
  xs 超小屏：超小屏及以上生效
第二个参数:Row 默认会把一行分成 12 等份列，这里第二个参数表示的是当前元素占 12 等份当中的几份
```

> col-xs-offset-4 偏移，往右偏移四等份

> col-xs-push-\* 排序 往后推几份
> col-xs-pull-\* 排序 往前拉几份

> hidden-\* 控制在某种屏幕下隐藏，其他屏幕可见，可选参数 lg、md、sm、xs

> pull-left 左浮动
> pull-right 右浮动

> text-right 文字右对齐
> text-left 文字左对齐
> text-center 居中
