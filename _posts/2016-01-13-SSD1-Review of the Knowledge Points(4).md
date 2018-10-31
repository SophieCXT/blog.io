---
layout: post
title: SSD1-Review of the Knowledge Points(4)
date: 2016-1-13
categories: blog
tags: SSD1(Software Systems Development1--Introduction to Information System)
description: SSD1-Review of the Knowledge Points. From Chapter_01 to Chapter_09.
---
# SSD1-Review of the Knowledge Points(4)
## 面向对象编程的三个原则

- 封装性（Encapsulation）
- 继承性（Inheritance）
- 多态性（Polymorphism）

## 类和对象
- 类是一个软件构件，定义了特定对象的数据（状态）和方法（行为），有了这个定义，由这个类可以构造多个属于这一类的对象
- 类就像一个模板，描述属于一个类型的对象具有的性质。
- 每个由类生成的对象称为这个类的实例（instance）

>[修饰符] class  类名[extends 父类名] {
 		 [访问修饰符] type 属性1;
 			……
 		 [访问修饰符] type 属性n;
 
 		 [访问修饰符] 类名(参数列表){主体}
 
 		 [访问修饰符]  返回值类型 方法1(参数列表){方法主体}
 			……
 		 [访问修饰符] 返回值类型  方法m(参数列表){方法主体}
 	}

## 类的成员
- 在类中，数据或变量被称为实例变量(instance variable)，代码包含在方法中。
- 定义在类中的方法和实例变量都称为类的成员(class members)
- 大多数类中，实例变量被定义为在该类中的方法被操作，也即方法决定了该类中的数据如何使用。	
- 定义在类中的实例变量，在类的每个实例中（即类的每个对象）都包含它自己对这些变量的拷贝。这样，一个对象的数据是独立且唯一的。

## 类的构造函数
- 构造函数在对象创建时初始化
- 它与类同名，语法与方法类似
- 一旦定义了构造函数，在对象被创建后，在new运算符完成前，构造函数立即自动调用
- 构造函数没有任何返回值
- 构造函数的任务就是初始化一个对象的内部状态，以便使得创建的实例变量能够完全初始化
- 如果不显式的为类定义一个构造函数，Java将为该类创建一个默认的构造函数
- 带自变量的构造函数

## 方法

- 方法的返回值
方法返回的数据类型必须与该方法指定的返回类型相兼容
```$xslt
public int getRow(){ 
   return 0; 
}
```
接收方法返回值的变量也必须与指定的方法返回值的类型相兼容
```$xslt
int i = getRow();
```
return; 和 return null;
```$xslt
public void test1(){
	…
	return;
}

```
```$xslt
public String test2(){
	…
	return null;
}
```
## 访问修饰符
一个成员如何被访问取决于它的声明的访问修饰符
- public：该成员可以被你的程序中的任何其他代码访问
- private：该成员只能被它的类中的其他成员访问
- protected：用于继承情况中，该成员能被它的类中的其他成员访问，也可以被其子类访问，以及处于同一包内的所有类访问
- 默认的访问修饰符：被处于同一个包内的类访问

## final的使用
- final变量
类中定义变量得前面加上final关键字，即表示该变量一旦被初始化便不可改变，这里不可改变的意思对基本类型来说是其值不可变，而对于对象变量来说其引用不可再变。其初始化可以在两个地方，一是其定义处，也就是说在final变量定义时直接给其赋值，二是在构造函数中。这两个地方只能选其一，要么在定义时给值，要么在构造函数中给值，不能同时既在定义时给了值，又在构造函数中给另外的值

## 对象的声明

- 声明类型为某个类的变量，称为是对该类的实例化
Java中，所有的类对象都必须动态分配
- BankAccount account = new BankAccount(“Bob”, 10.00);

## Java的访问修饰符
- public access allows code from outside a class definition to access a variable or a method directly. 
- private access does not allow access from outside a class. 





