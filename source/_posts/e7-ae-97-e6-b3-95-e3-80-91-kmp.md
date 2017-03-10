---
title: '[算法]- kmp'
id: 227
categories:
  - 学海无涯我游啊游
  - 数据结构算法
date: 2017-02-25 17:55:14
tags:
---

刷题遇到个kmp算法，以及求next数组的题目，没记得是什么，重新看了一遍这个算法，然后实现了一下。

解决的问题大概是查找一个字符串A是否包含字符串B。暴力o(mn)，即每次不匹配字符串A，B相对位置移动1位。KMP相当于在这个基础上优化，每次不止移动一位，next数组解决的就是每次移动多少相对位置的问题。

最简单的一种情况是，字符串B中没有重复，如abc，则每次不匹配之后可以直接把字符串B的首字符移动至字符串不匹配位置处继续比较，如图（-v- 灵魂画手）

![](http://www.arronlai.com/wp-content/uploads/2017/02/WechatIMG6-e1488015850577-300x225.jpeg)

这个比较好理解因为没有重复字符，比较到一个不同就直接从字符串B的首字符重新比较。

吊诡的是，如果字符串B里面有重复就不能直接移动到首位比较，然后问题就是应该移动到哪里。KMP的解决方案是维护一个next数组。以后解释，先直接贴代码


<pre>function getNext(str) {
    var len = str.length;
    var k = -1;
    var j = 0;
    var next = [-1];
    while(j &lt; len) {
      if(k==-1 || str[j] == str[k]) {
        k++;
        j++;
        next[j] = k;
      }else {
        k = next[k];    //from k to next[k] no need to compare
      }
    }
    console.log(next);
    return next;
  }</pre>

<pre>function KMP(m, n) {
    console.time("KMP:");
    var i = 0;
    var j = 0;
    var next = getNext(n);
    while(i &lt; m.length &amp;&amp; j &lt; n.length) {
      if(j==-1 || m[i] == n[j]) {
        i++;
        j++;
      } else {
        j = next[j];
      }
    }
    if(j == n.length) {
      console.timeEnd("KMP:");
      return (i-j);
    }
    console.timeEnd("KMP:");
    return "not found";
  }</pre>


&nbsp;

数组里存的是每次字符串A，B不匹配时候应该把字符串B移到什么位置，利用这个数组KMP的实现如下：

demo：https://arron-lai.github.io/algorithm/kmp