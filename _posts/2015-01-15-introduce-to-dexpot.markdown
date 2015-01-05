---
layout: post
title: "Dexpot软件介绍"
date: 2015-01-05 16:06
categories: software
---

[Dexpot][dexpot-official-site]是一款虚拟桌面软件，[小众软件][appin-dexpot]有对它的介绍，简单操作不再赘述。
Dexpot有3项功能，非常方便日常开发使用：
1. 屏幕分辨率设置
2. 创建规则自动分组正式库、测试库程序
3. 桌面文字提醒
下文将一一介绍。

文中提到的EosBuilder.exe（简称为平台）、Eos.exe（简称为前台）、EosSoft等都是我工作中使用的软件，它们可以被替换为任意其他的软件（如eclipse.exe、sublime_text.exe）

1. 屏幕分辨率设置
实际需求
工作中需要自定义单据前台展示界面，客户的电脑多是1024*768分辨率（或更高一点），故开发时屏幕分辨率需要设置成1024*768。而日常应用需要高分辨率，手动切换比较麻烦。
解决办法
在Dexpot的“配置桌面”中，可以分别设定每个桌面的分辨率。设置完成后使用Dexpot点击一下就能够切换（配合键盘快捷键可以不需要使用鼠标）。

2. 创建规则自动分组正式库、测试库程序
实际需求
开发过程中有同时登陆正式数据库与测试数据库，进行开发->测试->发布的需求。
同时开启多个Eosbuilder时，图标会重叠在一起。平台界面最下方有提示当前连接的数据库，但是每次操作前都要确认一遍非常繁琐。要是打算在测试库中删除销售订单单据，而不小心在正式库中删除了，损失“分分钟几百万上下”。
解决办法
复制Eosbuilder开发平台文件夹，分别命名为正式库、测试库，并在桌面建立“EosBuilder正式库”、“EosBuilder测试库”的快捷方式，可以解决图标重叠的问题，但由于它们的图标天生相同（使用PE.Explorer应该可以自定义图标，尚未尝试），区分度还是不够。
一劳永逸的办法：
首先将正式库中的EosBuilder.exe重命名为EosBuilderZS.exe，Eos.exe重命名为EosZS.exe；测试库中的EosBuilder.exe重命名为EosBuilderCS.exe，Eos.exe重命名为EosCS.exe。
然后在Dexpot的“桌面规则”中，创建4个规则，分别为
EosBuilderZS正式在左、EosZS正式在左、EosBuilderCS测试在右、EosCS测试在右


[dexpot-official-site]: http://dexpot.de/
[appin-dexpot]: http://www.appinn.com/dexpot/
