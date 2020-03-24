---
layout: post
title: Introduction to Mininet(Including Installation and Environment Setting) 
date: 2020-03-24
categories: blog
tags: Research
description: It's really confusing when I conducted the **Mininet VM Installation** recently. Actually the mininet.org is the tutorial on Youtube is limited as well.
---


# Get started
The first website we refers is: 
> http://mininet.org/download/.

I choose the option 1 so that this tutorial is aiming at Mininet VM Installation on Win 10. 

## Download
- Mininet VM(Virtual Machine) image.
  1.  Download the Mininet VM from the following website, finding the VM that suits you:  
  > https://github.com/mininet/mininet/releases
                                                        
  Here I choose: `mininet-2.2.2-170321-ubuntu-14.04.4-server-amd64.zip` because my computer is win 10, 64 bit.
  2. Right click the zip file to 'extract all' in the directory you want, you will get these two files: 
  ![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-24.PNG)

---
- VirtualBox
  1.  find the platform that suits you:  
  > https://www.virtualbox.org/wiki/Downloads. 
                                                        
  Here I choose:VirtualBox 6.1.4 platform packages
 ->_Windows hosts_.
  2. double click yor download file: `VirtualBox-6.1.4-136177-Win`
  3. use its default setting.(you can change the folder from `C:/` to `D:/` if you want.)
  4. launch the software, you will seccessfully see the following UI:
   ![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/VBUI.PNG)


## Run the VM on VirtualBox
The next step's website we refers is: 
>http://mininet.org/vm-setup-notes/
1. launch VirtualBox
2. double-click on the `mininet-2.2.2-170321-ubuntu-14.04.4-server-amd64.ovf ` file, the VirtualBox will automatically generate the following config:
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/20200324.PNG)
3. change the `machine base folder` (I set D:\research_TingLab\TestMininet )to the location you want and click `import`.
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-24import.PNG)
4. wait a few seconds, you will get the VM in your VirtualBox Manager:
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-24suc.PNG)
6. add a host-only network interface to your VM: 
     - click `setting`
     ![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-24-01.PNG)
     - click `Network`, don't change the Adapter 1(it will be initial ethernet 0). click Adapter 2 and check `Enable Network Adapter`. Then choose host-only like below:
     ![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-24-02.PNG)
    - click 'OK'
5. double-click or click the `Start` button to run the VM.
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-24-03.PNG)


## Log in to VM

Log in to the VM, using the following name and password:
```
mininet-vm login: mininet
Password: mininet
```
It runs like this:
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-24-04.PNG)

## SSH into VM
First, find the VM’s IP address, which for VMware is probably in the range 192.168.x.y. In the VM console:
```
ifconfig eth0
```
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-24-05.PNG)
You will see the `inet addr` is 192.168.56.102(You may get a different ip address, don't worry, that's normal)

Note: As we VirtualBox users have set up a host-only network on `eth1`, we then should use:
```
sudo dhclient eth1   # make sure that eth1 has an IP address
ifconfig eth1
```
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-24-06.PNG)


***Now you can do whatever you want! The links below are some references for your further development! ***









