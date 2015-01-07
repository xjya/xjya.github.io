---
layout: post
title: "Windows、Linux双系统安装并全盘加密"
date: 2015-01-06 12:06
categories: 進芫
permalink: /windows-linux-dual-boot-with-full-disk-encryption.html
---

这个问题曾经最好的解决方案是TrueCrypt，没有之一。它的影子系统至今没有同类软件能实现相同功能。  
自从TrueCrypt停止更新，事情开始变得扑朔迷离。  
我们不去探究TrueCrypt是否存在阴谋，单单探讨其它的解决方案。  

在两块硬盘上加密安装Windows、Linux系统非常easy，毫无难度。  
在一块硬盘上稍有点难度，也就是这篇教程所要讲述的内容。
我在一块120gb的ssd上安装了Win8.1和Debian 7双系统，本文以此为例。  
部分较简单的步骤请自行网上搜索教程。  

##1. 分区  
Windows必须留有启动分区，Win7约100mb，Win8约350mb。  
Linux必须单独分出/boot分区，300mb就足够。  
其它按照个人喜好来分。

##2. 安装  
1. 安装Windows到C盘。  
2. 启动Windows后，使用BitLocker加密C盘和D盘。  
3. 安装Debian，创建加密分区，使用lvm在加密分区中分出/和swap。  
上面的步骤都是网上容易找到的教程，接下来的一步是重点  
4. **安装grub到/boot**（例如/dev/sda5）  
5. 在Windows中给启动分区分配盘符，使用EasyBCD，安装引导项到启动分区。（EasyBCD请自行摸索）  

##3. 启动  
1. Windows：输入BitLocker密码进入  
2. Debian：选择“选择另一个系统”  

##4. 后记  
1. SSD的速度够快，实际使用中几乎感受不到加密的影响。  
2. 虽然每次进入系统，都需要输入两个密码（分区加密密码、系统登录密码），但是我觉得这值得。  
3. BitLocker在我看来，不是最好的解决办法，但是我们没有其他选择。  
4. 后来因为我的固态硬盘太小（120g），我把Linux分区删除了，把空间分配给了Windows的D盘(￣_￣|||)  

