---
title: CSS学习-选择器
date: 2019-03-23 08:53:37
tags: css
---

### 链接伪类选择器(a标签)
- :link
- :visited
- :hove(最常用)
- :active
``` style
    a: hove{
        color: red;
    }
```

<!--more-->

---

### 结构伪类选择器
- :first-child
- :last-child
- :nth-child(n):匹配其父元素的第n个子元素
- :nth-last-child(n):从最后一个子元素开始数
``` style
    li:nth-child(9){}   /* 匹配第9个子元素 */
    li:nth-child(even){}   /* 匹配所有的偶数位子元素 */
    li:nth-child(odd){}   /* 匹配所有的奇数位子元素 */
    li:nth-child(2n){}   /* 匹配偶数位 */
    li:nth-child(2n+1){}   /* 匹配奇数位 */
```

---
### 目标伪类选择器（:target）
``` html
<h2>目录</h2>
<a href="#life">1个人生活</a>
<a href="#experience">2人生经历</a>
<h3 id="life">个人生活</h3>
<h3 id="experience">人生经历</h3>
```
``` style
:target{
    color: red;
}
```


### 属性选择器
 选取标签带有某些特殊属性的选择器

选择器|示例|含义
--|:--:|--
E[attr]|div[title]|带有title的div
E[attr=val]|div[title=first]|带有title="first"的div
E[attr\*=val]|div[title\*=first]|带有title属性***包含***"first"的div
E[attr^=val]|div[title^=first]|带有title属性以"first"***开始***的div
E[attr\$=val]|div[title\$=first]|带有title属性以"first"***结尾***的div

### 伪元素选择器
示例|含义
--|--
p::first-letter|选择p标签内的第一个字
p::first-line|选择p标签内的第一行
p::selection|选择p标签内选中的文字
div::before|在div的内部前面插入
div::after|在div的内部后面插入