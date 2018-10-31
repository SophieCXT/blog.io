---
layout: post
title: SSD2-Review(The answer of the last post)
date: 2015-12-21
categories: blog
tags: [Software Systems Development(SSD),SSD1]
description: SSD2 
---

## Unit 1
Computer 
A computer is an electronic machine that performs input, processing, storing, and output according to programmed instructions to carry out specific tasks. 

Bit 
Each binary（二进制）digit （数字）is called a bit. 比特,度量信息的最小单位

Byte
Eight bits is one byte字节

Decimal
十进制

Binary
二进制

Hexadecimal
十六进制
0	1	2	3	4	5	6	7	8	9	10	11	12	13	14	15
0	1	2	3	4	5	6	7	8	9	A	B	C	D	E	F

0x后面跟着一串数字和英文的就是指十六进制拉
 

## Unit2
Four steps 
1. Fetch 取指- The control unit gets the instruction from memory.
2. Interpret 解码- The control unit decodes what the instruction means and directs the necessary data to be moved from memory to the ALU.
3. Execute 执行- The control unit directs the ALU to perform the necessary arithmetic or logic operations.
4. Store 存储- The result of the computation is stored in memory.

Register,Cache,RAM,Hard disk
按顺序容量越来越大，读取速度越来越慢，单位容量越来越便宜
register寄存器是中央处理器内的组成部分。寄存器是有限存贮容量的高速存贮部件，它们可用来暂存指令、数据和位址。在中央处理器的控制部件中，包含的寄存器有指令寄存器(IR)和程序计数器(PC)。在中央处理器的算术及逻辑部件中，包含的寄存器有累加器(ACC)。
　　寄存器是内存阶层中的最顶端，也是系统获得操作资料的最快速途径。寄存器通常都是以他们可以保存的位元数量来估量，举例来说，一个 “8 位元寄存器”或 “32 位元寄存器”。　　寄存器通常都用来意指由一个指令之输出或输入可以直接索引到的暂存器群组。更适当的是称他们为 “架构寄存器”。 
　　例如，x86 指令集定义八个 32 位元寄存器的集合，但一个实作 x86 指令集的 CPU 可以包含比八个更多的寄存器。
　　寄存器是CPU内部的元件，寄存器拥有非常高的读写速度，所以在寄存器之间的数据传送非常快。 

特点及原理
　　寄存器又分为内部寄存器与外部寄存器，所谓内部寄存器，其实也是一些小的存储单元，也能存储数据。但同存储器相比，寄存器又有自己独有的特点： 
　　①寄存器位于CPU内部，数量很少，仅十四个；
　　②寄存器所能存储的数据不一定是8bit，有一些寄存器可以存储16bit数据，对于386/486处理器中的一些寄存器则能存储32bit数据；
　　③每个内部寄存器都有一个名字，而没有类似存储器的地址编号。
　　寄存器的功能十分重要，CPU对存储器中的数据进行处理时，往往先把数据取到内部寄存器中，而后再作处理。外部寄存器是计算机中其它一些部件上用于暂存数据的寄存器，它与CPU之间通过“端口”交换数据，外部寄存器具有寄存器和内存储器双重特点。有些时候我们常把外部寄存器就称为“端口”，这种说法不太严格，但经常这样说。
　　外部寄存器虽然也用于存放数据，但是它保存的数据具有特殊的用途。某些寄存器中各个位的0、1状态反映了外部设备的工作状态或方式；还有一些寄存器中的各个位可对外部设备进行控制；也有一些端口作为CPU同外部设备交换数据的通路。所以说，端口是CPU和外设间的联系桥梁。CPU对端口的访问也是依据端口的“编号”（地址），这一点又和访问存储器一样。不过考虑到机器所联接的外设数量并不多，所以在设计机器的时候仅安排了1024个端口地址，端口地址范围为0--3FFH。 
寄存器用途
　　1.可将寄存器内的数据执行算术及逻辑运算；
　　2.存于寄存器内的地址可用来指向内存的某个位置，即寻址；
　　3.可以用来读写数据到电脑的周边设备。(摘自百度百科)

