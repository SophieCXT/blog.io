---
layout: post
title: linux cp复制/移动多个文件操作
date: 2020-06-26
categories: blog
tags: Research
description: It's really confusing when I learn the SDN terms. Here is one I think we should pay attention.
---
Ref:
>https://blog.csdn.net/re_call/article/details/105860821
>https://blog.csdn.net/qinglu000/article/details/9292417
>https://blog.csdn.net/zdb292034/article/details/82378800

在linux中，经常使用cp复制文件或文件夹。

##基本操作
最简单的把文件a复制到文件夹file_a中，使用：

cp a file_a，即可。

##复制多个文件
想把多个文件如a，b，c复制到文件夹file_a中，使用：

cp a b c file_a，即可。

##复制一个文件夹下的多个文件
如果我们想把文件夹file_a中的多个文件，如a，b，c复制到文件夹file_b中，该怎么办呢？

用最土的方法，cp file_a/a file_a/b file_a/c file_b，即可。我们可以看到我们把a，b，c文件的路径都写了一遍。 我们很容易想到能不能不用重复写相同的文件路径呢？答案是可以的，方法如下：

cp file_a/{a,b,c} file_b，即可。注意大括号中的文件是用逗号分开的。

大括号里面可以添加要复制的文件或者文件夹。

##复制名称相似的多个文件
如果想把文件a_1,a_2,a_3,a_4复制到文件夹file_a中，可以用如下方法：

cp a_[1-4] ./file_a，即可。

如果选择复制文件a_1，a_2，a_4到文件夹file_a中，可以用如下方法：

cp a_[1,2,4] ./file_a，即可。
————————————————
版权声明：本文为CSDN博主「re_call」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/re_call/article/details/105860821

#linux下mv 多个文件到各自文件夹，如何操作？

1. mv可以把多个文件移动到一个文件夹(目录)里面，比如：有a b c三个文件，一个目录d，用下面命令就能将a b c移动到d中
$ mv a b c d
需要注意的是，目录d必须在最后面，而且它前面不能再出现其他目录

2. 也可以使用带选项的mv命令，把多个文件移动到一个目录中，如
$ mv a b c -t d
$ mv -t d a b c
其中，-t后面紧接着的就是要移动到的目录，并且不能有多个目录出现

3. 如果出现了多个目录，比如下面的命令
$ mv -t adir a -t bdir b
mv: multiple target directories specified
会出现上面的警告，且只执行了前面正确的那部分，即只是将a移动到了adir，后面的没执行

4。如果你的文件和目录名称有一定的关系，你的问题可以通过脚本来解决，当然，脚本的具体内容也要视具体情况而定
假设有文件a b c，希望将a移动到adir，将b移动到bdir，将c移动到cdir，那么就可以这样来做
写一个简单shell脚本:move.sh
# FileName move.sh
#!/bin/bash
mv $1 "$1dir"

$ chmod +x move.sh
然后，
$ find . -type f | xargs -n 1 ./move.sh
执行完毕之后，就发现
$ tree
.
|-- adir
| `-- a
|-- bdir
| `-- b

即实现了将a移动到adir，b移动到bdir，c移动到cdir了。

#Linux下同时复制多个文件

使用cp命令：需要注意的是这几个文件之间不要有空格
cp /home/usr/dir/{file1,file2,file3,file4} /home/usr/destination/