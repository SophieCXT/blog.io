---
layout: post
title: SSD2-Review(Answer to unit 3, the outline of last post)
date: 2015-12-23
categories: blog
tags: [Study, Software Systems Development2(SSD2)]
description: SSD2 - Answer to unit 3, the outline of last post
---


# Unit3
## Software
Software consists of computer programs, support modules 模块, and data modules that work together to provide a computer with the instruction and data necessary for carry out a specific type of task, such as document production, video editing, or web browsing.
## 软件
能指示计算机完成任务的、以电子格式存储的指令序列和相关的数据。


## 编译器compiler
编译器把高级语言写成的指令变成机器语言写成的指令然后放在新文件里。
##interpreter 解释器
converts one instruction at a time while the program is running. More common with Web-based programs called scripts脚本, written in languages such as JavaScript and VBScript.根编译器差不多，不过是一边翻译语言一边运行程序，并不是生成新文件之后再运行。
## 源码
These languages help the programmer produce a lengthy list of instructions, called source code 


## 目标码
A compiler translates all of the instructions in a program as a single batch, and the resulting machine language instructions, called object code, are placed in a new file. 
## 机器指令Machine language
the instruction set that is “hard wired” within the microprocessor’s circuits.


## BIOS&CMOS
据说比较重要的是：存的是什么东西，特点，启动时各自的功能 步骤
CMOS Memory — configuration information used during the boot process互补金属氧化物半导体

## CMOS
是计算机主板上的一块可读写的芯片，里面存放的是关于系统的硬件配置情况和用户对某些参数的设定。CMOS芯片只有保存数据的功能，而对CMOS中各项参数的修改要通过BIOS的设定程序来实现。CMOS芯片由主板上的充电电池供电，即使系统断电，参数也不会丢失。
## BIOS
(基本输入/输出系统Basic Input / Output System)
BIOS是一组设置计算机硬件的程序，保存在主板上的一块ROM芯片中，它控制着系统全部硬件的运行，又为高层软件提供基层调用。它主要用于存放自诊断测试程序、系统载入程序、系统设置程序和主要I/O驱动程序及中断服务程序。自检测试完成后，系统将在指定的驱动器中寻找操作系统，并向内存中装入操作系统。BIOS程序在每次开机或者重启时便会自动开始运行。 
The BIOS, or Basic Input/Output System, is the most fundamental level of software. It deals directly with the signals that control each hardware component. Much of its work is performed when the computer is first turned on.
the lowest level of software on the machine.
操作系统和硬件之间连接的桥梁，负责在电脑开启时检测、初始化系统设备、装入操作系统并调度操作系统向硬件发出的指令。它实际上是被固化到计算机中的一组程序，为计算机提供最低级的、最直接的硬件控制。准确地说，BIOS是硬件与软件程序之间的一个“转换器”或者说是接口(虽然它本身也只是一个程序)，负责解决硬件的即时需求，并按软件对硬件的操作要求具体执行。  
基本输入输出系统（BIOS）是计算机开机后中心处理器用于启动计算机系统的程序。它管理操作系统中数据的流通以及各种外设，如：硬盘、显卡、键盘、鼠标和打印机。BIOS是计算机中不可缺少的部分。处理器通过ROM读取BIOS程序。当你打开计算机电源时，处理器就会读取存储在ROM中的BIOS程序。当BIOS程序启动你的计算机时，它首先检测所有的外设是否连接正确且能正常使用，然后从硬盘或软盘装载操作系统（或核心部分）到内存（RAM）。
three major functions:负责在电脑开启时检测
  1. initialize the hardware when the computer is   first turned on;初始化系统设备
  2. load the operating system;装入操作系统
  3. provide basic support for devices.调度操作系统向硬件发出的指令 
•	The BIOS is always present, but, it is only visible when you first power on the computer, before the operating system takes control

## 软件分层
User-Written Scripts or Macros用户编写的脚本或宏
User Interface用户界面
Application
Run-time Library执行时期链接库
Application Program Interface应用程序接口
Operating System
Kernel内核
Device Drivers
BIOS
(Hardware)

## Operating System
An operating system is essentially the master controller for all of the activities that take place within a computer.
操作系统是最底层的系统软件，它是对硬件系统功能的首次扩充，也是其它系统软件和应用软件能够在计算机上运行的基础。

## 操作系统具有五个方面的功能：
内存储器管理、处理机管理、设备管理、文件管理和作业管理。 
## Process
上课听到的关键词：进程 中断 中断的优先级 抢险多任务处理
A process is an instance of a running program. It includes a set of memory pages, a set of open file descriptors (if the process does any I/O), a process ID, and several other things.

## 进程
是指计算机运行中的一个实例。在Unix和其它操作系统中，当一个程序初始化之后进程就开始了。和任务一样，进程也是一个正在运行中的程序和一套特定的数据联系，以使进程能保持进行。当同时有多个用户使用一个程序时，这个程序只启动一个进程来执行每个用户的不同处理阶段。
## 线程
在计算机专业英语中，是相对于进程一概念而言的，进程可以看做是一个运行中的程序，而一个程序可以同时分为很多线进行，每一条线就是一个线程。在CPU一个瞬时只能处理一个线程的意义上，线程是基本执行单位。 
Each process can be in one of several states: running, runnable, or blocked. 
A blocked process is one that is waiting for some event to occur. 
The kernel maintains a queue 队列(also called the run queue), or waiting list of runnable processes. In order to give the illusion that all these processes are running at once, it uses a trick called preemptive multitasking抢先多任务处理. 


## Interrupt
An interrupt is a signal to the processor that some event has occurred that requires immediate attention.
中断是连接到计算机的设备或者是从计算机内部一个程序发出的信号，这个

## 程序是指计算机操作系统停止并判断下一步做什么的主程序。主要是指：　　　
   1）由于外部事件使得进程（例如一个计算机程序的执行）暂时挂起的现象，而且所中止的进程能够自动恢复正常的运行　　
   2）按照可重新恢复运行方式去停止一个进程；　　
   3）在数据传输中，接收站采取行动使发送站终止传输工作。


## nested interrupt

The second interruption is nested (嵌套的) inside the first.
An interrupt handler can only be interrupted by a higher priority interrupt. 

## interrupt Priority中断优先权
The processor also assigns priorities to different types of interrupts. 


## 虚拟内存virtual memory
虚拟内存的概念是相对于物理内存而言的，当系统的物理内存空间入不敷出时，操作系统便会在硬盘上开辟一块磁盘空间当做内存使用，这部分硬盘空间就叫虚拟内存。
提供比实际上各大的物理内存 
                                                                          缺点 速度小于物理内存
                                                                          需要特定的软硬件支持
                                                                          频繁读写硬盘引起程序错误

## Page fault
An invalid page fault or page fault error occurs when the operating system cannot find the data in virtual memory. This usually happens when the virtual memory area, or the table that maps virtual addresses to real addresses, becomes corrupt. 
## table 

.txt 	Plain text file            文本文件
.doc 	Microsoft Word document    Word文档
.htm 	HTML (Hypertext Markup Language) document
超文本链接标示语言文档
.xls 	Microsoft Excel spreadsheet  Excel文档
.gif 	GIF image (Graphic Interchange Format)
.jpg 	JPEG image (Joint Photographic Experts Group)
.wav 	Sound file
.exe 	Executable file (binary machine code)        可执行文件
.com 	MS-DOS executable ("command" file)       命令程序文件
.drv 	Driver (for a peripheral device)                驱动程序文件
.bat 	Batch (script) file for the DOS command interpreter
批处理文件
