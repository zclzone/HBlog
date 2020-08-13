---
title: CSS学习-background属性
date: 2019-03-23 08:53:37
tags: css
---

### background属性

<!-- more -->

属性|示例|备注
--|--|--
背景颜色|background-color: red;|
背景图片|background-image: url(iamges/\***.jpg);|
背景平铺|background-repeat: repeat-x;background-repeat: repeat-x;|-x:横向平铺；-y:纵向平铺；no-repeat为取消平铺
背景图片位置(一)|background-position: left top;<br/>background-position: right bottom;<br/>background-position: center;|分别为左上、右下、居中，若只写一个属性则另一个默认为center
背景图片位置(二)|background-position: 10px 30px;|第一个值为水平坐标，第二个值为纵向坐标
背景图片位置(三)：混搭|background-position: 10px center;|横向10px，纵向居中
背景附着|background-attachment: scroll / fixed;|默认是scroll
背景缩放（一）|background-size: 50%;<br/>background-size: 100px 200px;|缩放为原来一半大小；宽100px，高200px，尽量只改一个值，防止图片失真
背景缩放（二）|background-size: cover / contain;|cover：会自动调整缩放比列，保证图片始终填充满背景区域，移出部分会被隐藏;contain:自动调整缩放比例，保证图片完整显示，但背景可能会有部分裸露
> 简写方式:background: 颜色 图片 平铺 附着 位置
``` style
<style>
	body{
		background: #000 url(img/xxx.jpg) no-repeat fixed center -25px;
	}
</style>
```

凹凸文字效果
``` html
<body>
   <div>我是凸起的文字</div>
   <div>我是凹下的文字</div>
</body>
<style>
   body {
       background-color: #ccc;
   }
   div {
       color: #ccc;
       font: 700 80px "微软雅黑";
   }
   div:first-child {
       text-shadow: 1px 1px 1px #000,-1px -1px 1px #fff;
   }
   div:last-child {
       text-shadow: -1px -1px 1px #000,1px 1px 1px #fff;
   }
</style>
```