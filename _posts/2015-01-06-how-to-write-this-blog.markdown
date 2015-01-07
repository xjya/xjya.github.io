---
layout: post
title: "如何写本博客"
date: 2015-01-06 12:06
categories: 進芫
permalink: /how-to-write-this-blog.html
identifier: 20150106
---

#1. 成为合作编辑者  
需要先联系我，在项目设置中添加合作者。（需要github.com账号）

#2. 下载客户端  
下载[`Github for Windows`](https://windows.github.com/)或者[`GitHub for Mac`](https://mac.github.com/)。  

#3. 克隆项目文件  
猛戳[`这里`](github-windows://openRepo/https://github.com/xjya/xjya.github.io)，找个位置保存项目。  

#4. 开始写博客  
打开`\xjya.github.io\_posts`目录，新建一个文件，文件名要求是`年-月-日-标题.markdown`，如`2015-01-06-how-to-write-this-blog.markdown`  
文件开头有固定格式：  
{% highlight ruby %}
---  
layout: post  
title: "如何写本博客"  
date: 2015-01-06 12:06  
categories: 進芫  
permalink: /how-to-write-this-blog.html  
identifier: how-to-write-this-blog  
---  
{% endhighlight %}
`categories`填写小君、油油、進芫、bobo中的一个。  
`permalink`填一个你觉得好听的名字。
`identifier`用于评论的唯一码，起个唯一的名字。两篇博客需共享评论则设为相同。  
文件内容使用markdown语法，使用[`马克飞象`](http://maxiang.info/)来试试markdown语法吧~上手就会，根本不用教~  

#5. 发布博客
在Github客户端中，点击Uncommitted changes，输入Summary和Description。  
如果没有重要的更新，可以只输入时间。  
	小窍门
	搜狗输入法中，只需要输`rq`就能插入日期，`sj`就能插入时间。  
最后点客户端右上角的Sync，一篇博客就完成啦~


