---
layout: post
title: Difference between Dictionary, List and Tuple
date: 2017-9-03
categories: blog
tags: Python
description: Difference between Dictionary, List and Tuple
---
# Difference between Dictionary, List and Tuple
## There are three main types of data in Python: dictionaries, lists, and tuples. They are represented by curly braces, brackets, and parentheses, respectively.
## Python主要有三种数据类型：字典、列表、元组。其分别由花括号，中括号，小括号表示。

 列表/元组/集合/字典的理解

- （1）列表是任意对象的序列。列表用方括号表示。

- （2）将一组值打包到一个对象中，称为元组。元组用小括号表示。元组和列表的大部分操作相同。但是，列表是不固定的，可以随时插入，删除；而元组一旦确认就不能够再更改。所以，系统为了列表的灵活性，就需要牺牲掉一些内存；而元组就更为紧凑。（注意，元组在定义过程中，字符串必须用单引号‘扩起来。）

- （3）与列表和元组不同，集合是无序的，也不能通过索引进行访问。此外，集合中的元素不能重复。

- （4）字典就是一个关联数组或散列表，其中包含通过关键字索引的对象。用大括号表示。与集合相比，通过关键字索引，所以比集合访问方便。字典是Python解释器中最完善的数据类型。

## 元组(tuple)：
　　元组常用小括号表示，即：()，元素加逗号，是元组的标识。

```
#定义一个元组
 
#tuple = 'a',
 
tuple = ('a','b','c','d','e','f','g')
 
#常规来说，定义了一个元组之后就无法再添加或修改元组的元素，但对元组切片可以添加会修改元组的元素。
 
print tuple[1:5]
 
tuple = tuple[:2]+('h')+temp[2:]
 
print(tuple)
 
#使用for循环进行遍历元组
 
for each in tuple:
 
    print each
 
#通过range()函数和for循环获取元组内元素的序号
 
for index in range(len(tuple)):
 
    print tuple[index]
```

## 列表(list):
　　列表常用方括号表示，即：[]；

　　创建一个列表，只要把用逗号分隔的不同的数据项使用方括号括起来即可。

　　例如：
```
list1 = ['a','b','c',1,3,5]
list2 = [1,2,3,4,5,6]
list3 = ["abc","bcd","cde"]
```
　　遍历列表：（len(each)：表示每个迭代变量的长度，each：表示每个迭代的变量）
```
list1 = ['a','b','c',1,3,5]
for each in list1
print(each,len(each))
```
　　列表中常用的函数：

　　>cmp(list1,list2)：比较两个列表的元素
　　len(list)：返回列表元素个数
　  max(list)：返回列表元素最大值
  　min(list)：返回列表元素最小值
　　list(tuple)：将元组转换为列表

 

　　列表中常用的9个方法：

　　>list.append(obj)：在列表的末尾添加新的对象
　　list.count(obj)：统计某个元素在列表中出现的次数
　　list.extend(list)：在列表末尾添加包含多个值的另一个序列，有扩展列表的作用
    list.insert(index,obj)：将对象插入列表中的第index元素之前
    list.pop(obj=list[-1])：默认移除列表中的一个元素（默认最后一个元素），并且返回该元素的值 
　　list.remove(obj)：移除列表中某个值
　　list.reverse()：将列表中的元素反向排列
　　list.sort(function())：将列表进行排序

## 字典(dict)
　　字典是由花括号{}来包含其数据的，花括号内包含键(key)和其对应的值(value)，一对键和值成为一个项，键和值用冒号:隔开，项和项之间用逗号,隔开，空字典就是不包含任何项的字典，也可理解为空字典就是花括号内不包含任何内容，直接使用花括号{}表示。

　　创建一个字典：
```
　　dict = {'name':'john','age':20,'sex':male}
```
　　备注：键是一个不可变的数据类型

　　访问字典：

　　>由于字典是无序的，访问字典不能通过索引的方式；通过变量名[键名]来访问。

　　字典添加项：

　　>变量名:[新添加的键名] = 新添加的键对应的值

 

　　字典修改项的值:

　　>变量名:[要修改的键名] = 新值

 

　　字典删除项或值:

　　>del方法：删除键对应的值，del 变量名[键名]；

　　　　　　 删除字典，del 变量名。
　　>clear方法：清空字典内容。

　　　　　　　 变量名.clear()
　　>pop方法：删除键对应的值，但是它会把对应的值输出后再删除


