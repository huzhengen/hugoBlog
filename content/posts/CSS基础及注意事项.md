---
title: "CSS基础及注意事项"
date: 2018-10-11T13:39:57+08:00
draft: false
---

层叠样式表 (Cascading Style Sheets，缩写为 CSS）

注意事项

* 浮动：给子元素加`float:left/right;`，给父元素加`clearfix`
* div的高度是由其内部文档流元素的高度总和决定的（并不一定相等），文档流是文档内元素流动的方向，内联元素从左往右流动，块级元素从上往下流动。
* `position: fixed`可以脱离文档流
* `div>span`表示div的子元素span（不能是孙子元素）
* 没有必要的话，尽量不写height

```css
.clearfix{
    content: '';
    display: block;
    clear: both;
}
```

[CSS规范中文文档](http://www.ayqy.net/doc/css2-1/cover.html)