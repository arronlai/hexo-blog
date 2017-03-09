---
title: '[CSS] - 基础 - 1'
id: 40
categories:
  - 学海无涯我游啊游
  - HTML/css（HTML5/css3)
date: 2017-02-12 15:26:55
tags:
---

1 css - cascading style sheets

2 基本结构：选择器+声明

3 内联式css，嵌入式css，外部式css（相同权值，就近）

4 选择器

1）标签选择器

2）类选择器（多对多）

3）ID选择器（一对一）

4）子选择器&gt;

5）后代选择器

6）通用选择器*

7）伪类选择符 （选择html中标签的某种状态，如a:hover - 兼容性问题）

5 特性

继承，特殊性（权值：标签1，类10，ID100），重要性

6 字体

1）font-family:"Microsoft Yahei";

2）font-style, font-weight

3）text-decoration:underline; line-through

4）text-indent

5）line-height

6）letter-spacing, word-spacing

7）text-align

7 块元素    display:block;

1）&lt;div&gt;、&lt;p&gt;、&lt;h1&gt;...&lt;h6&gt;、&lt;ol&gt;、&lt;ul&gt;、&lt;dl&gt;、&lt;table&gt;、&lt;address&gt;、&lt;blockquote&gt; 、&lt;form&gt;

2）特性：独占一行；宽度、高度、行高、顶底边距可设；宽度为设置为父元素100%

8 内联元素    display:inline

1）&lt;a&gt;、&lt;span&gt;、&lt;br&gt;、&lt;i&gt;、&lt;em&gt;、&lt;strong&gt;、&lt;label&gt;、&lt;q&gt;、&lt;var&gt;、&lt;cite&gt;、&lt;code&gt;

2）特性：和其他内联元素在同行；宽度、高度、顶底边距不可设置；宽度为其包含文字或图片的宽度

9 内联块元素    display:inline-block

1）&lt;img&gt;、&lt;input&gt;

2）特性：和内联/内联块元素同行，宽度、高度、顶底边距可设置

10 盒模型

1）块模型具有盒模型的特点。内外填充（padding，margin，border）

2）border: {border-width border-style border-color} (dashed, dotted, solid)

3）宽度：包括margin，border，padding，和content（内容）宽度

11 布局模型

1）流动模型（默认）：块元素自上而下，每个占一行，未分配情况下宽度100%；内联元素从左到右排布

2）浮动模型：实现块元素同行显示，任何元素都可以加float。

3）层模型：position:{relative,absolute,fixed} （absolute和fixed的相对位置是父元素中具有相对属性即position:relative的元素，找不到则是body）

11 代码简写

1）盒模型：margin，padding，上，右，下，左；上下，左右；上下左右

2）颜色值缩写：#333，#369

3）字体缩写：font-weight, font-style, font-family, font-size, line-height, font-variant 等可合为font（font-size/line-height, font-family 必填）

12 字体大小

1）像素：px css规定90px为1英寸

2）em：以font-size为标准，如font-size:12px; text-indent:2em; 其中1em=12px，如果font-size是em则以父元素font-size为标准（responsive）

3）百分比：仍然以font-size为标准计算

13 水平居中

1）内联：父元素text-align:center;实现

2）定宽块元素：左右margin设为auto（定宽和块两个条件同时满足）

3）不定宽块元素：1\. 外部嵌套table，table设置左右margin为auto（table自适应内容宽度，相当于自动变成一个和内容长度相同的定宽块元素）；2\. 改为内联元素（display:inline;）后设置父元素text-align:center（不增加无语义标签，但牺牲块元素一些特性）；3\. 父元素float:left;position:relative;left:50%;子元素（需要居中的元素）position:relative;left:-50%;

14 垂直居中

1）父元素高度确定的单行文本：设置父元素height和line-height相同

2）父元素高度确定的多行文本/包括图片：1\. 加入table（包括td），即引入vertical-align:middle;到父元素，table默认已经带有这一属性，td需要设置高度，否则会自适应；2\. 父级块元素添加display:table-cell;vertical-aligh:middle;（兼容性差ie6、ie7不支持）

15 吊诡的float和position:absolute

会导致该元素display变成inline-block，然后可以设置宽度、高度、行高、顶底边距等。
