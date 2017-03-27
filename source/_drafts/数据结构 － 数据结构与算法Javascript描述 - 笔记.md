---
title: '[数据结构] － 数据结构与算法Javascript描述 - 笔记'
id: 220
categories:
  - 学海无涯我游啊游
  - 数据结构算法
tags:
---

题外话：这几天看算法和数据结构有种吃自助吃撑了还要接着塞的满足感。由于入了前端的坑，其他语言语法已经基本忘记（&lt;-有脸说），正在发愁要不要先看个c++语法的时候，看到了这么一本书

![](http://www.arronlai.com/wp-content/uploads/2017/02/Screen-Shot-2017-02-24-at-3.38.20-PM-230x300.png)

感觉可以不拯救语法先拯救一下数据结构，就开始看了。讲解得不错，推荐一下（这个封面让我想起了某让人死去活来的课）。

1\. JS内建对象 数组： 深复制，浅复制

indexOf(), lastIndexOf(), join(), toString(), concat(), splice(), slice()

push(), pop(), unshift(), shift(), reverse(), sort()

forEach(), map(), every(), filter(), some()

[codesyntax lang="javascript" lines="fancy"]
<pre>var arr = [11,2,333,4,9,9];
console.log(arr.sort()); //dictionary order
console.log(arr.sort(function(a,b){ return a-b; })); //numerical order</pre>
[/codesyntax]

2.