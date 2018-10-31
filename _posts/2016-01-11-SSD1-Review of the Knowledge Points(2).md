---
layout: post
title: SSD1-Review of the Knowledge Points(2)
date: 2016-1-11
categories: blog
tags: [Study, Software Systems Development1(SSD1)]
description: SSD1-Review of the Knowledge Points. From Chapter_01 to Chapter_09.
---

# Unit 2-3 Java编程基础

## JAVA程序

使用Java可以开发从命令行应用程序到图形用户界面应用程序、从桌面应用程序到Web应用程序、从小型嵌入式系统到大型分布式企业级应用等多种多样的程序。通常所指的Java程序可以分为：
命令行应用程序(Command-line Application)
图形界面应用程序(GUI Application)
小程序(applet)
服务端小程序(servlet)
服务器页面(JavaServer Pages, 检查JSP)
Web应用程序
嵌入式应用程序
企业级应用程序

## JAVA的运行环境

- Java程序运行在JAVA平台上，Java平台可以运行于Windows、 Linux、Solaris等操作系统上。
- Java平台由Java虚拟机(JVM)和Java编程接口(API)组成。
- ※Java虚拟机屏蔽了不同操作系统的差异
- ※Java API 为程序员提供了统一的编程接口
- Java API和JVM将Java程序从对硬件的依赖中分离出来，从而实现了Java程序对操作系统和硬件平台的无关性。

## 程序（Programs）

- 程序 是一些文本，这些文本可以让计算机完成一个任务
- 程序文本采用专门的语言编写，这个语言称为编程语言.
- 程序的内容称为代码.
- 当一个计算机运行或执行一个程序，则称程序在执行代码，或代码被执行了.
- Java是多种编程语言中的一种，它是一种面向对象（object-oriented）语言。.

## Programs and Models（程序与模型）
- 计算机程序都是为了解决某个问题，完成某个任务。模型就是对实际的问题进行抽象，是对问题的简单表示。模型是在对问题的分析基础上，突出了针对用户而言重要的方面，忽略其他不重要的方面。
- 每个模型都具有以下特性
※模型中的元素描述实际上更复杂的东西
※模型元素具有某些特定的行为（behavior）.
※模型元素可以基于一些共同的行为被划分为几个类
※模型元素外部的动作会触发模型元素的行为。

## 面向对象中的基本概念

- 对象（Object）
Java程序中模拟的元素称为对象
如：多个Catfish object、多个Crocodile object
- 行为（Behavior）
多个对象可能具有相同的行为。
如：Catfish都需要游动、吃食物等。

## JAVA程序的运行机制
- Java既可以被编译，又可以被解释。
- Java的源代码(后缀名为.java)文件，通过编译器，被翻译城一种中间代码，成为字节码(bytecode)(后缀名为.class)。Java的字节码被Java解释器解释执行。
- 可以把Java字节码看作是运行在Java虚拟机(JVM)上的机器代码指令。

- 消息（Message）
※Each message sent must specify which object is to receive it, what task that object should perform in response, and further details that must be supplied to describe the task adequately.（消息在不同的对象之间建立连接，是的多个对象彼此之间可以互动。）
※如：Catfish吃水草，水草的能量消失，转移到Catfish上

- Java程序（Java Program）
※A collection of objects that correspond to the important problem elements of the problem being solved or the computation being performed.
※为了完成一个任务（解决问题）的多个对象的一个集合。对象之间使用消息(message)进行联系（进行消息的传递）。

- 类（Class）
※A category of model elements is called a class in Java.（ Java中一类模型元素称为类）
※The fundamental job of a Java programmer is providing class definitions, or descriptions of how objects in each class must behavior.（Java程序员的基本工作就是定义类，或描述每个类的对象的行为）
※当程序中类已经被定义了，程序运行时可以产生类（class）的多个对象（object）。每个对象称为是该类的一个实例（instance）
※如：完成了Catfish类的定义后，可以使用Catfish类实例化多个Catfish对象。

- 预先定义的类（Predefined Objects and Classes）
※不同程序在执行时有许多相同的行为，如在屏幕上打印字符。这些功能可以由预先定义好的类实现和对象。
※Java中提供了许多这样的类，程序员在编写新的程序时可以利用这样的类和对象。

## Java程序的编译与执行

- 使用cmd进入命令行模式
- 使用javac命令对需要编译的.java源码文件进行编译，得到编译后的结果.class文件
- 执行java程序
※使用java命令执行
※将.class文件放在合适的位置供其他程序调用（如将servlet程序Welcome.class放在workbench中处理客户端发送的数据）

- Java规则（Java Rule）
※Java语法，即使用Java编写程序需要遵循的语法规则。
- 标识符（identifier）
※类或者行为需要有个名字，这个名字就是一个标识符。
※Java对大小写敏感，即标识符“system”和“System”是不同的标识符
※Java中类的名字通常以大写字母开头；其他的标识符（如方法的名字）以小写字母开头。

- 关键字（keyword）
Java语言中预先定义好的字，如class, public, static等
- Java语句（statement）的顺序
Java语言编写的顺序也是它们被处理执行的顺序。
- 程序格式（format）
※使用tab键实现缩进，是的所写的java代码美观易读
※单词和单词之间使用空格分开
※每行写一句代码(statement)，如果这局代码太长再分行。
※所有的语句用;结束
- 注释（comment）
※使用/*和*/进行注释一段文字；使用//注释一行文字
※好的习惯：在定义类之前，使用注释描述类的作用和行为。
※坏的习惯：整个程序基本没有注释。



























