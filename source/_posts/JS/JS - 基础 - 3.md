---
title: js - 基础编程练习
categories:
  - 学海无涯我游啊游
  - Javascript
tags:
---

题目描述

实现函数 makeClosures，调用之后满足如下条件：

1、返回一个函数数组 result，长度与 arr 相同

2、运行 result 中第 i 个函数，即 result[i]()，结果与 fn(arr[i]) 相同

输入例子:
<pre>
  var arr = [1, 2, 3];
  var square = function (x) {
  	return x * x;
  };
  var funcs = makeClosures(arr, square);
  funcs[1]();
</pre>

输出例子:
4

answer:
<pre>
function makeClosures(arr, fn) {
 	var funs = [];
 	for(var i = 0; i < arr.length; ++i) {
        (function(num){
            var temp = function() {
                return fn(num);

            }
            funs.push(temp);
        })(arr[i]);
    }
    return funs;
}
</pre>

why use anonymous function here?

curry,
toString
parseInt
for in loop