cache高速缓冲存储器
Cache, a special high-speed memory that stores most recently used data in order to speed up the process of instruction execution.
一种特殊的存储器子系统，其中复制了频繁使用的数据，以利于CPU快速访问。高速缓冲存储器存储了频繁访问的RAM位置的内容及这些数据项的存储地址。
RAM (random access memory) is a temporary 临时的 holding area for both data and instructions. It is also referred to as main memory主存.  通常所说的内存
the data in RAM is lost when the computer is turned off. 


RAM,ROM（Read-only memory）
内存储器位于主板上，分为随机读\写存储器（RAM）、只读存储器（ROM）
RAM — instructions to be executed when the computer is running
ROM — instructions needed to boot start a computer
RAM is measured by its memory capacity and latency(access time存取时间) 
DRAM动态随机存取存储器 - Dynamic RAM, a common type of RAM, made of an integrated circuit (IC), 优点是高密度和较低的成本，缺点是耗电量比较大。
SDRAM同步动态随机存取存储器 (Synchronous Dynamic RAM) used in many personal computers. It is fast and relatively inexpensive.目前奔腾计算机系统普遍使用的内存形式。SDRAM是目前最快的内存芯片，同时也是奔腾II和奔腾III计算机系统首选的内存条。
DDR SDRAM双数据率同步动态随机存取存储器A faster version of SDRAM is DDR SDRAM (Double Data Rate SDRAM), which transfers twice the amount of data per clock cycle compared to SDRAM. Its capacity is up to 2 GB. DDR(双数据率) 是SDRAM的更新换代产品，具有比SDRAM多一倍的传输速率和内存带宽
RDRAM (Rambus Dynamic RAM存储器总线式动态随机存储器), which has a higher bandwidth than SDRAM, but it is more expensive compared to SDRAM
SRAM静态随机存取存储器Static RAM is a type of RAM that uses transistors to store data，it is faster than DRAM，it holds fewer bits and costs more compared to DRAM of the same size. SRAM is appropriate for use in the cache because it is fast and cache does not require a large memory capacity. 
- Type of RAM	Capacity	Price
SDRAM	@@	$
DDR SDRAM	@@@	$
RDRAM	@@@	$$
SRAM	@	$$$
- ROM 只读存储器Read-only memory一次性制造，其中的代码与数据将永久保存，并且不能够进行修改。一般应用于PC系统的程序码、主机板上的 BIOS (基本输入/输出系统Basic Input / Output System)等。它的读取速度比RAM慢很多。
- EEPROM--electrically erasable programmable read-only memory电可擦可编程只读存储器具有可擦除功能，擦除后即可进行再编程，以约20V的电压来进行清除数据。另外它还可以用电信号进行数据写入。这类ROM内存多应用于即插即用（PnP）接口中。Flash memory快闪存储器is a type of EEPROM 
- - MROM: mask-programmed ROM, programmed when being manufactured.
- - PROM: programmable ROM, one-time programmable ROM using PROM programmer/burner by end users.
- - EPROM: erasable PROM, strong ultraviolet light erasable in bulk. 
- - EEPROM: electrically EPROM, erased by electrical signals and reprogrammed. Individual location.
- - Flash memory: take advantages of EPROM and EEPROM
 
- Mass storage:CD(-R,-ROM,-RW),VCD,DVD
- 磁、光存储器的定义
- 硬盘、软盘、磁带等应用的是磁存储器原理，他们用磁性微粒存储数据，当数据存储时，磁性微粒被磁化，读写头用来读写磁性微粒代表的数据
- CD、VCD存储技术应用的是光存储原理，他们用光盘表面的凹凸不平的亮点和黑点存储数据，用激光读取数据。激光将扫射到的亮点和黑点翻译成数据。
- 磁、光存储的优缺点
光：抗干扰 保存更持久，好像没什么缺点
磁：读写速度快、不能靠近有磁性的物体，容易被磁化
CD 670MB
DVD 4.7GB
- 为什么VCD比CD容量大
原因有二：VCD用蓝光读取数据，track更窄，CD用红光读取数据
          蓝光频率高，能量大，能够穿透更多的层数，所以VCD比CD层数多
