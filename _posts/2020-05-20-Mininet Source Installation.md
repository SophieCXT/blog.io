---
layout: post
title: Mininet Source Installation 
date: 2020-05-20
categories: blog
tags: Research
description: It's really confusing when I conducted the **Mininet Installation** recently. Actually the mininet.org is the tutorial on Youtube is limited as well. Also, it repository version is not matched with the Ubuntu Virtual Machine's python library so that there are dozens of bugs I encountered with. 
---


## Get started
- Ubuntu version:16.04
You can download this version on ubuntu's website.

![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-05-20.jpg)

- install git:
```
sudo apt install git
```
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-05-20-1.jpg)

- clone mininet repository:
```
git clone git://github.com/mininet/mininet
```
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-05-20-2.jpg)

- install begin:
```mininet/util/install.sh -a```

I want to consult about the deals, as I am a new client. However, I am not familiar with the websites contents. Could you please help me ?

## How to change the font size of XTerm? 
You can also Ctrl-Right mouse click for temporary change of font size


***Ref ***

- Installation Tutorial:
>https://www.youtube.com/watch?v=2jWs_9_1B8w
>
一秒解决虚拟机与主机之间粘贴复制

关闭虚拟机。虚拟机设置，选项，物理机隔离，把复制粘贴选上就ok
>https://blog.csdn.net/DDFFR/article/details/78740729
>
However, try to also specify your controller's IP like this :
For pingfail:
>https://stackoverflow.com/questions/53315404/mininet-pingall-fails
>https://stackoverflow.com/questions/35285262/ping-is-not-working-on-single-topology-created-on-mininet
`--controller=remote,ip=[CONTROLLER_IP]`

SDNlab:

>https://www.sdnlab.com/15096.html
>https://www.sdnlab.com/15077.html