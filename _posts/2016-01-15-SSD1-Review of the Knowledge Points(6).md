---
layout: post
title: SSD1-Review of the Knowledge Points(6)
date: 2016-1-15
categories: blog
tags: [标签一,标签二]
description: SSD1-Review of the Knowledge Points. From Chapter_01 to Chapter_09.
---

# 使用super
- 第一种使用：调用父类的构造函数
形式为：super(参数列表)
super(…)调用其直接父类的构造函数，且super(…)必须是子类构造函数中的第一个执行语句
如果在子类的构造函数中没有使用super(…)，则子类的构造函数会自动的执行其超类的默认的或无参数的构造函数
- 第二种使用：访问被子类的成员隐藏的父类成员
形式为：super.member

# 使用this
- this关键字可以在引用当前对象的所有方法中使用
- this总是调用该方法的一个引用
```$xslt
public class Box{
	int width;
	int height;
	int depth;

	Box(int i, int height, int depth) { 
		this.width = i;
		this.height = height;
		this.depth = depth;
	} 
} 
```













