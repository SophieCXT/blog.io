---
layout: post
title: SSD2-Review(Answer to unit 5, the outline of last post)
date: 2015-12-25
categories: blog
tags: [标签一,标签二]
description: SSD2 - Answer to unit 5, the outline of last post
---


# Unit5

## Internet
internet 是普通名词
–	泛指一般的互连网（互联网）
Internet 是专有名词
–	世界范围的互连网（互联网）
–	使用 TCP/IP 协议族
因特网是世界上最大的计算机网络，


## Internet languages
HTML Hyper Text Markup Language超文本标识语言
XML eXtensible Markup Language可扩展标记语言
JavaScript 
Java 

## LAN
LAN (Local Area Network局域网):在一个相对有限的地理范围内，由一组PC、服务器、打印机和类似的设备连接组成的网络。
局域网的特点是：
•	为一个单位所拥有，且地理范围和站点数目有限
•	所有的站共享较高的总带宽（即较高的数据传输率）
•	较低的实验和较低的误码率
•	各站为平等关系而不是主从关系
•	能进行广播（已占祥其他所有站发送）或多播（multicast,一站向多站发送，又称为组播）

## C/S
Many network applications are organized as client-server systems. The client runs on the user's computer and interacts with both the user and the server. 
The server can accept requests from any number of clients. It performs some service for them and returns the results. 
Example: World Wide Web
 

## P2P
Peer-to-peer (P2P). Instead of having a central server that all clients communicate with, every member of a peer-to-peer network can communicate with any other member. 
## HUB
也就是集线器。它的作用可以简单的理解为将一些机器连接起来组成一个局域网。
##  Switch
交换机（又名交换式集线器）作用与集线器大体相同。但是两者在性能上有区别：集线器采用的是共享带宽的工作方式，而交换机是独享带宽。这样在机器很多或数据量很大时，两者将会有比较明显的。而路由器与以上两者有明显区别，它的作用在于连接不同的网段并且找到网络中数据传输最合适的路径 ，可以说一般情况下个人用户需求不大。
## router
Router（路由器）是一种连接多个网络或网段的网络设备，它能将不同网络或网段之间的数据信息进行“翻译”，以使它们能够相互“读”懂对方的数据，从而构成一个更大的网络。 
路由器有两大典型功能，即数据通道功能和控制功能。 
路由器是产生于交换机之后，就像交换机产生于集线器之后，所以路由器与交换机也有一定联系，并不是完全独立的两种设备。路由器主要克服了交换机不能路由转发数据包的不足。

## URL
Every Web page has a unique address called a URL (Uniform resource 
## locator统一资源定位符
Most URLs begin with http://
URL 实际上就是文档在因特网中的地址。

## Domain name
因特网的域名Domain Name
域名服务器 DNS (Domain Name Server)
因特网中设有很多的域名服务器 DNS，用来把域名转换为 IP 地址。
例如，DNS 收到 www.cctv.com 后，经过查询过程，就把这个域名转换为 IP 地址：
       11001010011011001111100111001110


## Protocol:
在计算机网络中，协议(protocol)是通信双方必须严格遵守的规则。
–	协议也就是网络协议。
协议精确地规定在网络通信中使用的各种控制信息的格式、意义以及各种事件出现的先后顺序。


## TCP 协议保证了应用程序之间的可靠通信
TCP 给要传送的每一个字节的数据都进行编号。
–	接收端在收到数据后必须向发送端发送确认信息。
–	若发送端在规定的时间内没有收到对方的确认，就重传这部分数据。
当网络中的通信量过大时，TCP 就告诉发送端要放慢发送数据。这叫做流量控制。


## IP Internet Protocol 
因特网的 IP 协议最重要，它为分组在互连网中的发送、传输和接收制定了详尽的规则。
## IP: 网际协议
IP 协议控制分组在因特网的传输但因特网不保证可靠交付
TCP/IP协议不但包含了TCP和IP协议，还包含了许多其它协议(TCP、IP、UDP、ARP、 FTP、TELNET、SMTP、ICMP等)，这些协议全应用于计算机通信领域，所以通常统称它们为TCP/IP协议。
通常用 TCP/IP 这样的记法表示以 TCP 和 IP 为核心的协议族。


## HTTP
HTTP (hypertext Transfer Protocol超文本传送协议 ) is the communications standard that’s instrumental in ferrying Web documents to all corners of the Internet.


## TCP: 传输控制协议(Transmission Control Protocol)

## SMTP 
   发送邮件使用的协议——简单邮件传送协议
SMTP (Simple Mail Transfer Protocol)

## POP3(Post Office Protocol version 3)
接收邮件使用的协议——邮局协议版本3
## M I M E:

It is possible to attach images and other types of documents to an email message.
This raises a problem: how is the mail client (that is, an application that reads
email) supposed to know what to do with these documents? The solution is to give
each attachment a label explaining what kind of document it is. The labels are
called MIME types. Incidentally, MIME is the acronym for Multipurpose Internet
Mail Extension.
MIME type designations have two components: a type and a subtype, which are
separated by a slash (/). Some examples include text/plain, text/html, image/gif,
image/jpeg, and application/msword. Users can control how their mail clients
handle attachments of a given type through a configuration file called a MIME
types file. For example, they may specify that GIF and JPEG images should be
displayed using a particular viewer program, or that files associated with the
application/msword type should be opened immediately using Microsoft Word


