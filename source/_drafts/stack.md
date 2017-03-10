---
title: stack
categories:
  - 学海无涯我游啊游
  - 数据结构算法
tags:
---
包含最小值的栈
1.0 锉逼写法 －> pop完遍历找最小 TT
# -*- coding:utf-8 -*-
class Solution:
    def __init__(self):
        self.data = []
        self.minEle = []
    def push(self, node):
        # write code here
        self.data.append(node)
        if len(self.minEle) == 0:
            self.minEle.append(node)
        if self.minEle[0] > node:
            self.minEle[0] = node
        return
    def pop(self):
        # write code here
        cur = self.data.pop()
        if cur == self.minEle[0] and len(self.data) > 0:
            self.minEle[0] = self.data[0]
            for i in range(len(self.data)):
                if self.data[i] < self.minEle[0]:
                    self.minEle[0] = data[i]
        return cur
    def top(self):
        # write code here
        return self.data[0]
    def min(self):
        # write code here
        return self.minEle[0]

----

2.0 空间换时间（废话），minEle也维护一个栈
# -*- coding:utf-8 -*-
class Solution:
    def __init__(self):
        self.data = []
        self.minEle = []
    def push(self, node):
        # write code hedre
        self.data.append(node)
        if len(self.minEle) == 0:
            self.minEle.append(node)
        if self.minEle[0] > node:
            self.minEle.append(node)
        else:
            self.minEle.append(self.minEle[-1])
        return
    def pop(self):
        # write code here
        cur = self.data.pop()
        self.minEle.pop()
        return cur
    def top(self):
        # write code here
        return self.data[0]
    def min(self):
        # write code here
        return self.minEle[-1]
