---
layout: post
title: Tips in Research
date: 2020-07-05
categories: blog
tags: Research
description: 如何快速在线生成latex表格\How to exit Startx?\How to push large files in github**(not matured than dropbox and onedrive)**\How to Fix Server Not Found Error in Ubuntu in Vmware Workstation\Matlab readfile in pile\MATLAB中的常用清除命令有哪些

---


1. 如何快速在线生成latex表格
2. How to exit Startx?
3. How to push large files in github**(not matured than dropbox and onedrive)**
4. How to Fix Server Not Found Error in Ubuntu in Vmware Workstation
5. Matlab readfile in pile
6. MATLAB中的常用清除命令有哪些
## 如何快速在线生成latex表格

 `https://www.tablesgenerator.com/`
使用Table Generator，笔者发现国内访问有困难，大家节哀，文末会提供一些境内访问方法。
第一步：建表
复制word表格内容到excel里面，然后复制在excel里面的表格到这个位置：
也可以直接导入CSV
 
Ctrl+鼠标Right Click。
可以看到菜单，然后调整。


## How to exit Startx?
To exit nano file you need to press Control + X Which will exit nano, after prompting whether you want to save any changes to the file. You can also press Control + G to view the help file with the list of commands.

## How to push large files in github**(not matured than dropbox and onedrive)**
```
curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
sudo apt-get install git-lfs
git lfs install
```
## How to Fix Server Not Found Error in Ubuntu in Vmware Workstation

>[https://www.youtube.com/watch?v=rBflOiBjuys]


在数据库中，schema（发音 “skee-muh” 或者“skee-mah”，中文叫模式）是数据库的组织和结构，schemas andschemata都可以作为复数形式。模式中包含了schema对象，可以是表(table)、列(column)、数据类型(data type)、视图(view)、存储过程(stored procedures)、关系(relationships)、主键(primary key)、外键(foreign key)等。数据库模式可以用一个可视化的图来表示，它显示了数据库对象及其相互之间的关系

>[https://www.howtogeek.com/261383/how-to-access-your-ubuntu-bash-files-in-windows-and-your-windows-system-drive-in-bash/]

## matlab readfile in pile
https://blog.csdn.net/rosefun96/article/details/78964425
filepath='G:\traindata\';%文件夹的路径
 for i=0:21  %n是要读入的文件的个数
      dataname=['d0' num2str(i) '.dat']
      chr=[filepath dataname]
      d0=load(chr)
      figure;
      plot(1:length(d0),d0);
      clear(chr)
      clear(dataname)
 end
————————————————
版权声明：本文为CSDN博主「rosefunR」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/rosefun96/article/details/78964425

## MATLAB中的常用清除命令有哪些

1.clc命令：即可清空命令窗口中的内容。
2.clf命令：清除当前figure中的内容。
3.close命令：关闭当前打开的figure图形界面。
4.clear命令：清空workspace中的变量。
5.exit命令：退出MATLAB，执行后直接退出软件。
————————————————
版权声明：本文为CSDN博主「魏波-」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/weibo1230123/article/details/77153302
