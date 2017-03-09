---
title: '[JS] - 基础 - 2'
id: 183
categories:
  - 学海无涯我游啊游
  - Javascript
date: 2017-02-15 15:23:06
tags:
---

1\. 运算顺序：算术&gt;比较&gt;逻辑&gt;赋值

2\. a++ ++a

3\. 数组可以指定长度，如new Array(12);但实际还是变长的，可以储存长度之外个数组。

&nbsp;&nbsp;&nbsp; .length

&nbsp;&nbsp;&nbsp; 二维数组：相当于一维数组的元素是数组

4\. switch

switch() {

&nbsp;&nbsp;&nbsp; case 1:

&nbsp;&nbsp;&nbsp; break;

&nbsp;&nbsp;&nbsp; default:

}

注意 break;

5\. for, while, do while -&nbsp; break;&nbsp; continue;

6\. 事件 onclick, onmouseover, onmouseout, onfocus, onselect, onchange, onload, onunload(window close)

*7\. 对象*

1) Date

A. new Date(); new Date(2017,2,15); new Date("Oct 1 2017");

B. 方法：getFullYear(); getDay(); getTime(); setTime(); - 注：milliseconds

2) String

A. 方法：toUpperCase(); toLowerCase; charAt(); indexOf(substr, pos); split(char, limit); substring(start, end);&nbsp; substr(start, length);

3) Math

A. 方法：ceil(); floor(); round(); random(); （注：无参数）

4) Array

A. new Array(); new Array(10); new Array(1,2,3);

B. 方法：concat();（注：不修改数组本身） join();（注：可空，逗号）reverse(); slice(start, end);（注：end可省可负，不改变原数组）sort(function()); （注：－1，1）

*8\. window对象*

1) setInterval(function, interval); 注：interval以milliseconds计算。clearInterval(i);

2) setTimeout(function, time); clearTimeout(i);

9\. History 对象

1) 属性：length

2) 方法：go();（注：代表向前或向后多少页） back(); forward();

10\. Location

获取与当前地址相关信息

href, window.location.reload(); window.location.assign();

11\. Navagator

当前browser相关信息

1) userAgent; -&gt; 用户代理字符串

12\. screen (window.screen/screen)

1)属性：width, height, availWidth, availHeight

----------------

12\. DOM

1) getElementById(); getElementsByName(); getElementsByTagName();

2) getAttribute(); setAttribute(name, value);

3) nodeName, nodeValue, nodeType

4) childNodes, parentNode, firstChild, lastChild, nextSibling, previousSibling

5) appendChild(); insertBefore(,); removeChild(node); replaceChild(new, old);

6) document.createElement(); （注：创建元素节点，参数为tag name）document.createTextNode(); （注：创建的即为普通文本节点）

* * *

13\. 网页尺寸

1) 窗口宽高：cross browser：document.documentElement.clientWidth || document.body.clientWidth; document.documentElement.clientHeight || document.body.clientHeight;

2) 内容宽高: cross browser: document.documentElement.scrollWidth || document.body.scrollWidth; document.documentElement.scrollHeight || document.body.scrollHeight; 注：IE，Opera返回值可比clientHeight/clientWidth小，FF返回最小值等于窗口宽高。

3) 网页宽高：offsetHeight/offsetWidth = clientHeight/clientWidth + 滚动条 ＋ 边框

4) 滚动距离: scrollTop; scrollLeft; offsetTop; offsetLeft; （注：offset相对于该元素的父元素）
