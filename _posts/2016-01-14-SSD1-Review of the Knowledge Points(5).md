---
layout: post
title: SSD1-Review of the Knowledge Points(5)
date: 2016-1-14
categories: blog
tags: [Study, Software Systems Development1(SSD1)]
description: SSD1-Review of the Knowledge Points. From Chapter_01 to Chapter_09.
---

# 继承（Inheritance ）

- 被继承的类称为父类(parent class)，或称为超类(super class)、基类(base class)、超类型(supertype)
- 继承父类而产生的新类称为子类(subclass)、导出类(derived class)或子类型(subtype) 
- 定义子类的时候，使用extends关键字实现对父类的继承
> 类修饰符 class 子类名 extends 父类名{
    	类的主体
  }
- 父类的一个引用变量可以被任何从该父类派生的子类的引用赋值
> SuperClass A = new SuperClass();
  		SubClass B = new SubClass();
          A = B; 

# Override
- 类层次结构中，如果子类中的一个方法与它父类中的方法有相同的方法名和类型声明，称子类中的方法重写(override)父类中的方法
- 从子类中调用重写方法时，它总是调用子类定义的方法，而父类中定义的方法将被隐藏。

- 父类和子类之间的多态性
```$xslt
class A {
    void printLine(){
	 System.out.println(“No override!");
	}
}
class B extends A{	
    void printLine(){
	System.out.println(“Override printLine of A");
	}	
}
```
- 一个类中的多态性
```$xslt
class A {
		
    void printLine(){
	 System.out.println(“No parameter here");
	}
	
    void printLine(String str){
	System.out.println(s);
	}
}	
```