些
- Expansion slot扩充插槽A connector in a computer into which an expansion card can be plugged. The connector supplies power to the card and connects it to the data bus, address bus and control signals of the motherboard
- A PCI (Peripheral Component Interconnect周边元件扩展接口) slot can hold a variety of expansion cards such as a sound card or an Ethernet card 用来插声卡和网卡~
- An AGP (Accelerated Graphics Port加速图形接口) slot is primarily used for graphics cards用来插显（也叫图形加速卡）
- An ISA (industry standard architecture工业标准结构) older technology, used today for some modems and other relatively slow devices
- A PCMCIA (personal computer memory card international association 个人计算机存储卡国际协会) slot, CardBus cards or PC cards in laptops给本本用的

- Expansion card,扩展卡it is used to extend the capability of a computer. E.g.: sound card, video card 
- Graphics card- 图形加速卡，也就是显卡。video card, transforms images into analog data. 
- Sound card- 声卡allows a computer to play sounds such as music from CDs, sound files, games, or DVDs. It can also record sounds 
- Modem调制解调器（它能把数字信号转化为电信号的俗称猫）A modem converts the binary data into analog data-- data in binary form is sent out through a modem before transmitting it through a phone line or a cable line
- Ethernet card- 网卡serves as the interface to a Local Area Network (LAN)

- Expansion port端口(USB,firewire)connector between the expansion card and the peripheral device. For example, a video card provides a monitor port. 
 - 主机主要由CPU、内存、总线、输入 \输出设备（简称I\O接口）和扩展槽等构成。通常制成一块印刷线路板，称为主板。
- A serial port 串行端口 transfers data one bit at a time
- PS/2 port for keyboard and mouse connections，are gradually being replaced by USB ports.
- DB-9 port, another type of serial port, is also becoming obsolete过时. PDA devices used to connect to DB-9 ports before the advent of USB ports. 
- a parallel port 并行端口transfers one byte at a time. A parallel port is typically used to connect a computer to a printer. 
- Universal Serial Bus (USB) （好像要考全称）Up to 127 devices can be connected to the system unit via a USB hub, which provides multiple USB ports: mouse, keyboard, joystick操纵杆, scanner, printer, digital camera, and hard disk drive. 
- "hot connectivity" allows peripherals to be connected to the system, configured, and used without restarting the machine. 
- USB has become the replacement for serial and parallel ports
- FireWire 火线FireWire has a faster data transfer rate (FireWire is 50 MBps, USB is 1.5 MBps), and it supports up to 63 devices. FireWire is intended for data-intensive devices such as DVD players and digital camcorders. 速度比USB快
- Supports "hot connectivity", but more expensive 
 

I/O devices
- Input Devices 
- Cameras 相机
- Digital Camcorders 数码手提摄录机
- Scanners 扫描仪
- Output Devices: Monitors and Projectors 
- CRT Monitors 阴极射线管显示器（纯平）
- LCD Monitors 液晶
- Projectors 投影仪
- Output Devices: Printers 
- Ink Printers 喷墨打印机
- Dye-Sublimation Printers 热升华打印机
- Laser Printers 激光打印机
The most common input devices are the mouse and the keyboard. 
Monitors and projectors are typical devices to view outputs on a screen
 
a laser printer will offer the lowest cost per page (cpp) of all printers, making them economical in the long run, but with a large up front cost for the equipment. 
Benchmark基准：comparing disparate systems or components via a standardized set of instructions or series of tasks
Moore’s Law：硅晶元每平方英寸所能容纳的晶体管数每18个月将增加一倍，直到物理极限达到。其他的也是

 Bottleneck瓶颈影响性能最薄弱的环节 通常是cache RAM显卡 I/O设备
- Cache：Faster processors requiring more data input to run optimally may not receive enough data from small caches.
- RAM ： loads instructions from programs on disk. Therefore if there is not enough RAM memory, instructions will need to be loaded frequently from disk slowing down the execution of program instructions.
- I/O ： covers information transfer. Are the buses fast enough? Is the hard drive fast enough? The components may be able to send the data quickly enough, but if the system cannot transfer the data just as quickly, the system slows down.
- Video card：the slow 3-D rendering frame-rates produced by slower cards may hamper the performance of some applications.

- Data compression 
