---
layout: post
title: Tips in Research(II)
date: 2020-07-08
categories: blog
tags: Research
description:
7. 将CMD信息保存为文件
8. What is Monte Carlo Simulation?
9. Soft Wraps in Pycharm
10. wireshark
 
---



## 将CMD信息保存为文件
在使用Windows中的cmd.exe工具时，有时候我们想要把我们的输入命令及结果保存起来，但是用复制的方法过于麻烦；有时输出数据条数过大，会造成内容自动滚出屏幕，无法阅读，我们可将命令运行的结果输出到文本文件。如何将cmd中命令输出为TXT文本文件呢？
老实孩子教给大家一个方法：
在你输入命令后再加上“>”和你想保存的文件地址和名字就行了。
`例如：将Ping命令的加长包输出到D盘的ping.txt文本文件。`
1、在D:\目录下创建文本文件ping.txt（这步可以省略，偶尔提示无法创建文件时需要）
2、在提示符下输入`ping www.idoo.org.ru －t > D:\ping.txt`
3、这时候发现D盘下面的ping.txt里面已经记录了所有的信息
备注：
只用“>”是覆盖现有的结果，每一个命令结果会覆盖现有的txt文件，如果要保存很多命令结果的话，就需要建立不同文件名的txt文件。
那么有没有在一个更好的办法只用一个txt文件呢？答案是肯定的，要在同一个txt文件里面追加cmd命令结果，就要用“>>”替换“>” 就可以了.
 
linux命令行同样可以这样操作，只是将“D:\ping.txt”替换为系统内部存储空间：
`logcat -v time > /sdcard/logcat.txt
 `
参考：
>如何将cmd中命令输出保存为TXT文本文件_zhanghongyas_新浪博客

## What is Monte Carlo Simulation?
Monte Carlo simulation is a computerized mathematical technique that allows people to account for risk in quantitative analysis and decision making. The technique is used by professionals in such widely disparate fields as finance, project management, energy, manufacturing, engineering, research and development, insurance, oil & gas, transportation, and the environment.
Monte Carlo simulation furnishes the decision-maker with a range of possible outcomes and the probabilities they will occur for any choice of action. It shows the extreme possibilities—the outcomes of going for broke and for the most conservative decision—along with all possible consequences for middle-of-the-road decisions.
The technique was first used by scientists working on the atom bomb; it was named for Monte Carlo, the Monaco resort town renowned for its casinos. Since its introduction in World War II, Monte Carlo simulation has been used to model a variety of physical and conceptual systems.

## Soft Wraps in Pycharm

Soft-wrap these files
Use this field to apply soft wraps to specific file types (For example, it might be helpful when you are writing documentation in markdown files). Enter file extensions separating them with semicolon.
You can also enable or disable soft wraps right in the editor:
Right-click the left gutter and from the context menu, either select or clear the Soft-Wrap Current Editor option. Keep in mind that these settings affect only the current editor, not a file.

## wireshark

I got the same error like the ones mentioned in the question. 

In my fix(after you ssh -X usernme@ipaddress), I changed to directory mininet/util and ran the shell script install.sh. So basically 
```
1. cd mininet/util.   
2. sh install.sh.     
3. "sudo wireshark &".     to start wireshark and you will get warning, just hit Ok
```