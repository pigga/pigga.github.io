﻿---
title: java处理office文档与pdf文件(一)
date: 2013-08-22 13:57:00 +0800 
layout: post
permalink: /blog/2013/08/22/java处理office文档与pdf文件(一).html
categories:
  - 问题一箩筐
tags:
  - JAVA
  - POI
---

需求说明：<br/>
用户可以上传word,excel,ppt,pdf文件。在页面能够预览该文件，并可以通过搜索，找到对应的文件记录。<br/>
使用技术：<br/>
通过jacob将office转化为html，使用poi进行文件提取；<br/>
在前期调研的时候，搜索其他将office转化为html的技术，发现其转化之后的页面都不怎么逼真。但是，使用jacob转化的时候样式还可以就是有一点，该项目必须部署在windows环境上。通过协调之后，准备放弃兼容性使用jacob做html的转化。对于pdf的处理思路，在搜索pdf转化时，发现很多技术转化之后，文件都不怎么好看。想到直接使用html的embed标签实现。因为该项目主要在内网运行，所以加载相对较快。但是在使用该方案时，必须在ie时设置ActiveX的级别，并且客户端主机需安装对应的pdf阅读器。<br/>
数据库：<br/>
oracle10g<br/>
**实现思路整理**：<br/>
###### 1、文件上传至upload文件夹
###### 2、将文件转化为html;
###### 3、提取文件内容以作搜索使用。
 
将会在下一章编辑具体的代码实现，敬请期待。
 
第二章 传送门 
 http://pigga.iteye.com/blog/1929378