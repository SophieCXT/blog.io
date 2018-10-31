---
layout: post
title: SSD1-Servlet Summary
date: 2016-1-08
categories: blog
tags: SSD1(Software Systems Development1--Introduction to Information System)
description: Servlet
---

# Key Words
动态网页生成技术：FORM servlet
HTTP链接（connection）
会话（session）
Cookie
server push
client pull
表单控件（Form Control）Input Labe Textarea
提交给服务器的信息是名字－值对(name-value pair)
Servlet

# Content
## 1.	动态网页生成原理和HTTP connection
1）动态网页生成原理
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/WHU/2016-1-07-01.jpg)

2）HTTP连接过程
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/WHU/2016-1-07-02.jpg)
- 1）	session：为了完成一个任务而进行的多个HTTP连接（客户机与服务器的信息交互）
- 2）	Cookie：服务器发送给浏览器的体积很小的纯文本信息，用户以后访问同一个Web服务器时浏览器会把它们原样发送给服务器。通过让服务器读取它原先保存到客户端的信息，网站能够为浏览者提供一系列的方便，例如在线交易过程中标识用户身份、安全要求不高的场合避免用户重复输入名字和密码、门户网站的主页定制、有针对性地投放广告，等等。 
- 3）	推拉模式（Server push & Client pull）
- i.	Server push:

- - a.	Client-Server的交互由Server控制

- - b.	Server主动给Client发送数据，HTTP连接保持，直到Server自己关闭连接，或者Client中断了连接。
- ii.	Client pull
- - a.	Client自动生成请求信息（无需用户参与）
- - b.	在传统的用户驱动（user driven）的C/S交互中，用户驱动客户机向服务器发起请求，（如点击一个链接），返回的信息由用户定（如请求特定的网页）；而在Client pull模式，是由服务器或servlet（而不是用户）指定对Client请求的处理。
- - c.	在传统的用户驱动（user driven）的C/S交互中，用户驱动Client向Server发起请求（如点击一个链接），返回的信息由用户定（如请求特定的网页）；而在Client pull模式，是由服务器或servlet（而不是用户）指定对Client请求的处理。

## 2.	FORM
- 1）	为什么使用form：使用表单可以实现页面的数据传送（传送给服务器）
- 2）	当用户在页面内在各种控件（control）中填写信息后，单击提交（submit）按钮可以实现数据的发送（发送给服务器）。在Carnegie提供的实例中，我们所用的workbench就是一个形象化的服务器
- 3）	表单必须和一个程序连接实现数据的处理，即由FORM中的action属性指定处理数据的程序（如一个servlet的名字），表单中使用method属性告诉浏览器数据传送的方法（post或get）
- 4）	Form的格式：
<FORM element attributes>
表单内容 ...
</FORM>
	主要的element attributes有action, method等，如：
<FORM action=“服务器上处理数据的程序名” method =“数据传输的方法(post或get)”>
</FORM>
- 5）	form控件
Textarea：文本框
Label：勾选框
Select
Input
Option
Button
File Select
- 6）	Input：
<INPUT type=“checkbox”> 产生一个复选框（复选）
<INPUT type=“text”> 产生一个单行的文字输入字段
<INPUT type=“image”> 建立一个用来代替提交按钮的图片（与提交按钮一样按下后会把表单数据传送给指定的程序）
<INPUT type=“password”> 产生一个单行的密码输入字段（输入的内容会以 * 号显示）
<INPUT type=“radio”> 产生一个单选按钮
<INPUT type=“submit”> 产生一个表单数据提交按钮，按下后会把表单数据传送给指定的程序
<INPUT type=“reset”> 产生一个用来恢复表单内容的清除按钮，按下以后表单内容会恢复成原本的默认值
<INPUT type=“hidden”> 建立一个隐藏字段（该字段不会显示在浏览器窗口上）
- 7）	FORM Control
Name（给控件一个名字）：每个控件都必须有一个名字（由控件的name属性指定）
Value（赋值给控件，不同的控件该属性值的意义不同）：每个控件都有一个初始值(initial value)和当前值(current value) ,初始值也叫缺省值，由value属性设定。当网页第一次被载入的时候控件的值叫初始值，此后对控件值的修改得到的值称为当前值。如果控件没有初始值，且没有当前值，则该控件为未定义的（undefined）
Type（控件的类型，如input控件中使用type属性定义不同的控件）
Length
Maxlengh
Align
当表单向服务器提交数据时，将<FORM>和</FORM>之间的控件的名字和相应的值传送给服务器。
所有由表单传送给服务器的控件（即有名字和值的控件）称为成功的控件(successful controls)

## 3.	Servlet（服务器端小程序）

- 1）	位于服务器端
- 2）	接受来自客户端的名字－值对
- 3）	处理信息，服务器将处理后的信息发送给客户端

```$xslt
package javax.servlet;

import java.io.IOException;

public abstract interface Servlet
{
  public abstract void init(ServletConfig paramServletConfig)
    throws javax.servlet.ServletException;

  public abstract ServletConfig getServletConfig();

  public abstract void service(ServletRequest paramServletRequest, ServletResponse paramServletResponse)
    throws javax.servlet.ServletException, IOException;

  public abstract String getServletInfo();

  public abstract void destroy();
}

```









