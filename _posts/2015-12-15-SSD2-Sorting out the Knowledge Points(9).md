---
layout: post
title: SSD2-Review(Answer to unit 4, the outline of last post)
date: 2015-12-24
categories: blog
tags: Software Systems Development2(SSD2)
description: SSD2 - Answer to unit 4, the outline of last post
---


# Unit4
## Wildcard characters通配符
Certain commands accept a list of file names. Rather than typing in an actual list, it is often easier to use an asterisk ( * ) within a file name specification to get the command processor to generate a list of file names for us. An asterisk ( * ) acts as a wildcard character that can match any number of characters in a file name.
Here are some examples of an asterisk used as a wildcard character with the dir command
- List only those files and folders in the root folder whose names start with "n":
dir c:\n* 
- List only those files and folders in the root folder whose names end with "n":
dir c:\*n 
- List only those files and folders in the root folder whose names contain an "n" anywhere:
dir c:\*n * 
Using the asterisk wildcard would give more unrelated responses than the question mark in these situations. The "?" is most often used when referring to a group of files with names that are similar
## redirection重定向符号 
On a PC, the command processor coordinates with the operating system to redirect all data from the keyboard driver to the Standard Input virtual device and all data from the Standard Output virtual device to the display driver. Redirection allows the user to change this. 
List all files in the root folder to the printer instead of the display:
dir c:\*.* >lpt: 

## Dos command:help(/?).dir.type.del.md.cd.ren.. 
the DOS command-line user interface 
开始—运行— 输入cmd，确定即可进入

cd	Change the working directory. 
md	Make a new directory.
rd	Remove an existing empty directory. 
deltree	Remove an existing directory and its contents. 
attrib	Change a file's attributes
copy	Make a copy of a file. 
xcopy	Make a copy of files and sub-directories.
ren	Rename a file within a directory.
move	Move a file from one drive/directory to another.
del	Delete files. 
dir	List files in a directory.
type	Display the contents of a text file.

## Batch file
Batch files are text files containing DOS commands used to run programs and manipulate files.
批处理文件是文本文件，它包含一组有次序的系统操作指令。之所以叫它批处理文件，是因为它将一组命令打包成一个单独的文件，而这些命令本身是要通过键盘与用户进行交互的。当用户需要按一定顺序重复执行某些命令的时候就可以使用批处理文件。操作系统中一般包含有批处理文件。你可以在命令提示符下直接键入批处理文件的文件名来执行它。　


## Software engineering
Software engineering is a body of techniques for the disciplined creation and maintenance of large, complex software systems, usually by teams of programmers.
软件工程是研究和应用如何以系统性的、规范化的、可定量的过程化方法去开发和维护软件，把经过时间考验而证明正确的管理技术和当前能够得到的最好的技术方法结合起来。

## Issues in Large-Scale Software Development
The Software Development Process 
Define or Redefine the Problem 
Plan a Solution to the Problem 
Code the Solution 
Evaluate and Test Everything 

## The Software Development Process

•	Define or redefine the problem. 
•	Plan a solution to the problem. 
•	Code the solution. 
•	Evaluate and test everything.
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/WHU/2015-12-24.png)
## Open source
open source software开放源码软件被定义为描述其源码可以被公众使用的软件,并且此软件的使用,修改和分发也不受许可证的限制。开放源码软件通常是有copyright的，它的许可证可能包含一些限制。
开放源码软件（Open source software）表示软件的开发、测试以及维护过程都在公众协议下进行，而且其发布采取共享方式，同时还要保证在软件发布之后仍然保证开源性质。整个开发组织包括众多开发人员，其中以研究机构的人员居多，

## public domain software
公开领域中的程序，由于作者希望和别人共享，所以没有申请版权公开领域中的程序可以不受限制的被用作其他程序的一部分。当重复使用如此的源代码时，最好是了解它的历史以便你能确定它真的是在公开的领域中。 



## Shareware
共享软件是一种免费发放的试验软件，用户以后可能需要或者花钱买这些软件。有些软件开发者提供带有内置截止日期的共享软件（30天以后，用户再也不能访问该程序）。其它共享软件禁用了一些功能，以引诱用户购买程序的完整版本。　　 
免费提供的程序称免费软件。然而，它受版权保护，你不能将其程序并入你正在开发的任何程序。限制最少的免费程序为不受版权保护的公共软件程序，包括许多小的UNIX程序。在你的程序中再次使用公共软件时，你最好了解一下程序的历史，以确认它确实是公共的。


