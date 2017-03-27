---
title: '[JS] - 基础 - 1'
id: 96
categories:
  - 学海无涯我游啊游
  - Javascript
date: 2017-02-14 18:57:38
tags:
---

1\. 基本格式

&lt;script type="text/javascript"&gt; //code &lt;/script&gt;

&lt;script src=""&gt;&lt;/script&gt;

2\. 变量命名：字母、下划线、美元符号开头，由任意数字、字母、下划线、美元符号组成。区分大小写。

3\. io

document.write()用于向html流输出，可输出变量

alert()确认框打印，类似document.write，**点击确定前不进行任何操作**

confirm()获取用户输入，true/false

prompt()获取用户输入，null/string

4\. window

window.open(string url, string name, string params)&nbsp; name('_blank', '_self', '_top'); params包括window距离屏幕的位置，window大小，menubar、scrollbar是否包括等。

window.close(); - 关闭当前窗口 or [窗口对象].close();

5\. DOM

1) Document Object Model将html呈现为节点树结构（包括元素，属性，文本三种节点）eg.&lt;a href="http"//www.arronlai.com"&gt;click me&lt;/a&gt;

2) document.getElementById() 返回HTML Object

3) .innerHTML

4) .style.property (display)

5) className
