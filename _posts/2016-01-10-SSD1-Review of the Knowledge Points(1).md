---
layout: post
title: SSD1-Review of the Knowledge Points(1)
date: 2016-1-10
categories: blog
tags: [Study, Software Systems Development1(SSD1)]
description: SSD1-Review of the Knowledge Points. From Chapter_01 to Chapter_09
---

# SSD1Introduction to Information Systems

## Unit 1-网络程序及HTML语言

- ※ 1.1 知识点
- 因特网(Internet)
Internet是目前世界上最大的计算机网络，是网络的网络（或者说是互连的网络），几乎覆盖整个世界的范围。该网络没有一个中心机构。
Internet网络的组建最初源于二十世纪60年代美国国防部高级研究计划局(ARPA)提出的ARPAnet，目的是为了研究部门和大学服务。二十世纪九十年代后，因特网面向社会，并得到飞速发展。

- 环球网(World Wide Web)
又称Web网、WWW or W3
1989年工作于欧洲物理粒子研究所的Tim Berners-Lee 发明了World Wide Web。他被称为WEB之父，也是W3C组织(World Wide Web Consortium)的领导人之一。
Web是一个大型的相互链接的文件所组成，范围包括整个世界，通过超文本链接，新手也可以轻松上网浏览。通过http协议进行通信的网络
使用者需要使用浏览器来浏览Web网页，所有的浏览器都使用http协议发起请求并从其他机器得到响应（即得到请求的网页）。

- 网络冲浪(Surfing the Web )
浏览Web网页
相关其他名词：
页面(page), 位置(place), 站点(site)
主页(homepage)

- 网页(Web Pages) 
ISP是“网络服务提供商(Internet Service Provider)”的缩写
ISP向广大用户提供互联网接入业务、信息业务等业务的电信运营商。
比如，如果你要建立一个Web站点，你需要注册一个网站名，并支付一定的费用给ISP。

- 浏览器(Browser)
- 服务提供商(Internet Service Provider)
- 客户端(Clients)& 服务器(Servers)
客户机(Client)是一个应用程序，他们同服务器(server)通信并从服务器请求获得信息。
服务器(Server)是一个给连接的客户机应用程序提供信息或其他资源的网络应用程序。
服务器需要及时的响应多个客户机的请求，因此通常运行在高性能的计算机上；而客户机对计算机资源的要求则不需要很高。

- 统一资源定位器(URL) 
- HTTP (Hypertext Transfer Protocol)
HTTP协议是 “超文本传输协议(Hypertext transport protocol)”的简称
HTTP协议是一种Internet协议，负责传输WWW信息，它定义了Web服务器如何回答信息请求，通过锚点(anchor)和URL构成。

- 搜索引擎(Search Engine)
搜索引擎(search engine)是一个对互联网上的信息资源进行搜集整理，然后供你查询的系统。包括信息搜索、信息整理和用户查询三部分。用户通过关键字(keyword)可以在网上搜寻所需的信息。
搜索网站(search site)使用搜索引擎提供搜索服务
Excite: www.excite.com 
AltaVista: www.altavista.com 
Lycos: www.lycos.com 
Google: www.google.com

## ※ 1.2 知识点
- DNS
DNS即域名系统(Domain Name System)，也成域名服务器(Domain Name Server)，它把域名转换称计算机能理解的IP地址（这个过程成为域名解析）。比如，如有你想访问武大网站(www.whu.edu.cn)，DNS即将www.whu.edu.cn转换称IP地址 “202.114.64.139”。
每一台联网的计算机都有一个DNS来解析域名。
- HTML
Hypertext markup language的缩写，是创建网页(Web page)所使用的语言。
由一般文本和标记(tag)组成，标记用于提示浏览器(browser)如何处理一条激活的链接。
HTML语言是SGML(标准化的一般标记语言)的子集。
- HTML标记 


##  ※ 1.3 请求-响应信息交互
- Session(会话)
 为了完成一个任务而进行的多个HTTP连接（客户机与服务器的信息交互）
- Cookie
Cookie是服务器发送给浏览器的体积很小的纯文本信息，用户以后访问同一个Web服务器时浏览器会把它们原样发送给服务器。通过让服务器读取它原先保存到客户端的信息，网站能够为浏览者提供一系列的方便，例如在线交易过程中标识用户身份、安全要求不高的场合避免用户重复输入名字和密码、门户网站的主页定制、有针对性地投放广告，等等。 

- 服务器推模式（server push）
  客户机－服务器的交互由服务器控制
  服务器主动给客户机发送数据，HTTP连接保持，直到服务器自己关闭连接，或者客户机中断 了连接。










