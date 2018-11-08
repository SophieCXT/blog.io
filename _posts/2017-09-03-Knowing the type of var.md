---
layout: post
title: Knowing the type of var
date: 2017-9-03
categories: blog
tags: Python
description: Knowing the type of var
---
# Knowing the type of var
## 有时候我们需要知道变量类型，但不知道如何查看
- 使用内置函数type(object)
>在介绍数据类型的文章中提到过，要怎么样查看对像的数据类型。type()就是一个最实用又简单的查看数据类型的方法。type()是一个内建的函数，调用它就能够得到一个反回值，从而知道想要查询的对像类型信息。

type使用方法
```
>>>type(1)
<type 'int'>    #返回整形
>>>type('content')
<type 'str'>    #返回字符串
```
type返回值属于type类型
```
>>>type(type(1))
<type 'type'>    #返回type类型
```
